// div가 아니라 template로 해야 요소가 사라지고 한번에 나타남 div로 하면 div...div로 가려져있음
<template>
  <button @click="handler">
    click me!
  </button>
  <h1 v-if="isShow">
    Hello?!
  </h1>
  <h1 v-else-if="count > 3">
    Count > 3
  </h1>
  <h1 v-else>
    Good~
  </h1>

  <template v-if="isShow">
    <h1>1</h1>
    <p>2</p>
    <p>3</p>
  </template>
  <h1 v-show"isShow">
    Hello?!
  </h1>
</template>

<script>
export default {
  data() {
    return{
      isShow: true,
      count: 0
    }
  },
  methods: {
    handler(){
      this.isShow = !this.isShow,
      this.count += 1
    }
  }
}
</script>