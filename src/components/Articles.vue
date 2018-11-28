<template>
  <div class="article">
    <h1>{{ title }}</h1>
    <div class="row">
        <div class="six columns">
            <div v-for="article in articles" :key="article.id" class="card">
            <div class="content">
                <div class="media">
                <iframe             
                    :src="`https://www.youtube.com/embed/${article.cover.id}`"
                    frameborder="0"
                    allow="encrypted-media">
                </iframe>
                </div>
                <div class="description">
                <h1>{{article.title}}</h1>
                <p>{{article.description}}</p>
                </div>
            </div>
            </div>
        </div>
     </div>
  </div>
</template>

<script>

  import source from '@/data.json';  
    console.log(source);
  export default {
    name: 'Articles',
        props: {
        title: String,
    },
    data () {
        return {
           articles: source.articles
        }
    }
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<!--style scoped lang="scss">
</style-->
