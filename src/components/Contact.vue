<template>
    <section id="contact">
        <h2>Me contacter</h2>
        <form @submit.prevent="sendMessage">
            <p>
                Nom, prénom :
                <textarea v-model="pseudo" name="pseudo"></textarea>
            </p>
            <p>
                Adresse e-mail :
                <textarea v-model="email" name="e-mail"></textarea>
            </p>
            <p>
                Votre commentaire, message :
                <textarea v-model="commentaire" name="commentaire"></textarea>
            </p>
            <input class="bouton" type="submit" value="Envoyer">
        </form>
        <div v-if="messageSent" class="confirmation-message">
            ✅ Votre message a bien été envoyé à {{ staticEmail }} !
        </div>
    </section>
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

<style>
section {
    border: 1px solid white;
    background-color: #782221;
}

h2 {
    display: flex;
    justify-content: center;
}

.bouton {
    border-radius: 25px;
}

form {
    width: 50%;
    margin: auto;
}

section {
    padding: 50px;
}

textarea {
    position: relative;
    top: 22px;
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

p, h2, .bouton{
    margin: 50px auto;
}
</style>