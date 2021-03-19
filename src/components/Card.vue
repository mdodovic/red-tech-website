<template>
  <div class="glass">
    <div class="card-content">
      <div class="media columns is-mobile">
        <div class="column is-one-third-mobile is-two-thirds-tablet is-one-third-desktop is-centered">
          <figure class="image is-1by1">
            <img class="is-rounded clip has-border" :src="require(`../assets/images/${person.image}`)" :alt="person.name">
          </figure>
        </div>
      </div>
      <a :href="person.linkedin" class="is-centered is-flex is-justify-content-center is-align-items-center">
        <h3 class="title is-5 is-inline-block mb-1 mr-1">{{person.name}}</h3>
        <figure class="image is-16x16 is-inline-block">
          <img src="../assets/images/logo-linkedin.svg" alt="LinkedIn profile">
        </figure>
      </a>
      <h4 class="subtitle has-text-centered is-6 mt-3">{{person.position}}</h4>
      
    </div>
  </div>
</template>

<script>
export default {
  props: {
    person: {
      name: String,
      position: String,
      image: String,
      description: String,
      linkedin: String
    }
  }
}
</script>

<style lang="scss" scoped>
.clip {
  object-fit: cover;
}

.glass {
  background: rgba( 255, 255, 255, 0.25 );
  box-shadow: 0 8px 32px 0 rgba( 31, 38, 135, 0.37 );
  backdrop-filter: blur( 4px );
  -webkit-backdrop-filter: blur( 4px );
  border-radius: 10px;
  border: 1px solid rgba( 255, 255, 255, 0.18 );
  height: 100%;
}

.is-centered {
  margin: 0 auto;
}

.has-border {
  border: 5px solid white;
}
</style>