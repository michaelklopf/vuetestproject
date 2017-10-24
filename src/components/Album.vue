<template>
  <div class="fl w-50 w-25-m w-20-l pa2">
    <a v-bind:href="linkText" class="db link dim tc">
      <img
        v-bind:src="pictureLink"
        v-bind:alt="pictureAltText"
        class="w-100 db outline black-10"
      />
      <dl class="mt2 f6 lh-copy">
        <dt class="clip">Title</dt>
        <dd class="ml0 black truncate w-100">{{ album.title }}</dd>
        <dt class="clip">Artist</dt>
        <dd class="ml0 gray truncate w-100">{{ album.artist }}</dd>
      </dl>
    </a>
  </div>
</template>

<script>
export default {
  props: {
    album: {
      type: Object,
      required: true,
    },
  },
  computed: {
    pictureAltText() {
      return `${this.album.artist} ${this.album.title} Album Cover`;
    },
    linkText() {
      return `https://www.last.fm/music/${this.album.artist}`;
    },
    pictureLink() {
      return `/static/${this.album.picture}`;
    },
  },
};
</script>

<style>
.outline {
    outline: 1px solid;
}

.db {
    display: block;
}

.fl {
    float: left;
    _display: inline;
}

.fw4 {
    font-weight: 400;
}

.lh-copy {
    line-height: 1.5;
}

.link {
    text-decoration: none;
    transition: color .15s ease-in;
}

.link:link, .link:visited {
    transition: color .15s ease-in;
}

.link:hover {
    transition: color .15s ease-in;
}

.link:active {
    transition: color .15s ease-in;
}

.link:focus {
    transition: color .15s ease-in;
    outline: 1px dotted currentColor;
}

.w-50 {
    width: 50%;
}

.w-100 {
    width: 100%;
}

.black-10 {
    color: rgba(0, 0, 0, .1);
}

.black {
    color: #000;
}

.gray {
    color: #777;
}

.pa3 {
    padding: 1rem;
}

.ml0 {
    margin-left: 0;
}

.mt2 {
    margin-top: .5rem;
}

.mv0 {
    margin-top: 0;
    margin-bottom: 0;
}

.tc {
    text-align: center;
}

.ttu {
    text-transform: uppercase;
}

.f3 {
    font-size: 1.5rem;
}

.f6 {
    font-size: .875rem;
}

.truncate {
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
}

.clip {
    position: fixed !important;
    _position: absolute !important;
    clip: rect(1px 1px 1px 1px);
    clip: rect(1px, 1px, 1px, 1px);
}

.dim {
    opacity: 1;
    transition: opacity .15s ease-in;
}

.dim:hover, .dim:focus {
    opacity: .5;
    transition: opacity .15s ease-in;
}

.dim:active {
    opacity: .8;
    transition: opacity .15s ease-out;
}

@media screen and (min-width: 30em) and (max-width: 60em) {
    .w-25-m {
        width: 25%;
    }
}

@media screen and (min-width: 60em) {
    .w-20-l {
        width: 20%;
    }
}
</style>
