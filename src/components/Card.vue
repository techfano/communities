<template>
  <div>
    <div class="card">
        <div class="content">
            <div class="media">
              <div v-if="type==='video'">
                <iframe :src="`https://www.youtube.com/embed/${value}`"
                  frameborder="0"
                  allow="encrypted-media">
                </iframe>
              </div>
              <div v-if="type==='image'">
                <img :src="`${value}`" alt="foto">
              </div>
            </div>
            <div class="description">
              <h1>{{title}}</h1>
              <p v-html="description"></p>
            </div>
        </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Card',
  props: {
    id: String,
    type: String,
    value: String,
    title: String,
    description: String,
  },
};
</script>

<style lang="scss">
  .card{
    width: 600px;
    & .content{
      & .description{
        & img{
          width: 100%;
        }
      }
    }
  }
</style>



