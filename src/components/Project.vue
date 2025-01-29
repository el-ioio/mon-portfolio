<template>
  <div class="project-container">
    <h3 class="project-title">{{ project.title }}</h3>
    <img :src="project.image" :alt="project.title" @click="openModal" class="project-image" />
    <TheModal
      :isOpen="isModalOpen"
      :title="project.title"
      :date="project.date"
      :description="project.description"
      :link="project.link"
      :technology="project.technology"
      @close="isModalOpen = false"
    />
  </div>
</template>

<script>
import TheModal from './modal/TheModal.vue';

export default {
  components: {
    TheModal,
  },
  props: {
    project: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {
      isModalOpen: false,
    };
  },
  methods: {
    openModal() {
      this.isModalOpen = true;
    },
  },
};
</script>

<style scoped>
.project-image {
  width: 100%;
  cursor: pointer;
  object-fit: cover;
  border-radius: 5px;
  transition: transform 0.2s ease;
}

.project-image:hover {
  transform: scale(1.05);
}

.project-container {
  text-align: center;
  margin: 20px;
  width: 500px;
}

.project-title {
  font-size: 90%;
}
</style>