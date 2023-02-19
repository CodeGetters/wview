<template>
  <div class="w-switch">
    <div @click="toggle" :class="{ checked }" class="switch-core">
      <div class="switch-button"></div>
    </div>
  </div>
</template>

<script lang="ts">
import { switchProps } from './type'
import { defineComponent, ref } from 'vue'
import '@/styles/components/switch.scss'

export default defineComponent({
  name: 'w-switch',
  props: switchProps,
  setup (props) {
    const checked = ref(false)
    const toggle = () => {
      checked.value = !checked.value
    }
    return { toggle, checked }
  }
})
</script>

<style lang="scss" scoped></style>
