<template>
  <section v-if="hasFruit">
    <h1>Fruits</h1>
    <ul>
      <li v-for="fruit in fruits" :key="fruit">
        {{ fruit }}
      </li>
    </ul>
  </section>
  <section>
    <h1>Reverse Fruits</h1>
    <ul>
      <li v-for="fruit in reverseFruits" :key="fruit">
        {{ fruit }}
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  data() {
    return {
      fruits: [
        'Apple', 'Banana', 'Cherry'
      ]
    }
  },
  computed: {
    hasFruit() {
      return this.fruits.length > 0 // boolean 값 반환
    },
    reverseFruits() {
      return this.fruits.map(fruit => 
        fruit.split('').reverse().join('')
      )
    }
  }
}
</script>

<style>
section {
  font-size: 50px;
}
</style>


<!-- <template>
  <li>{{ name }}?!</li>
</template>

<script>
  export default {
    props: {
      name: {
        type: String,
        default: ''
      }
    },data (){
      return{
        count: 2
      }
    },
    beforeCreate(){
      console.log('before Created!')
      console.log(this.count)
    },
    created(){
      console.log('Created!')
      console.log(this.count)
    },
    beforeMount(){
      console.log('before Mount!')
      console.log(this.count)
      console.log(document.querySelector('h1'))

    },
    mounted() {
      console.log('Mounted!')
      console.log(this.count)
      console.log(document.querySelector('h1'))
    }
  }
</script>
  
<style scoped lang="scss">
  h1{
    color: red !important;
  }
</style> -->