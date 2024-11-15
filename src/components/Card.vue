<template>
    <div class="card" :class="{ 'card-horizontal': !main, 'card-vertical': main }">
        <img :src="src" alt="Image de la Card" class="img-fluid mb-3 image-about" v-if="main" />
        <div class="card-body">
            <h3>{{ title }}</h3>
            <p>{{ description }}</p>
            <slot></slot>
        </div>
        <img :src="src" alt="Image de la Card" class="img-fluid mb-3 image-vertical" v-if="!main" />
    </div>
</template>

<script>
export default {
    name: 'Card',
    props: {
        main: {
            type: Boolean,
            default: true
        },
        title: String,
        description: String,
        src: String
    }
};
</script>

<style scoped>

.card-body p {
    width: 250px;
}
.card {
    display: flex;
    align-items: center;
    padding: 15px;
}

.card-horizontal {
    flex-direction: row;
}

.card-vertical {
    flex-direction: column;
}

.card-body {
    flex: 1;
    margin-left: 15px;
}

.img-fluid {
    max-width: 100%;
    height: auto;
}

.image-about {
    width: 100%;
    max-height: 300px;
    object-fit: cover;
}

.image-vertical {
    max-width: 200px;
    height: auto;
    object-fit: cover;
}</style>
