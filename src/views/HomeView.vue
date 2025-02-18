<template>
  <div class="container">
    <TodoList />
    <div style="margin-top: 10px;" />
    <main class="home-grid">
      <MaterialList />
      <PiecesList />
    </main>
  </div>
</template>

<script>
import MaterialList from '@/components/MaterialList.vue';
import PiecesList from '@/components/PiecesList.vue';
import TodoList from '@/components/TodoList.vue';

export default {
  name: "HomeView",
  components: {
    MaterialList,
    TodoList,
    PiecesList
  },
  data() {
    return {
    }
  }
};
</script>
<style scoped>
.container {
  margin:auto;
  width: 90%;
  max-width: 1200px;
}

.home-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
}
</style>
