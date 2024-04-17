<template>
  <a href="https://naver.com"
  target="_blank"
  @click.prevent.once="handler">
  NAVER
</a>
</template>

<script>
export default {
  methods: {
    handler(event){
      console.log(event)
    }
  }
}

</script>

<style>
  a {
    font-size: 100px;
  }
</style>