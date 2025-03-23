<template>
    <footer>
        <section class="liens">
            <div class="logo">
                <a href="https://github.com/el-ioio" target="_blank">
                    <img src="@/assets/image/github.png" alt="logo cliquable de github">
                </a>
                <a href="https://twitter.com/iordan3725" target="_blank">
                    <img src="@/assets/image/twitter.png" alt="logo cliquable de twitter">
                </a>
            </div>
            <small>Mise à jour le <time datetime="2025-01-10">10/01/2025</time></small>
        </section>
    </footer>
</template>

<style scoped>
section, footer {
    border: 1px solid white;
    background-color: #782221;
}

.liens {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    justify-content: center;
}

section {
    padding: 50px;
}

img {
    height: 50px;
}
</style>