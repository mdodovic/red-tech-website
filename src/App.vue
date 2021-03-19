<template>
  <main>
    <section class="section">
      <div class="container">
        <figure class="image logo-size center">
          <img src="./assets/images/logo.svg" alt="Red!Tech logo">
        </figure>
        <h1 class="title center has-text-centered">Computer Science explained!</h1>
      </div>
    </section>
    <section class="section">
      <div class="container">
        <figure class="image center">
          <img src="./assets/images/poster.png" alt="IT Isn't Rocket Science lecture curriculum">
        </figure>
      </div>
    </section>
    <div class="clipped-background">
      <section class="section">
          <div class="container mt-6">
            <h2 class="title has-text-centered mb-6">Our team</h2>
            <div class="columns is-8 is-centered mt-6 is-multiline">
              <div class="column is-one-third" v-for="person in persons" :key="person.name">
                <Card :person="person"></Card>
              </div>
            </div>
          </div>
      </section>
      <footer class="footer transparent">
        <div class="content has-text-centered">
          <p class="has-text-dark">
            by <a href="https://jelenkovic.xyz" class="has-text-dark"><strong>Andrija Jelenkovic</strong></a>. Copyright © 2021. All Rights Reserved.
          </p>
        </div>
      </footer>
    </div>
  </main>
</template>

<script>
import Card from './components/Card.vue';

export default {
  name: "App",
  components: {
    Card,
  },
  data() {
    return {
      persons: [{
        name: "Andrija Jelenkovic",
        position: "Software Engineer @ Logeecom",
        image: "img_3916.png",
        linkedin: "https://www.linkedin.com/in/andrija-jelenkovic-5740b4194/",
        }, {
        name: "Djordje Dimitrijevic",
        position: "Software Engineer @ Algotech",
        image: "djordje.jpg",
        linkedin: "https://www.linkedin.com/in/djordje-dimitrijevic14/",
        }, {
        name: "Matija Dodovic",
        position: "2x Awardee for the best student on Module Computer Engineering and Information theory",
        image: "doda.jpg",
        linkedin: "https://www.linkedin.com/in/matija-dodovic-b8b4b8113/",
        }, {
        name: "Mladen Basic",
        position: "Software Engineer Intern @ Microsoft",
        image: "mladen.png",
        linkedin: "https://www.linkedin.com/in/basic-mladen/"
        }, {
        name: "Damjan Denic",
        position: "Software Engineer Intern @ Microsoft",
        image: "damjan.jpg",
        linkedin: "https://www.linkedin.com/in/damjan-deni%C4%87-5212b3166/"
        }, {
        name: "Milan Cupac",
        position: "Top 3% of students at the Techincal University of Munich",
        image: "milan.jpg",
        linkedin: "https://www.linkedin.com/in/milan-cupac/"
        },
      ]}
  }
};
</script>

<style lang="scss">

@import './assets/scss/main.scss';

.logo-size {
  max-width: 50%;
}

.center {
  margin: 0 auto;
}

.clipped-background {
  background:
    linear-gradient(322deg, 
      $red, rgba($red, 0) 70%),
    linear-gradient(178deg,
      $mandarine, rgba($mandarine, 0) 70%),
    linear-gradient(24deg,
      $rose, rgba($rose, 0) 35%);
  
}

.transparent {
  background: transparent;
}

</style>
