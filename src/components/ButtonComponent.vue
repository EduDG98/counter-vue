<script>
export default {
    name: 'ButtonComponent',
    props: {
        symbol: {
            type: String,
            default: '❌',
            required: true
            // validator
        }
    }
}
</script>

<template>
    <button>{{ symbol }}</button>
</template>

<style>
button {
    padding: 25px;
    background-color: #E4DCCF;
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