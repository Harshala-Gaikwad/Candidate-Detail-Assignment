<!-- src/views/CandidateProfile.vue -->
<template>
  <div class="candidate-profile-layout">
    <div class="candidate-main">
      <CandidateProfileHeader />
      <CandidateDetails />
      <AssignedJobsSection />
    </div>
    <div class="candidate-right-panel">
      <ActivityNotes />
      <ActivityNotes />
      <ActivityNotes />
    </div>
  </div>
</template>

<script>
import CandidateDetails from "@/components/CandidateDetails.vue";
import CandidateProfileHeader from "@/components/CandidateProfileHeader.vue";
import AssignedJobsSection from "@/components/AssignedJobsSection.vue";
import Tabs from "@/components/Tabs.vue";
import ActivityNotes from "@/components/ActivityNotes.vue";

export default {
  name: "CandidateProfile",
  components: {
    CandidateDetails,
    AssignedJobsSection,
    Tabs,
    ActivityNotes,
    CandidateProfileHeader,
  },
};
</script>

<style scoped>
.candidate-profile-layout {
  display: flex;
  gap: 2rem;
  margin-top: 2rem;
  margin-left: 4rem;
}
.candidate-main {
  flex: 2;
  min-width: 0;
}
.candidate-right-panel {
  flex: 1;
  min-width: 320px;
  max-width: 400px;
  background: #fff;
  border-radius: 8px;
  box-shadow: 0 1px 4px #0001;
  padding: 1rem;
  margin-top: 1rem;
  height: fit-content;
}
@media (max-width: 1024px) {
  .candidate-profile-layout {
    flex-direction: column;
  }
  .candidate-right-panel {
    max-width: 100%;
    margin-top: 2rem;
  }
}
</style>
