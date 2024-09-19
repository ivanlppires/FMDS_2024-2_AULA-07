<template>
    <v-list>
        <v-list-subheader>Clientes</v-list-subheader>
        <v-list-item v-for="user in users" :key="user.id">
            <v-btn variant="text" :to="'/user/' + user.id">
                {{  user.name  }}</v-btn>
        </v-list-item>
    </v-list>
</template>
<script setup>
    import { useUsersStore } from '@/stores/users';
    const users = useUsersStore().getUsers;
</script>