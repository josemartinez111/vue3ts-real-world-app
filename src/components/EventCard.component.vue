<!-- EventCardComponent.vue -->

// 🌀🌀💻 SCRIPT 💻🌀🌀
<!-- 🎵🎵🔲🔲◾️◾️◾️◾️◾️◾️◾️ -->
<script lang="ts">
import { defineComponent, PropType } from 'vue'
import type { EventType } from "@/types/Event.type"
// ⚫️⚫️☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰
export default defineComponent({
  name: 'EventCardComponent',
  props: {
    event: {
      type: Object as PropType<EventType>,
      required: true
    }
  }
})
</script>
<!-- 🌀🌀💻================================================= -->

// 🌀🌀💻 HTML 💻🌀🌀
<!-- 🎵🎵🔲🔲◾️◾️◾️◾️◾️◾️◾️ -->
<template>
  <!-- 🎵🎵🔲🔲◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️ -->
  <router-link class="event-link"
               :to="{ name: 'EventDetailsPage',
               params: { id: event.id } }"
  >
    <div class="eventCardContainer">
    
      <span>
        <b>@ {{ event.time }} on {{ event.date }}</b>
      </span>
    
      <h4>
        <b>{{ event.title }}</b>
      </h4>
    </div>
  </router-link>
  <!-- 🎵🎵🔲🔲◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️ -->
</template>
<!-- 🌀🌀💻================================================ -->

// 🌀🌀💻 STYLES 💻🌀🌀
<!-- 🎵🎵🔲🔲◾️◾️◾️◾️◾️◾️◾️ -->
<style scoped lang="scss">
.eventCardContainer {
  padding: 20px;
  width: 250px;
  cursor: pointer;
  border: 1px solid #39495c;
  margin-bottom: 18px;
  
  &:hover {
    transform: scale(1.01);
    box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2);
  }
  
  /// 🎵🔲🔲️◾️◾️◾️◾️◾  (|  nested styles  |)  ◾️◾️◾️◾️◾🔲🔲🎵
  .event-link {
    color: #2c3e50;
    text-decoration: none;
  }
}

/// - END OF: eventCardContainer
</style>
<!-- 🌀🌀💻================================================ -->

