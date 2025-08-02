<template>
  <nav class="navbar" style="width: 92vw; right: 0; top: 0; left: 84px">
    <div class="navbar-container">
      <!-- Left side - Search -->
      <div class="navbar-left">
        <div class="search-container">
          <div class="search-icon">
            <svg width="16" height="16" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
            </svg>
          </div>
          <input
            type="text"
            placeholder="Search Pipedrive"
            class="search-input"
            v-model="searchQuery"
          />
        </div>
      </div>

      <!-- Center - Logo -->
      <div class="navbar-center">
        <div class="logo-container">
          <div class="logo-icon">
            <span>rc</span>
          </div>
          <span class="logo-text">recruit crm</span>
        </div>
      </div>

      <!-- Right side - Action buttons and user -->
      <div class="navbar-right">
        <!-- Add button -->
        <button class="btn-add">
          <svg width="16" height="16" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4v16m8-8H4" />
          </svg>
        </button>

        <!-- Gift/Calendar button -->
        <button class="btn-icon">
          <svg width="20" height="20" fill="currentColor" viewBox="0 0 24 24">
            <path d="M19 3h-1V1h-2v2H8V1H6v2H5c-1.11 0-1.99.9-1.99 2L3 19c0 1.1.89 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm0 16H5V8h14v11zM7 10h5v5H7z"/>
          </svg>
        </button>

        <!-- Mail button -->
        <button class="btn-icon">
          <svg width="20" height="20" fill="currentColor" viewBox="0 0 24 24">
            <path d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/>
          </svg>
        </button>

        <!-- Notifications button -->
        <button class="btn-icon">
          <svg width="20" height="20" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 17h5l-5-5V9a4 4 0 00-4-4v0a4 4 0 00-4 4v3L2 17h5m6 0v1a2 2 0 01-2 2v0a2 2 0 01-2-2v-1m6 0H9" />
          </svg>
        </button>

        <!-- User profile -->
        <div class="user-profile">
          <div class="user-avatar">
            <span>PY</span>
          </div>
          <div class="user-info">
            <div class="user-name">Phyllis Yang</div>
            <div class="user-company">Silicon Links Inc</div>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'HeaderNavbar',
  data() {
    return {
      searchQuery: ''
    }
  },
  methods: {
    handleSearch() {
      console.log('Searching for:', this.searchQuery);
    },
    handleAdd() {
      console.log('Add button clicked');
    },
    handleCalendar() {
      console.log('Calendar button clicked');
    },
    handleMail() {
      console.log('Mail button clicked');
    },
    handleNotifications() {
      console.log('Notifications button clicked');
    },
    handleUserProfile() {
      console.log('User profile clicked');
    }
  }
}
</script>

<style scoped>
.navbar {
  width: 100%;
  height: 56px;
  background-color: #ffffff;
  border-bottom: 1px solid #e5e7eb;
  box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.1);
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
}

.navbar-container {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 20px;
  max-width: 100%;
}

/* Left Section - Search */
.navbar-left {
  display: flex;
  align-items: center;
  flex: 0 0 auto;
}

.search-container {
  position: relative;
  display: flex;
  align-items: center;
}

.search-icon {
  position: absolute;
  left: 12px;
  color: #9ca3af;
  pointer-events: none;
  z-index: 1;
}

.search-input {
  width: 280px;
  height: 36px;
  padding: 8px 16px 8px 40px;
  border: 1px solid #d1d5db;
  border-radius: 18px;
  background-color: #f9fafb;
  font-size: 14px;
  color: #374151;
  outline: none;
  transition: all 0.2s ease;
}

.search-input::placeholder {
  color: #9ca3af;
}

.search-input:focus {
  border-color: #3b82f6;
  background-color: #ffffff;
  box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.1);
}

/* Center Section - Logo */
.navbar-center {
  display: flex;
  align-items: center;
  justify-content: center;
  flex: 1 1 auto;
}

.logo-container {
  display: flex;
  align-items: center;
  gap: 8px;
}

.logo-icon {
  width: 32px;
  height: 32px;
  background-color: #3b82f6;
  border-radius: 6px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #ffffff;
  font-weight: 700;
  font-size: 12px;
  text-transform: lowercase;
}

.logo-text {
  font-size: 18px;
  font-weight: 600;
  color: #111827;
  letter-spacing: -0.025em;
}

/* Right Section - Actions & User */
.navbar-right {
  display: flex;
  align-items: center;
  gap: 8px;
  flex: 0 0 auto;
}

.btn-add {
  width: 36px;
  height: 36px;
  background-color: #3b82f6;
  border: none;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #ffffff;
  cursor: pointer;
  transition: background-color 0.2s ease;
}

.btn-add:hover {
  background-color: #2563eb;
}

.btn-icon {
  width: 40px;
  height: 40px;
  background-color: transparent;
  border: none;
  border-radius: 6px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #6b7280;
  cursor: pointer;
  transition: all 0.2s ease;
}

.btn-icon:hover {
  background-color: #f3f4f6;
  color: #374151;
}

.user-profile {
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 4px;
  border-radius: 8px;
  cursor: pointer;
  transition: background-color 0.2s ease;
  margin-left: 8px;
}

.user-profile:hover {
  background-color: #f9fafb;
}

.user-avatar {
  width: 40px;
  height: 40px;
  background-color: #10b981;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #ffffff;
  font-weight: 600;
  font-size: 14px;
  text-transform: uppercase;
}

.user-info {
  display: flex;
  flex-direction: column;
  text-align: left;
}

.user-name {
  font-size: 14px;
  font-weight: 600;
  color: #111827;
  line-height: 1.2;
}

.user-company {
  font-size: 12px;
  color: #6b7280;
  line-height: 1.2;
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .search-input {
    width: 200px;
  }
  
  .user-info {
    display: none;
  }
  
  .navbar-container {
    padding: 0 16px;
  }
}

@media (max-width: 640px) {
  .navbar-container {
    padding: 0 12px;
  }
  
  .search-input {
    width: 160px;
  }
  
  .logo-text {
    font-size: 16px;
  }
  
  .navbar-right {
    gap: 4px;
  }
}
</style>