<template>
  <form action="" @submit.prevent="addTodo">
    <fieldset role="group">
      <input v-model="newTodo" type="text" placeholder="Tâche à effectuer">
      <button :disabled="newTodo === ''">Ajouter</button>
    </fieldset>
  </form>
  
  <div v-if="todos.length === 0">
    Vous n'avez pas de tâches à faire.
  </div>
  
  <div v-else>
    <ul>
      <li v-for="todo in sortedTodos" :key="todo.date" :class="{completed: todo.completed}">
        <label>
          <input type="checkbox" v-model="todo.completed">
          {{ todo.title }}
        </label>
      </li>
    </ul>
    
    <label>
      <input type="checkbox" v-model="hideCompleted">
      Masquer les tâches complétées
    </label>
  </div>
  <checkbox label = "Bonjour"/>
</template>

<script setup>
import { ref, computed } from 'vue';
import checkbox from './checkbox.vue';

const newTodo = ref('');
const hideCompleted = ref(false);
const todos = ref([
  { title: 'Tâche de test', completed: true, date: 1 },
  { title: 'Tâche à faire', completed: false, date: 2 }
]);

// Fonction pour ajouter une nouvelle tâche
const addTodo = () => {
  if (newTodo.value.trim()) {
    todos.value.push({
      title: newTodo.value.trim(),
      completed: false,
      date: Date.now()
    });
    newTodo.value = ''; // Réinitialiser l'input
  }
};

// Fonction computed pour obtenir les tâches triées
const sortedTodos = computed(() => {
  // Tri des tâches en mettant les non-complétées avant les complétées
  const sorted = [...todos.value].sort((a, b) => a.completed - b.completed);
  
  // Filtrer si l'option "Masquer les tâches complétées" est activée
  return hideCompleted.value ? sorted.filter(todo => !todo.completed) : sorted;
});
</script>

<style>
.completed {
  opacity: .5;
  text-decoration: line-through;
}
</style>
