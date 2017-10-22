<template>
  <div class="mw9 center ph3-ns">
    <div class="cf ph2-ns">
      <div class="fl w-100 w-third-ns pa2">
        <div class="outline bg-red pv4"></div>
      </div>
      <div class="fl w-100 w-third-ns pa2">
        <div class="outline bg-blue pv4"></div>
      </div>
      <div class="fl w-100 w-third-ns pa2">
        <div class="outline bg-green pv4"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Albums',
  data() {
    return {
      albums: [
        {
          title: 'Nevermind',
          artist: 'Nirvana',
        },
        {
          title: 'To be everywhere is to be nowhere',
          artist: 'Thrice',
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
