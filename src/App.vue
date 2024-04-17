<template>
  <!-- <Vif /> -->
  <!-- <Vfor /> -->
  <EventHandling />
</template>

<script>
import Vif from '@/components/Vif.vue'
import Vfor from '@/components/Vfor.vue'
import EventHandling from '@/components/EventHandling.vue'

export default {
  components: {
    Vif: Vif,
    Vfor: Vfor,
    EventHandling: EventHandling
  }
}
</script>


// 스타일데이터타입에서 객체타입으로 변경 배열형태로 객체 묶음
<!-- <template>
  <h1
    :style="[fontStyle, backgroundStyle]"
    @click="changeStyle">
    Hello?!
  </h1>
</template>


<script>
export default {
  data() {
    return {
      fontStyle: {
        color: 'orange',
        fontSize: '30px'
      },
      backgroundStyle: {
        backgroundColor: 'black'
      }
    }
  },
  methods: {
    changeStyle() {
      this.fontStyle.color = 'red'
      this.fontStyle.fontSize = '50px'
    }
  }
}
</script> -->


// 클래스 바인딩
<!-- <template>
  <h1
  :class="{active: isActive}"
  @click="activate">
    Hello?!({{ isActive }})
  </h1>

</template>

<script>
export default {
  data() {
    return {
      isActive: false
    }
  },
    methods: {
    activate() {
      this.isActive = !this.isActive
    }
  }
}
</script>

<style scoped>
  .active{
    color: red;
    font-weight: bold;
  }
</style> -->


// 옵션에 관하여
<!-- <template>
  <button @click='add'>
    ADD
  </button>
  <h1>{{ msg.split('').reverse().join('') }}</h1>
  <h1>{{ reverseMessage() }}</h1>
  <h1>{{ reversedMessage }}</h1>
  <h1>{{ reversedMessageGS }}</h1>
  <h1 @click="changeMessage">{{ msg }}</h1>
</template>

<script>
export default {
  data() {
    return {
      // Getter, Setter
      msg: 'Hello Computed!'
    }
  },
  computed: {
    // 캐싱을 통해서 한번만 연산함
    // Getter
    reversedMessage(){
      return this.msg.split('').reverse().join('')
    },
    reversedMessageGS: {
      get() {
        return this.msg.split('').reverse().join('')
      },
      set(value) {
        this.msg = value
      }
    }
  },
  // 특정데이터가 변경되었음을 감시
  watch: {
    msg(newValue) { // 매개변수는 변경된 값
      console.log('msg: ', newValue)
    },
    // computed로 변경된 값도 감시 가능
    reversedMessage(newValue){
      console.log('reversedMessage: ', newValue)
    }
  },
  methods: {
    // 부를때마다 연산함
    reverseMessage() {
      return this.msg.split('').reverse().join('')
    },
    add(){
      this.reversedMessageGS += '!?'
    },
    changeMessage(){
      this.msg = 'Good!'
    }
  }
}
</script> -->


<!-- <template>
  <Fruit />
</template>


<script>
import Fruit from '@/components/Fruit.vue'

export default {
  components: {
    Fruit
  }
}
</script> -->


<!-- <template>
  <h1 @click="increase">
    {{ count }}
  </h1>
  <div v-if="count > 4">
    4보다 큽니다!
  </div>
  <ul>
    <Fruit
      v-for="fruit in fruits"
      :key="fruit"
      :name="fruit">
      {{ fruit }}
    </Fruit>
  </ul>

  <h1 v-bind:class="msg">
    {{ msg }}
  </h1>

</template>

<script>
// import Fruit from 'C:/_programing/vue-test/src/components/Fruit.vue'
import Fruit from '@/components/Fruit.vue'

export default {
  components: {
    Fruit: Fruit
  },
  data() {
    return {
      count: 0,
      fruits: ['Apple', 'Banana', 'Cherry'],
      msg: 'active'
    }
  },
  methods: {
    increase() {
      this.count += 1;
    },
    add(){
      this.msg +='!';
    }
  }
}
</script>

<style lang="scss">
  h1 {
    font-size: 50px;
    color: royalblue;
  }

  ul{
    li{
      font-size: 40px;
    }
  }

  .active {
    color:red;
    font-size: 100px;
  }
</style> -->