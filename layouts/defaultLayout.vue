<template>
  <div>
    <PageHeader></PageHeader>
    <nuxt></nuxt>
    <PageFooter></PageFooter>
  </div>
</template>
<script>
import PageHeader from '@/components/page/PageHeader.vue'
import PageFooter from '@/components/page/PageFooter.vue'

export default {
  components: {
    PageHeader,
    PageFooter
  }
}
</script>
