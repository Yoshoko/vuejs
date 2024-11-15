<template>
    <div class="social-links">
        <a v-for="(link, index) in links" :key="index" :href="link.url" target="_blank">
            <i :class="getIconClass(link.name)"></i>
        </a>
    </div>
</template>

<script>
export default {
    name: 'SocialLinks',
    props: {
        links: Array
    },
    methods: {
        getIconClass(name) {
            switch (name.toLowerCase()) {
                case 'facebook':
                    return 'fab fa-facebook-f';
                case 'twitter':
                    return 'fab fa-twitter';
                case 'pinterest':
                    return 'fab fa-pinterest';
                case 'linkedin':
                    return 'fab fa-linkedin-in';
                case 'instagram':
                    return 'fab fa-instagram';
                default:
                    return '';
            }
        }
    }
};
</script>

<style scoped>
.social-links {
    display: flex;
    justify-content: left;
    margin-left: 32px;
    gap: 10px;
    margin-top: 20px;
}

.social-links a {
    color: #555;
    font-size: 24px;
    text-decoration: none;
}

.social-links a:hover {
    color: #007bff;
}
</style>
