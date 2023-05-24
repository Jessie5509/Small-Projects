<template>
    <div class="btn-container">
        <button class="btn-global" @click="toggleBtn(text)">{{ text }}</button>
    </div>
</template>

<script>
export default {
    props: {
        text: { String, default: "Pepe" }
    },
    data() {
        return {}
    },
    methods: {
        toggleBtn(text) {
            this.$emit('toggle-btn', text);
        }
    }
}
</script>
<style scoped>
.btn-container {
    display: inline;
    flex-direction: row;
    justify-content: center;
    margin: 5px 5px 5px 5px;
}

.btn-global {
    cursor: pointer;
    border: none;
    border-radius: 5px;
    padding-top: 6px;
    padding-bottom: 6px;
    padding-left: 10px;
    padding-right: 10px;
    background-color: rgb(173, 165, 165);
}
</style>