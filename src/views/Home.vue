<template>
  <div class="home">
  <snav></snav>
  <hero></hero>
  <short></short>
  <!-- <stats></stats> -->
  <boost></boost>
  <sfoot></sfoot>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import snav from '@/components/navbar.vue'
import hero from '@/components/Home/hero'
import short from '@/components/Home/shorten'
import stats from '@/components/Home/statistics'
import boost from '@/components/Home/boost'
import sfoot from '@/components/footer'

export default {
  name: 'home',
  components: {
    snav, hero, short, stats, boost, sfoot
  }
}
</script>
