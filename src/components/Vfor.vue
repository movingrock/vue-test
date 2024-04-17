<template>
  <div>
    <button @click="handler">
      Click me!
    </button>
  </div>

  <ul>
    <li v-for="(fruit,index) in fruits"
    :key="fruit">
      {{ fruit }}-{{ index + 1}}
    </li>
    <li v-for=" {id, name} in newFruits"
    :key="id">
    {{ name }}-{{ id }}
    </li>
  </ul>
</template>

<script>
import { nanoid } from 'nanoid'

export default {
  data() {
    return {
      fruits: ['Apple', 'Banana', 'Cherry']
    }
  },
  computed:{
    newFruits() {
      return this.fruits.map(fruit => ({
          id: nanoid(),
          name: fruit
      }))
    }
  },
  methods: {
    handler() {
      this.fruits.push('Orange')
    }
  }
}
</script>

<style scoped>
  li {
    font-size: 50px;
  }
</style>