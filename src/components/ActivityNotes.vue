<template>
  <div class="note-card">
    <div class="note-card__tags">
      <span class="tag note">Note</span>
      <span class="tag todo">To Do</span>
    </div>

    <p class="note-card__content">
      {{ content }}
    </p>

    <a href="#" class="note-card__link">
      {{ associationText }}
    </a>

    <div class="note-card__footer">
      <span class="note-card__footer-item">
        <svg class="icon" viewBox="0 0 24 24">
          <path d="M5.121 17.804A9.968 9.968 0 0112 15c2.5 0 4.77.92 6.879 2.448M15 11a3 3 0 11-6 0 3 3 0 016 0z"/>
        </svg>
        {{ author }}
      </span>
      <span class="note-card__footer-item">
        <svg class="icon" viewBox="0 0 24 24">
          <path d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"/>
        </svg>
        {{ timestamp }}
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ActivityNotes',
  props: {
    content: {
      type: String,
      default: 'Lorem dolore sit et aute cupidatat eu Lorem tempor proident consequat. In dolore mollit laborum ex cillum laboris occaecat ipsum Lorem cupidatat.'
    },
    associationText: {
      type: String,
      default: '1 Association(s)'
    },
    author: {
      type: String,
      default: 'John Doe'
    },
    timestamp: {
      type: String,
      default: 'Jul 12, 2023, 11:54 am'
    }
  }
}
</script>

<style scoped>
.note-card {
  background-color: #ffffff;
  border: 1px solid #e5e7eb;
  border-radius: 8px;
  padding: 16px;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.05);
  font-family: system-ui, sans-serif;
  text-align: left;
}

.note-card__tags {
  display: flex;
  gap: 8px;
  margin-bottom: 8px;
}

.tag {
  font-size: 12px;
  font-weight: 600;
  padding: 4px 8px;
  border-radius: 4px;
  display: inline-block;
}

.tag.note {
  background-color: #e0f2fe;
  color: #2563eb;
}

.tag.todo {
  background-color: #f3f4f6;
  color: #4b5563;
}

.note-card__content {
  font-size: 14px;
  color: #374151;
  line-height: 1.5;
  margin-bottom: 12px;
  text-align: left;
}

.note-card__link {
  font-size: 14px;
  font-weight: 500;
  color: #2563eb;
  text-decoration: none;
  display: inline-block;
  margin-bottom: 8px;
}

.note-card__link:hover {
  text-decoration: underline;
}

.note-card__footer {
  display: flex;
  justify-content: space-between;
  font-size: 12px;
  color: #6b7280;
}

.note-card__footer-item {
  display: flex;
  align-items: center;
  gap: 4px;
}

.icon {
  width: 16px;
  height: 16px;
  stroke: #9ca3af;
  fill: none;
  stroke-width: 2;
}
</style>
