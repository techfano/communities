<template>
  <div class="home">
    <Header />
    <Articles title="Articulos"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue';
import Articles from '@/components/Articles.vue';

export default {
  name: 'home',
  components: {
    Articles,
    Header
  },
};
</script>
