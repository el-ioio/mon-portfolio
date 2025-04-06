<template>
  <div v-if="isOpen" class="modal-overlay" @click="closeModal">
    <div class="modal-content" @click.stop>
      <button class="modal-close" @click="closeModal">x</button>
      <div class="police">
        <h2>{{ title }}</h2>
        <p><strong>Date : </strong>{{ date }}</p>
        <p>{{ description }}</p>
        <p><strong>Technologie utilisée : </strong>{{ technology }}</p>
      </div>
      <a :href="link" id="ouvrir-lien" target="_blank" rel="noopener noreferrer">Voir le projet</a>
      <div v-if="codePdfUrl" class="mt-4 text-right">
        <a :href="codePdfUrl" target="_blank" rel="noopener noreferrer" class="text-blue-600 hover:underline">Voir le code</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    isOpen: {
      type: Boolean,
      required: true,
    },
    title: {
      type: String,
      default: 'Titre du projet',
    },
    date: {
      type: String,
      default: 'Date de création',
    },
    description: {
      type: String,
      default: 'Description du projet',
    },
    link: {
      type: String,
      default: '#',
    },
    technology: {
      type: String,
      default: 'Non spécifiée',
    },
    codePdfUrl: {
      type: String,
      default: '',
    },
  },
  methods: {
    closeModal() {
      this.$emit('close');
    },
  },
};
</script>

<style scoped>
.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background-color: rgba(0, 0, 0, 0.5);
  display: flex;
  align-items: center;
  justify-content: center;
}

.modal-content {
  background-color: white;
  padding: 20px;
  border-radius: 5px;
  position: relative;
  max-width: 500px;
  width: 100%;
}

.modal-close {
  position: absolute;
  top: 10px;
  right: 10px;
  background: transparent;
  border: none;
  font-size: 1.5rem;
  cursor: pointer;
}

.police {
  color: black;
}
</style>