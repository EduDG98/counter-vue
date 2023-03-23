<script >
import CounterDisplay from './components/CounterDisplay.vue'
import ButtonComponent from './components/ButtonComponent.vue'
import WaveComponent from './components/WaveComponent.vue'

export default {
  name: 'App',
  components: {
    CounterDisplay,
    WaveComponent,
    ButtonComponent
  },
  data() {
    return {
      count: 0
    }
  },
  methods: {
    increment() {
      this.count++;
    },
    decrement() {
      this.count--;
    }
  }
}
</script>

<template>
  <div class="container">
    <ButtonComponent @click="increment" :result='count' symbol="➕" class="plus"></ButtonComponent>
    <CounterDisplay :count='count'></CounterDisplay>
    <ButtonComponent @click="decrement" :result="count" symbol="➖" class="less"></ButtonComponent>
  </div>
  <WaveComponent></WaveComponent>
</template>

<style >
body {
  height: 80vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.container {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 20px;
}
</style>
