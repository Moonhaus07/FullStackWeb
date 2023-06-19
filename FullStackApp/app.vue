<template>
  <div>
    <h1>Users</h1>
        <table>
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Course</th>
                    <th>Is Active</th>
                    <th>Action</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="user in users" :key="user.id">
                    <td>{{ user.name }}</td>
                    <td>{{ user.course }}</td>
                    <td>{{ user.isActive ? 'Active' : 'Inactive'}}</td>
                    <td>
                        <a class="router-link-active router-link-exact-active" href="/_id.vue"></a>
                        <NuxtLink to= "app/_id.vue">view</NuxtLink>
                    </td>
                </tr>
            </tbody>
        </table>
  </div>
</template>

<script>
export default {
    data() {
        return {
            users: [
                {
                    id: 1001,
                    name:'Mabby Segurog',
                    course: 'BSIT',
                    isActive: true,
                },
                {
                    id: 1002,
                    name:'Caleb Fabila',
                    course: 'BSIT',
                    isActive: true,
                },
                {
                    id: 1003,
                    name:'Calby Haus',
                    course: 'BSIT',
                    isActive: false,
                },
            ],
        };
    },
};
</script>