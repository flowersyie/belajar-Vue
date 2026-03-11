<script setup>
import Counter from './components/icons/Counter.vue'
// // reactive state 
// const count = ref(0)

// // trigger reactivity
// function increment() {
//   count.value++
// }

// const user = reactive({
//   name: 'Marklee',
//   age: 25,
//   email: 'marklee@example.com',
// })

// const tambahUmur = () => {
//   user.age++
// }

// const kurangiUmur = () => {
//   user.age--
// }

// // lifecycle hook
// onMounted(() => {
//   console.log('The initial count is:', count.value)
// })

// const todos = reactive([ 'Mandi', 'Makan', 'Tidur' ])

// const addTodo = () => {
//   todos.push('Mengaji')
// }

</script>

<template>
  <Counter />
  <!-- <div>
    <p> name: {{ user.name }}</p>
    <p> age: {{ user.age }}</p>
    <p> email: {{ user.email }}</p>
    <button @click="kurangiUmur">Kurang</button>
    <button @click="tambahUmur">Tambah</button>
  </div> -->

  <!-- <div>
    <h3>Kegiatan Sehari - hari</h3>
    <ul>
      <li v-for="todo in todos" :key="todo">
        {{ todo }}
      </li>
    </ul>
    <button @click="addTodo">Tambah Kegiatan</button>
  </div> -->

 
</template>

<style scooped></style>