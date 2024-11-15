<template>
    <div class="image-quartet">
        <img v-for="(image, index) in images" :key="index" :src="image" alt="Image" />
    </div>
</template>

<script>
export default {
    props: {
        images: Array
    }
};
</script>

<style scoped>
.image-quartet {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 0;
    width: 400px;
    height: 400px;
    margin: auto;
}

.image-quartet img {
    width: 100%;
    height: 100%;
    object-fit: fill;
}</style>
