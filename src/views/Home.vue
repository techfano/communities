<template>
  <div class="home">
    <Header />
    <Communities title="Comunidades"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue';
import Communities from '@/components/Communities.vue';

export default {
  name: 'home',
  components: {
    Communities,
    Header
  },
};
</script>
