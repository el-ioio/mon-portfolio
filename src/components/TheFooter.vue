<template>
    <main id="contact">
        <h1>Me contacter</h1>
        <br>
        <br>
        <form @submit.prevent="sendMessage">
            <p>
                Nom, prénom :
                <textarea v-model="pseudo" name="pseudo"></textarea>
            </p>
            <br>
            <br>
            <p>
                Adresse e-mail :
                <textarea v-model="email" name="e-mail"></textarea>
            </p>
            <br>
            <br>
            <p>
                Votre commentaire, message :
                <textarea v-model="commentaire" name="commentaire"></textarea>
            </p>
            <br>
            <br>
            <input class="bouton" type="submit" value="Envoyer">
        </form>
        <div v-if="messageSent" class="confirmation-message">
            ✅ Votre message a bien été envoyé à {{ staticEmail }} !
        </div>
    </main>
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
            <small>Mise à jour le <time datetime="20254-12-10">10/12/2024</time></small>
        </section>
    </footer>
</template>

<script>
export default {
    data() {
        return {
            messageSent: false,
            pseudo: '',
            email: '',
            commentaire: '',
            staticEmail: import.meta.env.VITE_EMAIL,
        };
    },
    methods: {
        sendMessage() {
            console.log(`Message envoyé par : ${this.pseudo}`);
            console.log(`Adresse e-mail : ${this.email}`);
            console.log(`Message : ${this.commentaire}`);
            
            this.messageSent = true;
            
            this.pseudo = '';
            this.email = '';
            this.commentaire = '';
            
            setTimeout(() => {
                this.messageSent = false;
            }, 5000);
        }
    }
};
</script>

<style scoped>
main, footer {
    border: 1px solid white;
    background-color: #782221;
}

h1 {
    display: flex;
    justify-content: center;
}

.bouton {
    border-radius: 25px;
}

.liens {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    justify-content: center;
}

form {
    width: 50%;
    margin: auto;
}

main {
    padding: 50px;
}

textarea {
    position: relative;
    top: 22px;
}

img {
    height: 50px;
}

.confirmation-message {
    margin-top: 20px;
    padding: 10px;
    background-color: #d4edda;
    color: #155724;
    border: 1px solid #c3e6cb;
    border-radius: 5px;
    text-align: center;
    font-size: 16px;
}
</style>