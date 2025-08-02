// src/components/Tabs.vue
<template>
  <div class="tabs">
    <div class="tab-buttons">
      <button
        v-for="tab in tabs"
        :key="tab"
        :class="['tab-button', { active: activeTab === tab }]"
        @click="activeTab = tab"
      >
        {{ tab }}
      </button>
    </div>
    <div class="tab-content">
      <slot :name="activeTab.toLowerCase()" />
    </div>
  </div>
</template>

<script>
import '@/assets/styles/tabs.scss';
export default {
  name: 'Tabs',
  data() {
    return {
      tabs: ['Activity', 'Notes', 'Emails'],
      activeTab: 'Activity'
    };
  }
};
</script>
