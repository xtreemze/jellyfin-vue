<template>
  <v-btn
    class="align-self-center ma-1"
    v-bind="$props"
    icon
    size="small"
    variant="elevated">
    <slot name="icon" />

    <v-tooltip v-if="$slots.tooltip" location="bottom">
      <slot name="tooltip" />
    </v-tooltip>
  </v-btn>
</template>

<script setup lang="ts">
withDefaults(
  defineProps<{
    color?: string;
    disabled?: boolean;
  }>(),
  { color: '', disabled: false }
);
</script>
