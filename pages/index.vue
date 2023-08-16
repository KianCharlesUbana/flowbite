<script>
export default {
  data() {
    return {
      user: [
        { 
            id: 1,
            name: 'Jhemar Masarap',
            section: 'BSOAD',
            email: 'kiancharlesubana@gmail.com',
            contact_num: '0951112527'
        },
        { 
            id: 2,
            name: 'JM NOLASCO',
            section: 'BSIT',
            email: 'kiancharlesubana@gmail.com',
            contact_num: '0951112527'
        }
      ], // Initialize an empty array for the fetched data
    };
  },
};
</script>


<template>
  <div>
    <div class="relative overflow-x-auto shadow-md sm:rounded-lg">
      <table class="w-full text-sm text-left text-gray-500 dark:text-gray-400">
        <thead
          class="text-xs text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-gray-400"
        >
          <tr>
            <th scope="col" class="px-6 py-3">ID</th>
            <th scope="col" class="px-6 py-3">Name</th>
            <th scope="col" class="px-6 py-3">Section</th>
            <th scope="col" class="px-6 py-3">Email</th>
            <th scope="col" class="px-6 py-3">Contact No.</th>
            <th scope="col" class="px-6 py-3">Actions</th>
          </tr>
        </thead>
        <tbody  v-for="users in user" :key="users.id">
          <tr class="bg-white border-b dark:bg-gray-800 dark:border-gray-700">
            <td class="px-6 py-4">{{ users.id }}</td>
            <th
              scope="row"
              class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white"
            >
            {{ users.name }}
            </th>
            <td class="px-6 py-4"> {{ users.section }}</td>
            <td class="px-6 py-4"> {{ users.email }}</td>
            <td class="px-6 py-4"> {{ users.contact_num }}</td>
            <td class="px-6 py-4">
              <modal :item="users"/>
              <button
                type="button"
                class="text-white bg-red-700 hover:bg-red-800 focus:outline-none focus:ring-4 focus:ring-red-300 font-medium rounded-full text-sm mt-1 px-5 py-2.5 text-center mr-2 mb-2 dark:bg-red-600 dark:hover:bg-red-700 dark:focus:ring-red-900"
              >
                Delete
              </button>
            </td>
          </tr>
          
        </tbody>
      </table>
    </div>

    
  </div>
</template>