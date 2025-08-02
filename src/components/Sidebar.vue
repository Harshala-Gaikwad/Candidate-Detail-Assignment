<template>
  <aside class="sidebar">
    <div v-for="icon in icons" :key="icon.alt" class="icon-wrapper">
      <img :src="icon.src" :alt="icon.alt" class="icon" />
    </div>
  </aside>
</template>

<script>
import '@/assets/styles/sidebar.scss';
export default {
  name: 'Sidebar',
  data() {
    return {
      icons: [
        { src: '/src/assets/icons/dashboard.png', alt: 'Dashboard' },
        { src: '/src/assets/icons/candidates.png', alt: 'Candidates' },
        { src: '/src/assets/icons/email.png', alt: 'Email' },
        { src: '/src/assets/icons/notes.png', alt: 'Notes' },
        { src: '/src/assets/icons/tasks.png', alt: 'Tasks' },
        { src: '/src/assets/icons/search.png', alt: 'Search' },
        { src: '/src/assets/icons/settings.png', alt: 'Settings' },
      ]
    }
  }
}
</script>
