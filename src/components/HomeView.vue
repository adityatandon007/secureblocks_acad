<template>
  <div>
    <div class="mdl-grid">
      <div class="mdl-cell mdl-cell--3-col mdl-cell mdl-cell--1-col-tablet mdl-cell--hide-phone"></div>
      <div class="mdl-cell mdl-cell--6-col mdl-cell--4-col-phone">
        <div v-for="video in this.videos">
          <div class="mdl-card mdl-shadow--2dp wide-card">
            <div class="mdl-card__title">
              <h2 class="mdl-card__title-text">{{ video.comment }}</h2>
            </div>
            <div class="mdl-card__supporting-text">
              {{ video.desc }}
            </div>
            <div class="mdl-card__actions mdl-card--border">
              <a class="mdl-button mdl-button--colored mdl-js-button mdl-js-ripple-effect" @click="displayDetails(video.id)">
                Get Started
              </a>
              <div></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
  import data from '../data'
  export default {
    methods: {
      displayDetails (id) {
        this.$router.push({name: 'detail', params: { id: id }})
      }
    },
    data () {
      return {
        'videos': data.videos
      }
    }
  }
</script>
<style scoped>
  .list {
    width: 100%;
    padding: 0;
  }
  .wide-card {
    width: 100%;
    min-height: 150px;
    margin-bottom: 1rem;
  }
</style>