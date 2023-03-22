<script >
import CounterDisplay from './components/CounterDisplay.vue'
import WaveComponent from './components/WaveComponent.vue';
export default {
  name: 'App',
  components: {
    CounterDisplay,
    WaveComponent
  },
  data() {
    return {

    }
  }
}
</script>

<template>
  <CounterDisplay></CounterDisplay>
  <WaveComponent></WaveComponent>
</template>

<style ></style>
