<template>
  <div class="assigned-jobs-container">
    <!-- Tab Navigation -->
    <div class="tab-navigation">
      <div
        v-for="tab in tabs"
        :key="tab"
        :class="['tab-item', { active: activeTab === tab }]"
        @click="activeTab = tab"
        tabindex="0"
        role="tab"
        :aria-selected="activeTab === tab"
      >
        {{ tab }}
      </div>
    </div>

    <!-- Section Header -->
    <div class="section-header">
      <div class="section-title">
        <span class="section-text">Assigned Job to</span>
        <span class="candidate-name">William Sample</span>
      </div>
      <div class="header-actions">
        <button class="btn btn-primary assign-btn" @click="assignToJob">Assign To Job</button>
        <button class="btn btn-outline view-all-btn" @click="viewAllJobs">View All Assigned Jobs</button>
      </div>
    </div>

    <!-- Job List -->
    <div class="job-list">
      <AssignedJobItem
        v-for="job in jobs"
        :key="job.id"
        :job="job"
        @view-files="viewFiles"
        @toggle-job="toggleJob"
      />
    </div>
  </div>
</template>

<script>
import AssignedJobItem from './AssignedJobItem.vue';
export default {
  name: 'AssignedJobsSection',
  components: { AssignedJobItem },
  data() {
    return {
      activeTab: 'Assigned Jobs',
      tabs: [
        'All Details',
        'Assigned Jobs',
        'Related Emails',
        'Candidate Questions',
        'Hotlists',
        'Related Deals',
        'Contact(s) Pitched'
      ],
      jobs: [
        {
          id: 1,
          title: 'Senior Product Manager',
          source: 'Recruit CRM',
          candidate: 'William Sample',
          date: 'Jul 10, 2023',
          status: 'Assigned',
          isActive: true
        },
        {
          id: 2,
          title: 'Senior Product Manager',
          source: 'Recruit CRM',
          candidate: 'William Sample',
          date: 'Jul 10, 2023',
          status: 'Assigned',
          isActive: true
        },
        {
          id: 3,
          title: 'Senior Product Manager',
          source: 'Recruit CRM',
          candidate: 'William Sample',
          date: 'Jul 10, 2023',
          status: 'Assigned',
          isActive: true
        }
      ]
    }
  },
  methods: {
    assignToJob() {
      this.$emit('assign-to-job');
    },
    viewAllJobs() {
      this.$emit('view-all-jobs');
    },
    viewFiles(jobId) {
      this.$emit('view-files', jobId);
    },
    toggleJob(jobId) {
      this.$emit('toggle-job', jobId);
    }
  }
}
</script>

<style scoped>
@import '@/assets/styles/_common.scss';
.assigned-jobs-container {
  background: white;
  font-family: var(--font-main);
}

.tab-navigation {
  display: flex;
  border-bottom: 1px solid #e0e0e0;
  background: #f8f9fa;
}

.tab-item {
  padding: 12px 16px;
  cursor: pointer;
  font-size: 14px;
  color: #666;
  border-bottom: 3px solid transparent;
  white-space: nowrap;
}

.tab-item.active {
  color: var(--primary-color);
  border-bottom-color: var(--primary-color);
  font-weight: 500;
}

.tab-item:hover:not(.active) {
  color: #333;
}

.section-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 16px 20px;
  border-bottom: 1px solid #e0e0e0;
}

.section-title {
  font-size: 14px;
}

.section-text {
  color: #666;
}

.candidate-name {
  color: #333;
  font-weight: 500;
  margin-left: 4px;
}

.header-actions {
  display: flex;
  gap: 12px;
}

.job-list {
  padding: 0 20px;
}
</style>