    <template>
        Buscar as informações do usuário: {{ user }}
    </template>
<script setup>
import { useRoute } from 'vue-router';
import { useUsersStore } from '@/stores/users';

const $route = useRoute();
const store = useUsersStore();
const user = store.getUserById($route.params.id);

</script>