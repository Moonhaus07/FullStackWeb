<template>
    <div>
        <h1>User</h1> <br>
        <button>Back</button>
        <h1>{{ user.name }}</h1>
        <p>Course: {{ user.course }}</p>
        <p>Is Active: {{ user.isActive ? 'Active' : 'Inactive' }}</p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            user: null,
        };
    },
    mounted() {
        const userID = this.$route.params.id;
        this.fetchUser(userID)
    },
    methods: {
        fetchUser(userID) {
            this.user = {
                id: userID,
                name:'Mabby Segurog',
                course: 'BSIT',
                isActive: true,
            };
        },
        goBack() {
            this.$$router.go(-1);
        },
    },
};
</script>