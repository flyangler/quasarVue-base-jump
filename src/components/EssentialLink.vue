<template>
  <q-item
    clickable
    class="text-grey-4"
    :to="to"
  >
    <q-item-section
      v-if="icon"
      avatar
      size="md"
    >
      <q-icon :name="icon" />
    </q-item-section>

    <q-item-section>
      <q-item-label>{{ title }}</q-item-label>
    </q-item-section>
  </q-item>
</template>

<script>
export default {
  name: 'EssentialLink',
  props: {
    title: {
      type: String,
      required: true
    },
    icon: {
      type: String,
      default: ''
    },
    to: {
      type: String,
      default: '/'
    }
  }
}
</script>
