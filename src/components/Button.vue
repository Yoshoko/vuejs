<template>
    <button class="btn">{{ text }}</button>
</template>

<script>
export default {
    name: 'Button',
    props: {
        text: String
    }
};
</script>

<style scoped>
.btn {
    background-color: #e74c3c;
    color: #fff;
    border: none;
    padding: 10px 15px;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
}
</style>
