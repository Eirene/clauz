<template>
  <div class="inline-flex items-center text-sm font-medium px-2.5 py-0.5 rounded"
    :class="`bg-${color}-100 text-${color}-800`">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "AppBadge",
  props: {
    color: {
      type: String,
      default: 'blue',
    }
  }
}
</script>
