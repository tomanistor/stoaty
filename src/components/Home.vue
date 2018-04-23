<template>
  <div>
    <v-layout row wrap class="mb-2">
      <v-flex xs12 sm6 class="text-xs-center text-sm-right">
        <v-btn large router to="/meetups" class="info">Explore Meetups</v-btn>
      </v-flex>
      <v-flex xs12 sm6 class="text-xs-center text-sm-left">
        <v-btn large router to="/meetup/new" class="info">Organize Meetup</v-btn>
      </v-flex>
    </v-layout>

    <v-layout row wrap>
      <v-flex xs12>
        <v-carousel>
          <v-carousel-item v-for="meetup in meetups" :src="meetup.src" :key="meetup.id">
            <div class="title">
              {{ meetup.title }}
            </div>
          </v-carousel-item>
        </v-carousel>
      </v-flex>
    </v-layout>

    <v-layout row wrap class="mt-2">
      <v-flex xs12 class="text-xs-center">
        <p>
          Join a meetup!
        </p>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        meetups: [
          {
            title: 'Home & Away',
            src: 'https://s3-media1.fl.yelpcdn.com/bphoto/Wf-TWNOEp97zmORNQdxOQw/o.jpg',
            id: '94382kjnsdf'
          },
          {
            title: 'Brew Project',
            src: 'https://res-4.cloudinary.com/dostuff-media/image/upload//w_1200,q_75,c_limit,f_auto/v1480058045/page-image-8159-f37e9b85-a20d-4d19-834e-7b5a6d626b64.jpg',
            id: '434382knsoo'
          }
        ]
      }
    }
  }
</script>

<style scoped lang="scss">
  .title {
    position: absolute;
    left: 50%;
    bottom: 50px;
    transform: translate(-50%);
    background-color: rgba(0, 0, 0, .5);
    color: #FFF;
    font-size: 2em;
    padding: 20px;
    text-align: center;
  }
</style>
