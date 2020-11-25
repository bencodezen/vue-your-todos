<script>
import TabNavItem from './TabNavItem.vue'

export default {
  props: {
    currentView: {
      type: String,
      default: 'All',
      validator: value => {
        return ['All', 'Current', 'Completed'].indexOf(value) !== -1
      }
    },
    taskListOverview: {
      type: Array,
      required: true
    }
  },
  components: {
    TabNavItem
  },
  setup(props, ctx) {
    const updateCurrentView = payload => {
      ctx.emit('update-current-view', payload.value)
    }

    return {
      updateCurrentView
    }
  }
}
</script>

<template>
  <nav>
    <ul :class="$style['tab-nav-wrapper']">
      <TabNavItem
        v-for="taskList in taskListOverview"
        :key="`task-list-${taskList.name}`"
        :listLength="taskList.length"
        :listName="taskList.name"
        :isActive="currentView === taskList.name"
        @emit-tab-value="updateCurrentView"
      />
    </ul>
  </nav>
</template>

<style module>
.tab-nav-wrapper {
  display: flex;
  column-gap: 30px;
  list-style: none;
  margin: 45px 0 20px;
  padding: 0;
}
</style>
