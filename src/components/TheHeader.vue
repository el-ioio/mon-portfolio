<template>
    <header id="presentation" class="head">
        <h1>Portfolio de Iordan Mazette</h1>
        <nav>
            <ul>
                <li><a href="#presentation">Accueil</a></li>
                <li><a href="#projets">Projets</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
        <nav class="remonte">
            <a href="#presentation">
                <img src="/fleche-remonte.jpg" alt="remonte la page">
            </a>
        </nav>
    </header>
</template>

<style scoped>
h1 {
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 300%;
}

nav {
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 120%;
}

* {
    font-family: 'raleway';
}

.remonte {
    position: fixed;
    bottom: -5px;
    right: -576px;
}

.remonte a img {
    width: 10%;
}
</style>