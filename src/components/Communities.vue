<template>
  <div class="container">
    <h1>{{ title }}</h1>
    <div class="row">
        <div class="twelve columns">
            <Card v-for="community in communities" :key="community.id" 
                type=""
                value="community.cover.id"
                v-bind:title="community.name"
                v-bind:description="community.description"
            />
        </div>
     </div>
  </div>
</template>

<script>
//import source from '@/data.json';
import source from '@/comunidades.json';
import Card from '@/components/Card.vue';

console.log(source);
export default {
    name: 'Communities',
        props: {
        title: String,
    },
    components: {
        Card
    },
    data () {
        return {
            communities: source
        }
    }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
    .container{
        width: 1280px;
        position: absolute;
        
    }
</style>
