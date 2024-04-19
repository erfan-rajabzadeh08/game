<template>
    <div>
        <error />
    </div>
</template>

<script>
export default {
  components: {
      error: () => import('@/layouts/error')
  },
}
</script>