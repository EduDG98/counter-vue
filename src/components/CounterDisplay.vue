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
    <div class="container">
        <button @click="increment()" class="plus">➕</button>
        <span> {{ count }} </span>
        <button @click="decrement" class="less">➖</button>
    </div>
</template>

<style>
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

span {
    min-width: 100px;
    min-height: 50px;
    padding: 20px;
    background-color: palevioletred;
    border-radius: 100% 0% 100% 0% / 100% 0% 100% 0%;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 30px;
}

button {
    padding: 25px;
    background-color: peachpuff;
    transition: all 1s;
}

button.plus {
    clip-path: polygon(100% 0%, 75% 50%, 100% 100%, 25% 100%, 0% 50%, 25% 0%);
    border-radius: 100% 0% 0% 100% / 50% 0% 100% 50%;


}

button.less {
    clip-path: polygon(75% 0%, 100% 50%, 75% 100%, 0% 100%, 25% 50%, 0% 0%);
    border-radius: 0% 100% 100% 0% / 0% 50% 50% 100%;
}

button.plus:active {
    transform: scale(0.9);
}

button.less:active {
    transform: scale(0.9);
}
</style>
