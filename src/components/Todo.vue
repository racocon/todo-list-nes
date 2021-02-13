<template>
  <div class="todo">
    <h2 class="center-align">{{ msg }}</h2>

    <!-- Add todo list -->
    <input 
      type="text" 
      class="nes-input" 
      placeholder="Add todo..."
      v-on:keyup.enter="addTodo">

    <ul>
    <!-- Todo list -->
      <li 
        v-for="todo in todos"
        :key="todo.id"
        class="flex">

        <label>
          <input 
            type="checkbox" 
            class="nes-checkbox"
            v-model="todo.done">
          <span>&nbsp;</span>
        </label>

        <del v-if="todo.done">{{ todo.text }}</del>
        <span v-else>{{ todo.text }}</span>
        
        <div class="space"></div>
        <button 
          class="nes-btn is-error padding"
          v-on:click="removeTodo(todo.id)">X</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Todo',
  data () {
    return {
      msg: 'TODOS:',

      todos: [
        { text: 'Create a todo list using Vue.js', done: true, id: Date.now() },
        { text: 'Get scholarship from Krenovator', done: false, id: Date.now() + 1 },
        { text: 'Reach Platinum rank in Apex', done: false, id: Date.now() + 2 }
      ]
    }
  },
  methods: {
    // Add todo into the list
    addTodo(event) {
      const text = event.target.value
      this.todos.push({text, done: false, id: Date.now()})
      event.target.value = ''
    },

    // Remove todo from the list
    removeTodo(id) {
      this.todos = this.todos.filter(todo => todo.id !== id)
    },

    // Check todo as done in the list
    check(todo) {
      todo.done = !todo.done
    }
  }
}
</script>

<style scoped>

li {
  margin: 8px;
}

label {
  margin: 5px;
}

del {
  color: rgba(0, 0, 0, 0.3);
}

</style>
