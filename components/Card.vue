<template>
<div class="card">
  <div class="card-image">
    <figure class="image is-4by3">
      <img :src="image" alt="Placeholder image">
    </figure>
  </div>
  <div class="card-content">
    <div class="media">
      <div class="media-left">
        <figure class="image is-48x48">
          <img src="https://bulma.io/images/placeholders/96x96.png" alt="Placeholder image">
        </figure>
      </div>
      <div class="media-content">
        <p class="title is-4 has-text-red">{{title}}</p>
        <p class="subtitle is-6">@johnsmith</p>
      </div>
    </div>

    <div class="content">
      {{description}}
      <a class="button-alex">@bulmaio</a>.
      <a href="#">#css</a> <a href="#">#responsive</a>
      <br>
      <time datetime="2016-1-1">11:09 PM - 1 Jan 2016</time>
    </div>
  </div>
</div>
</template>

<script>
export default {
    name: 'Card',
    props: {
        title: {
            type: String,
            default: 'Untitled'
        },
        description: {
            type: String,
            default: 'Untitled'
        },
        image: {
            type: String,
            default: 'http://placehold.it/600x40'
        }
    }
}
</script>
<style scoped>
  .title {
    color: red;
  }
</style>



