<template>
  <main>
    <section class="disclaimer">
      <div class="ms_container">
        <div class="container-fluid">
          <h5 class="small-title mb-3">Avada forum is the place to be</h5>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aspernatur nam cupiditate, ullam veritatis esse nemo recusandae dolor ipsa optio reprehenderit labore.</p>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
    name: 'AppMain',
}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';
@import '../style/common.scss';

.disclaimer {
  text-align: center;
  width: 100%;
  padding: 5rem;
  background-color: $background-grey;
  .ms_container {
    width: 33%;
    margin: 0 auto;
  }
  p {
    font-size: 1.2rem;
    color: $text-grey;
  }
}
</style>