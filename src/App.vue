<template>
  <div id="app">
    <component :is="layout">
      <router-view/>
    </component>
  </div>
</template>
<script>

    import EmptyLayout from './layotes/EmptyLayout';
    import MainLayout from './layotes/MainLayout';

    export default {
        computed: {
            layout() {
                return (this.$route.meta.layout || 'empty') + '-layout';
            }
        },
        components: {
            EmptyLayout,
            MainLayout
        }
    }
</script>
<style lang="scss">
  @import "~materialize-css/dist/css/materialize.css";
  @import "assets/index.css";
</style>
