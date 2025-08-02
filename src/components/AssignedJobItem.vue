<template>
  <div class="job-item">
    <div class="job-avatar flex-center">{{ job.candidate.charAt(0) }}</div>
    <div class="job-details">
      <div class="job-title text-ellipsis">{{ job.title }}</div>
      <div class="job-source text-ellipsis">{{ job.source }}</div>
    </div>
    <div class="job-info">
      <div class="candidate-info flex-center">
        <div class="candidate-icon">👤</div>
        <span class="candidate-text text-ellipsis">{{ job.candidate }}</span>
      </div>
      <div class="date-info flex-center">
        <div class="date-icon">📅</div>
        <span class="date-text">{{ job.date }}</span>
      </div>
    </div>
    <div class="job-status">
      <span class="status-badge">{{ job.status }}</span>
    </div>
    <div class="job-actions">
      <button class="btn btn-outline view-files-btn" @click="$emit('view-files', job.id)">View Files</button>
      <div class="toggle-switch">
        <input
          type="checkbox"
          :id="'toggle-' + job.id"
          v-model="localActive"
          @change="$emit('toggle-job', job.id)"
          :aria-checked="localActive.toString()"
        >
        <label :for="'toggle-' + job.id" class="toggle-label" :aria-label="'Toggle job ' + job.title"></label>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AssignedJobItem',
  props: {
    job: {
      type: Object,
      required: true
    }
  },
  data() {
    return {
      localActive: this.job.isActive
    }
  },
  watch: {
    'job.isActive'(val) {
      this.localActive = val;
    }
  }
}
</script>

<style scoped>
@import '@/assets/styles/_common.scss';
.job-item {
  display: flex;
  align-items: center;
  padding: 16px 0;
  border-bottom: 1px solid #f0f0f0;
  gap: 16px;
}
.job-item:last-child {
  border-bottom: none;
}
.job-avatar {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background: #ffa726;
  color: white;
  font-weight: 600;
  font-size: 16px;
  flex-shrink: 0;
}
.job-details {
  flex: 1;
  min-width: 0;
}
.job-title {
  font-size: 14px;
  font-weight: 500;
  color: #333;
  margin-bottom: 4px;
}
.job-source {
  font-size: 13px;
  color: #666;
}
.job-info {
  flex: 1;
  min-width: 0;
}
.candidate-info,
.date-info {
  gap: 6px;
  margin-bottom: 4px;
}
.candidate-icon,
.date-icon {
  font-size: 12px;
  color: #666;
}
.candidate-text,
.date-text {
  font-size: 13px;
  color: #666;
}
.job-status {
  flex-shrink: 0;
}
.job-actions {
  display: flex;
  align-items: center;
  gap: 12px;
  flex-shrink: 0;
}
.toggle-switch {
  position: relative;
}
.toggle-switch input[type="checkbox"] {
  display: none;
}
.toggle-label {
  display: block;
  width: 44px;
  height: 24px;
  background: #ccc;
  border-radius: 12px;
  cursor: pointer;
  position: relative;
  transition: background 0.3s;
}
.toggle-label::after {
  content: '';
  position: absolute;
  top: 2px;
  left: 2px;
  width: 20px;
  height: 20px;
  background: white;
  border-radius: 50%;
  transition: transform 0.3s;
  box-shadow: 0 2px 4px rgba(0,0,0,0.2);
}
.toggle-switch input[type="checkbox"]:checked + .toggle-label {
  background: var(--primary-color);
}
.toggle-switch input[type="checkbox"]:checked + .toggle-label::after {
  transform: translateX(20px);
}
</style>
