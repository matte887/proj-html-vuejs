<template>
  <main>
    <section class="ms_disclaimer">
      <div class="ms_container">
        <div class="container-fluid">
          <h5 class="small-title mb-3">Avada forum is the place to be</h5>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aspernatur nam cupiditate, ullam veritatis esse nemo recusandae dolor ipsa optio reprehenderit labore.</p>
        </div>
      </div>
    </section>

    <section class="ms_news mt-4">
      <h5 class="ms_small-title mb-3">Phasellus eget metus</h5>
      <h3 class="ms_h3-title">All the latest news</h3>
      <div class="container">
        <div class="row row-cols-3 gx-5">
          <div class="col">
            <img src="../assets/images/selected/post_feat_img_25-700x441.jpg" alt="">
            <h5>Morbi vitae dui euismod vulputate siollicitudin</h5>
            <p class="ms_small-text">October 11th, 2015 | <span>2 Comments</span></p>
            <p class="ms_test-grey">Lorem ipsum dolor sit amet consectetur adipisicing elit. Nemo voluptatem quia explicabo laboriosam inventore praesentium, a maxime.</p>
          </div>
          <div class="col">
            <img src="../assets/images/selected/post_feat_img_24-700x441.jpg" alt="">
            <h5>Vivamus pellenteque, felis quis varius</h5>
            <p class="ms_small-text">October 11th, 2015 | Comments off</p>
            <p class="ms_test-grey">Lorem ipsum dolor sit amet consectetur adipisicing elit. Nemo voluptatem quia explicabo laboriosam inventore praesentium, a maxime.</p>
          </div>
          <div class="col">
            <img src="../assets/images/selected/post_feat_img_23-700x441.jpg" alt="">
            <h5>Donec ornare pretium erget scelisque justo</h5>
            <p class="ms_small-text">October 11th, 2015 | Comments off</p>
            <p class="ms_test-grey">Lorem ipsum dolor sit amet consectetur adipisicing elit. Nemo voluptatem quia explicabo laboriosam inventore praesentium, a maxime.</p>
          </div>
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

.ms_disclaimer {
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

.ms_news {
  text-align: center;

  h3:after {
    width: 5rem;
    height: 2px;
    content: "";
    display: block;
    margin: 3rem auto;
    background-color: $accent-color;
  }

  .container {
    text-align: initial;
    h5 {
      margin-top: 1.5rem;
      font-size: 1.1rem;
      font-weight: 700;
    }
    p span {
      color: initial;
      font-weight: 500;
    }
  }
}
</style>