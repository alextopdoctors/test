<template>
  <div class="container is-fluid">
      <header-main/>
      <div class="columns is-medium">
        <div class="column is-narrow">
          <div class="box" style="width: 200px;">
            <p class="title is-5">Narrow column</p>
            <p class="subtitle">This column is only 200px wide.</p>
          </div>
        </div>
        <div class="column">
          <div class="box">
            <p class="title is-5">Flexible column</p>
            <p class="subtitle">This column will take up the remaining space available.</p>
          </div>
        </div>
      </div>
      <div class="column">
          <div class="columns is-11 is-multiline">
            <div v-for="card in cardItems" :key="card.id" class="column">
              <card :title="card.title" :image="card.img" :description="card.description"/>
              <a class="button is-medium is-fullwidth">Medium</a>
            </div>
          </div>
      </div>
  </div>
</template>

<script>
import HeaderMain from "~/components/Header.vue";
import Card from "~/components/Card.vue";

export default {
  name: "Main",
  components: {
    HeaderMain,
    Card
  },
  data() {
    return {
      cardItems: [
        {
          id: 1,
          title: "PORCHE GT",
          img: "/img/2017-porsche-panamera-.jpg",
          description:
            "Textos simulados: su función como texto de relleno o como herramienta para comparar el efecto visual de diferentes tipos de letraLos textos simulados son aquellos textos que, en ausencia de un texto definitivo, sirven como sustituto de futuros contenidos en la producción de maquetas para publicaciones o sitios web. También son llamados textos dummy, ficticios o de relleno. A parte de ser utilzados dentro del sector de la imprenta y del grafismo, algunos compositores de canciones también utilizan textos simulados al componer melodías, cantando estos textos antes de escribir las letras de la canción. Ya en el siglo XVI, los tipógrafos solían usar textos simulados. "
        },
        {
          id: 2,
          title: "PANAMERA",
          description:
            "Description, alex asdasd asdasd a dasderom fkemfw  Description, alex asdasd asdasd a dasderom fkemfw "
        },
        {
          id: 3,
          img: "/img/2017-porsche-panamera-.jpg",
          title: "PORCHE 911",
          description: "Description, alex asdasd asdasd a dasderom fkemfw"
        }
      ]
    };
  }
};
</script>

<style>
</style>

