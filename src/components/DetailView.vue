<template>
  <div class="mdl-grid">
    <div class="mdl-cell mdl-cell--8-col">
      <div class="video">
        <iframe width="100%" height="315" :src="this.videos[$route.params.id].url" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
      </div>
      <div class="info">
        <span>{{ this.videos[$route.params.id].info }}</span>
      </div>
    </div>
    <div class="mdl-cell mdl-cell--4-col mdl-cell--8-col-tablet">
      <div class="comment">
        <span>{{ this.videos[$route.params.id].comment }}</span>
      </div>
      <div class="description">
          <span>{{ this.videos[$route.params.id].desc }}</span>
      </div>
    </div>
  </div>
</template>
<script>
import data from '../data'
export default {
  data () {
    return {
      'videos': data.videos
    }
  }
}
</script>
<style scoped>
  .video > img {
    color: #fff;
    width:100%;
  }
  .info {
    padding: 5px;
    color: #2196f3;
    margin: 5px;
  }
  .comment {
    padding: 10px;
    color: #2196f3;
    font-size: larger;
  }
  .actions {
    text-align: center;
  }
</style>