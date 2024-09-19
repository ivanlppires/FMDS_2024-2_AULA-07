<template>
    O nome do usuário é {{  app.getUserName }} 
</template>

<script setup>
import { useAppStore } from '@/stores/app'
const app = useAppStore();
</script>
