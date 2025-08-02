<!-- src/App.vue -->
<template>
  <div class="app-wrapper">
    <Sidebar />
    <div class="main-content">
      <Header />
      <CandidateProfile />
    </div>
  </div>
</template>

<script>
import Sidebar from '@/components/Sidebar.vue';
import Header from '@/components/Header.vue';
import CandidateProfile from '@/views/CandidateProfile.vue';

export default {
  name: 'App',
  components: {
    Sidebar,
    Header,
    CandidateProfile
  }
};
</script>

<style scoped>
.app-wrapper {
  display: flex;
  height: 100vh;
  overflow: hidden;
  font-family: Arial, sans-serif;
}

.main-content {
  flex: 1;
  display: flex;
  flex-direction: column;
  overflow-y: auto;
  background-color: #f5f7fa;
}
</style>
