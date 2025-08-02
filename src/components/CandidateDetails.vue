// src/components/CandidateDetails.vue
<template>
  <div class="candidate-details">
    <div class="top-row">
      <!-- <img src="/src/assets/avatar.png" alt="Avatar" class="avatar" />
      <div class="info">
        <h2>William Sample</h2>
        <p class="title">Senior Product Manager</p>
        <p class="location">United States • Dallas</p>
        <div class="contact-links">
          <img v-for="icon in icons" :src="icon.src" :alt="icon.alt" :key="icon.alt" class="icon" />
        </div>
      </div> -->
      <div class="contact-info">
        <div class="left-section">
            <div class="contact-item">
                <svg class="contact-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 4.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/>
                </svg>
                <a href="mailto:williamsample@gmail.com" class="contact-text">williamsample@gmail.com</a>
            </div>
            <div class="contact-item">
                <svg class="contact-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"/>
                </svg>
                <span class="phone-text">+91 9021232326</span>
            </div>
        </div>
        <div class="right-section">
            <div class="user-info">
                <svg class="user-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"/>
                </svg>
                <span class="user-name">Phyllis Yang</span>
            </div>
            <div class="timestamp-info">
                <svg class="clock-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"/>
                </svg>
                <span class="timestamp">Jul 14, 2023, 4:04 pm</span>
            </div>
        </div>
    </div>
    </div>
    <table class="details-table">
        <tbody>
        <tr>
            <td class="field-label">Current Organization</td>
            <td class="field-value">World Bank Group</td>
            <td class="field-label-right">Summary</td>
            <td class="field-value-right">Current Organization</td>
        </tr>
        <tr>
            <td class="field-label">Skills</td>
            <td class="field-value">HTML, CSS, Javascript</td>
            <td class="field-label-right">Current Employment Status</td>
            <td class="field-value-right">Employed</td>
        </tr>
        <tr>
            <td class="field-label">Available From</td>
            <td class="field-value">Jul, 14, 2023</td>
            <td class="field-label-right">Date of Birth</td>
            <td class="field-value-right">15 June 1993</td>
        </tr>
        <tr>
            <td class="field-label">Current Salary</td>
            <td class="field-value">$6000</td>
            <td class="field-label-right">Relevant Experience</td>
            <td class="field-value-right">7 Years</td>
        </tr>
        <tr>
            <td class="field-label">Notice Period</td>
            <td class="field-value">90 Days</td>
            <td class="field-label-right">Salary Expectation</td>
            <td class="field-value-right">$9000</td>
        </tr>
        <tr>
            <td class="field-label">Full Address</td>
            <td class="field-value">9400 Ashton Rd, Philadelphia...</td>
            <td class="field-label-right">Status</td>
            <td class="field-value-right">Submitted to Client</td>
        </tr>
        <tr>
            <td class="field-label">Resume</td>
            <td class="field-value">Resume</td>
            <td class="field-label-right">Salary Type</td>
            <td class="field-value-right">Annual</td>
        </tr>
        <tr>
            <td class="field-label">Total Experience</td>
            <td class="field-value">5 Years</td>
            <td class="field-label-right">Language Skills</td>
            <td class="field-value-right">English(Elementary proficiency)</td>
        </tr>
        </tbody>
    </table>
  </div>
</template>

<script>
import '@/assets/styles/candidate-details.scss';
export default {
  name: 'CandidateDetails',
  data() {
    return {
      icons: [
        { src: '/src/assets/icons/linkedin.png', alt: 'LinkedIn' },
        { src: '/src/assets/icons/twitter.png', alt: 'Twitter' },
        { src: '/src/assets/icons/facebook.png', alt: 'Facebook' },
        { src: '/src/assets/icons/github.png', alt: 'GitHub' },
        { src: '/src/assets/icons/link.png', alt: 'Website' }
      ]
    }
  }
}
</script>
