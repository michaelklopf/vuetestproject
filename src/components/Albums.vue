<template>
  <div class="cf pa2">
    <Album
      v-for="album in albums"
      :key="album.id"
      :album="album"
    />
  </div>
</template>

<script>
import Album from './Album';

export default {
  name: 'Albums',
  data() {
    return {
      albums: [
        {
          id: 1,
          title: 'Nevermind',
          artist: 'Nirvana',
          picture: 'nevermind.jpg',
        },
        {
          id: 2,
          title: 'To be everywhere is to be nowhere',
          artist: 'Thrice',
          picture: 'tbeitbn.jpg',
        },
        {
          id: 3,
          title: 'The Colour and the Shape',
          artist: 'Foo Fighters',
          picture: 'tcats.png',
        },
        {
          id: 4,
          title: 'Diamond Eyes',
          artist: 'Deftones',
          picture: 'diamond eyes.jpg',
        },
      ],
    };
  },
  components: {
    Album,
  },
};
</script>

<style>
.cf:before, .cf:after {
    content: " ";
    display: table;
}

.cf:after {
    clear: both;
}

.cf {
    *zoom: 1;
}

.pa2 {
    padding: .5rem;
}
</style>
