<script>
export default {
    name: 'CounterDisplay',
    props: {
        count: {
            type: Number,
            default: 1000,
            required: true
        }

    },
    data() {
        return {
            counter: this.count
        }
    }
}
</script>

<template>
    <span> {{ count }} </span>
</template>

<style>
span {
    min-width: 100px;
    min-height: 50px;
    padding: 20px;
    background-color: #EA5455;
    border-radius: 100% 0% 100% 0% / 100% 0% 100% 0%;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 30px;
}
</style>
