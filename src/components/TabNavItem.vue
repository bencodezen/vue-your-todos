<script>
import { computed, useCssModule } from 'vue'

export default {
  props: {
    isActive: {
      type: Boolean,
      default: false
    },
    listName: {
      type: String,
      required: true
    },
    listLength: {
      type: Number,
      required: true
    }
  },
  setup(props, ctx) {
    const style = useCssModule()

    const emitTabValue = () => {
      ctx.emit('emit-tab-value', {
        value: props.listName
      })
    }

    const tabNavItemClassNames = computed(() => {
      if (props.isActive) {
        return [style.tabNavItem, style.isActive]
      } else {
        return style.tabNavItem
      }
    })

    return {
      emitTabValue,
      tabNavItemClassNames
    }
  }
}
</script>

<template>
  <li :class="tabNavItemClassNames">
    <button :class="$style.tabNavItemButton" @click="emitTabValue">
      {{ listName }} ({{ listLength }})
    </button>
  </li>
</template>

<style module>
.tab-nav-item {
  padding-bottom: 2px;
}

.tab-nav-item:hover .tab-button {
  color: #0728bf;
}

.tab-nav-item.is-active {
  border-bottom: 3px solid #0631f8;
}

.tab-nav-item.is-active .tab-button {
  color: #2d2d2d;
}

.tab-nav-item-button {
  border: 0;
  background-color: transparent;
  color: #6b6b6b;
  letter-spacing: 1px;
  font-weight: bold;
  font-family: 'Source Sans Pro';
  padding: 0;
  font-size: 1rem;
}

.tab-nav-item-button:hover {
  cursor: pointer;
}
</style>
