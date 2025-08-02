// src/components/AssignedJobs.vue
<template>
  <div class="assigned-jobs">
    <h3>Assigned Jobs (3)</h3>
    <div class="job-cards">
      <div class="job-card" v-for="job in jobs" :key="job.title">
        <h4>{{ job.title }}</h4>
        <p>{{ job.company }}</p>
        <p class="meta">{{ job.location }} • {{ job.type }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import '@/assets/styles/assigned-jobs.scss';
export default {
  name: 'AssignedJobs',
  data() {
    return {
      jobs: [
        {
          title: 'Senior Product Manager',
          company: 'Facebook',
          location: 'Remote',
          type: 'Full Time'
        },
        {
          title: 'Senior Product Manager',
          company: 'Google',
          location: 'Remote',
          type: 'Contract'
        },
        {
          title: 'Senior Product Manager',
          company: 'Netflix',
          location: 'USA',
          type: 'Part Time'
        }
      ]
    };
  }
};
</script>

