<template>
  <div class="candidate-profile-header">
    <!-- Navigation Bar -->
    <div class="nav-bar">
      <div class="nav-left">
        <span class="nav-link">Candidates</span>
        <span class="nav-separator">></span>
        <span class="nav-link current">Robert Hardy</span>
        <span class="nav-id">ID - 231</span>
      </div>
      <div class="nav-right">
        <button class="nav-btn">Request Profile Update</button>
        <button class="nav-btn">Previous</button>
        <button class="nav-btn">Next</button>
      </div>
    </div>

    <!-- Profile Section -->
    <div class="profile-section">
      <div class="profile-left">
        <div class="avatar">
          <svg width="30" height="30" viewBox="0 0 24 24" fill="#28a745">
            <path d="M12 12c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm0 2c-2.67 0-8 1.34-8 4v2h16v-2c0-2.66-5.33-4-8-4z"/>
          </svg>
        </div>
        <div class="profile-info">
          <div class="name-row">
            <h2 class="name">William Sample</h2>
            <div class="social-icons">
              <div class="social-icon twitter">
                <svg width="12" height="12" viewBox="0 0 24 24" fill="white">
                  <path d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z"/>
                </svg>
              </div>
              <div class="social-icon facebook">
                <svg width="12" height="12" viewBox="0 0 24 24" fill="white">
                  <path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/>
                </svg>
              </div>
              <div class="social-icon linkedin">
                <svg width="12" height="12" viewBox="0 0 24 24" fill="white">
                  <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
                </svg>
              </div>
              <div class="social-icon github">
                <svg width="12" height="12" viewBox="0 0 24 24" fill="white">
                  <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
                </svg>
              </div>
              <div class="social-icon email">
                <svg width="12" height="12" viewBox="0 0 24 24" fill="white">
                  <path d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/>
                </svg>
              </div>
            </div>
          </div>
          <div class="details-row">
            <span class="title">Senior Product Manager</span>
            <span class="location">United States</span>
            <span class="city">Dallas</span>
          </div>
        </div>
      </div>
      <div class="profile-right">
        <div class="action-buttons">
          <button class="btn contact-linked">Contact Linked</button>
          <button class="btn icon-btn star">★</button>
          <button class="btn icon-btn notification">🔔</button>
          <button class="btn icon-btn edit">✏️</button>
          <button class="btn icon-btn more">⋯</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CandidateProfileHeader',
  data() {
    return {
      candidate: {
        id: 231,
        name: 'William Sample',
        title: 'Senior Product Manager',
        location: 'United States',
        city: 'Dallas',
        avatar: 'https://via.placeholder.com/60x60/4CAF50/white?text=WS'
      }
    }
  },
  methods: {
    requestProfileUpdate() {
      console.log('Request profile update clicked');
    },
    goToPrevious() {
      console.log('Previous candidate');
    },
    goToNext() {
      console.log('Next candidate');
    },
    contactLinked() {
      console.log('Contact linked clicked');
    },
    toggleStar() {
      console.log('Star toggled');
    },
    toggleNotification() {
      console.log('Notification toggled');
    },
    editProfile() {
      console.log('Edit profile clicked');
    },
    showMore() {
      console.log('More options clicked');
    }
  }
}
</script>

<style scoped>
.candidate-profile-header {
  background: white;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
}

.nav-bar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 12px 20px;
  border-bottom: 1px solid #e0e0e0;
  background: #f8f9fa;
}

.nav-left {
  display: flex;
  align-items: center;
  gap: 8px;
}

.nav-link {
  color: #007bff;
  cursor: pointer;
  font-size: 14px;
}

.nav-link.current {
  color: #333;
  font-weight: 500;
}

.nav-separator {
  color: #666;
  margin: 0 4px;
}

.nav-id {
  color: #666;
  font-size: 14px;
  margin-left: 8px;
}

.nav-right {
  display: flex;
  gap: 8px;
}

.nav-btn {
  padding: 6px 12px;
  border: 1px solid #ddd;
  background: white;
  border-radius: 4px;
  cursor: pointer;
  font-size: 13px;
  color: #333;
}

.nav-btn:hover {
  background: #f5f5f5;
}

.profile-section {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
}

.profile-left {
  display: flex;
  align-items: center;
  gap: 16px;
}

.avatar {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  overflow: hidden;
  background: #d4edda;
  display: flex;
  align-items: center;
  justify-content: center;
}

.avatar img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.profile-info {
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.name-row {
  display: flex;
  align-items: center;
  gap: 12px;
}

.name {
  margin: 0;
  font-size: 20px;
  font-weight: 600;
  color: #333;
}

.social-icons {
  display: flex;
  gap: 6px;
}

.social-icon {
  width: 20px;
  height: 20px;
  border-radius: 50%;
  cursor: pointer;
}

.social-icon.twitter {
  background: #1DA1F2;
}

.social-icon.facebook {
  background: #4267B2;
}

.social-icon.linkedin {
  background: #0077B5;
}

.social-icon.github {
  background: #333;
}

.social-icon.email {
  background: #EA4335;
}

.details-row {
  display: flex;
  gap: 16px;
  color: #666;
  font-size: 14px;
}

.title {
  font-weight: 500;
}

.action-buttons {
  display: flex;
  gap: 8px;
  align-items: center;
}

.btn {
  padding: 8px 16px;
  border: 1px solid #ddd;
  border-radius: 4px;
  cursor: pointer;
  font-size: 13px;
  background: white;
}

.btn:hover {
  background: #f5f5f5;
}

.contact-linked {
  background: #ff6b6b !important;
  color: white !important;
  border-color: #ff6b6b !important;
}

.contact-linked:hover {
  background: #ff5252 !important;
}

.icon-btn {
  width: 36px;
  height: 36px;
  padding: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 16px;
}

.star {
  color: #ffc107;
}

.notification {
  color: #666;
}

.edit {
  color: #666;
}

.more {
  color: #666;
  font-weight: bold;
}
</style>