<script>
export default {
    name: 'CounterDisplay',
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
    <button @click="increment()">➕</button>
    <span> {{ count }} </span>
    <button @click="decrement">➖</button>
</template>

<style></style>
