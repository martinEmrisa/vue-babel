<template>
  <div class="about">
    <img
      src="https://bbu.world/uploads/babelbetweenus/original/1X/d148a656cefb8fec73359e0a16e50fcac57628d3.jpeg"
    />
    <div id="about-text" />
    <h2>Image by Sune Skote, Fornvårdar, 1950</h2>
  </div>
</template>

<script>
export default {
  name: "About",
  data() {
    return {
      abouts: [
        `Babel Between Us is a cartographic visualization of a collaboratively created world, 
          exploring the uncharted waters between collaboration, fiction and ethnography.`,
        `A group of 18 writers collectively improvise a story on an online forum during an extensive amount of time. 
          The resulting fiction is analyzed by a team of ethnographers and presented as an interactive map. 
          This map is then presented back to the group throughout the process. 
          The final map is presented in itself as an entry point for the general public to experience the work.`,
        `The project is currently ongoing. This site lets you read the texts produced by the writers, the ethnographic part will be added eventually. Follow us on <a href="https://twitter.com/babelbetweenus">twitter</a> for recurring updates.`,
        `If you have any questions contact us on <a href="https://bbu.world/">our forum</a>, or at team [at] bbu.world.`,
        `Babel between us is led by Ola Claësson, Jennifer McGeachie, Filip Nyström, Alja Gudžević, Amelia Hassoun, Hugi Ásgeirsson and Jakob Skote. Our ethnographic team is Bojan Mucko, Lea Vene, Jakob Skote and Hugi Asgeirsson with Amelia Hassoun as the senior ethnography and research advisor. Jim Segevid developed the Babel Reader software. Our 18 writers remain anonymous. Babel Between Us is a collaboration with with <a href="https://www.blivande.com/">Blivande</a> and <a href="https://edgeryders.eu/">Edgeryders</a>, and with funding from <a href="https://www.konstnarsnamnden.se/Kulturbryggan/">Kulturbryggan</a>.`
      ]
    };
  },
  mounted() {
    this.abouts.map(about => {
      document.getElementById("about-text").innerHTML +=
        `<p
          style="text-align: left;
          margin-bottom: 40px;
          font-size: 18px;
          line-height: 1.6em;"
        >` +
        about +
        `</p>`;
    });
  }
};
</script>

<style scoped>
.about {
  margin: 20px 0px;
}
img {
  width: 95%;
}
h2 {
  text-align: left;
  white-space: pre-wrap;
  color: #8a8a8a;
  font-weight: 400;
  font-style: italic;
  line-height: 1.3em;
  font-size: 12px;
  text-transform: none;
  text-decoration: none;
  letter-spacing: 0.02em;
}
</style>
