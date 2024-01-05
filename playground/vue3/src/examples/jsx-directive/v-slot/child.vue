<script setup lang="tsx">
const slots = defineSlots<{
  default: () => any
  bottom: (props: { foo: 1 }) => any
}>()

defineRender(() => (
  <span>
    <slots.default />
    <slots.bottom {...{ foo: 1 }} />
  </span>
))
</script>
