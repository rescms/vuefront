<template>
  <vf-o-layout class="not-found">
    <vf-m-row align-h="center">
      <vf-m-col lg="7" class="text-center">
        <vf-a-heading :level="1" tag="h6" class="mb-5 font-weight-400">{{$t('elements.common.error.textError')}}</vf-a-heading>
      </vf-m-col>
    </vf-m-row>
  </vf-o-layout>
</template>
<script>
export default {
  created() {
    this.$store.commit('common/breadcrumbs/setLoaded', true);
  }
}
</script>