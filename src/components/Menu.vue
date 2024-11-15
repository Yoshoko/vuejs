<template>
    <nav class="menu">
        <ul>
            <li><a href="#">Accueil</a></li>
            <li><a href="#">Œuvres</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>
</template>

<script>
export default {
    name: 'Menu'
};
</script>

<style scoped>
.menu {
    list-style: none;
    padding: 0;
    margin: 0;
    text-decoration: none;
}

.menu ul {
    display: flex;
    flex-direction: column;
    gap: 10px;
    list-style: none;
}

.menu li {
    font-weight: bold;
    
}

.menu a {
    color: #333;
}

</style>
