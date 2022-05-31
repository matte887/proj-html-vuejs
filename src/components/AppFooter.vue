<template>
  <footer>
    <!-- footer -->
    <div class="ms_footer">
      <div class="container my-5">
        <div class="row row-cols-4">
          <div class="col">
            <h4>Avada tech forum</h4>
            <p class="ms_text-grey">
              Phasellus eget metus non magna pellentesque rhoncus non at nisi.
              Vestibulum eu bibendum velit. Nunc euismod in lorem vitae aliquam.
              Mauris auctor justo.
            </p>
          </div>
          <div class="col" v-for="(item, index) in footerItems" :key="index">
            <h4>{{ item.title }}</h4>
            <ul>
              <li v-for="(bulletPoint, index) in item.voices" :key="index">
                <a href="">
                  {{ bulletPoint }}
                </a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <!-- /footer -->
    <hr />
    <!-- footer bottom -->
    <div class="ms_footer-bottom my-4">
      <div class="container">
        <div class="row align-items-center">
          <div class="col">
            <p class="ms_text-grey">
              &copy; Copyright 2012 - 2020 | Avada Theme by
              <span class="ms_text-black">Theme Fusion</span>
              | All Rights Reserved | Powered by
              <span class="ms_text-black">WordPress</span>
            </p>
          </div>
          <div class="col-auto">
            <ul class="d-flex">
              <li>
                <a class="facebook" href=""
                  ><i class="fa-brands fa-facebook-f"></i
                ></a>
              </li>
              <li>
                <a class="twitter" href=""
                  ><i class="fa-brands fa-twitter"></i
                ></a>
              </li>
              <li>
                <a class="instagram" href=""
                  ><i class="fa-brands fa-instagram"></i
                ></a>
              </li>
              <li>
                <a class="youtube" href=""
                  ><i class="fa-brands fa-youtube"></i
                ></a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <!-- /footer bottom -->
  </footer>
</template>

<script>
export default {
  name: "AppFooter",
  props: {
    footerItems: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

footer {
  font-size: 0.9rem;
}

.ms_footer {
  h4 {
    text-transform: uppercase;
    margin-bottom: 2rem;
    font-size: 1.2rem;
    font-weight: 700;
  }

  ul {
    padding: 0;
    li {
      font-weight: 500;
      margin-left: 0.7rem;
      position: relative;
    }

    li::before {
      font-family: "FontAwesome";
      content: "\f105";
      font-size: 0.7rem;
      position: absolute;
      left: -12px;
      top: 2px;
    }

    li::after {
      content: "";
      display: block;
      width: 100%;
      height: 1px;
      background-color: $background-grey;
      margin: 1rem 0;
    }
  }
}

hr {
  color: gray;
}

.ms_footer-bottom {
  .ms_text-black {
    color: initial;
  }
  li a {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 50px;
    height: 50px;
    margin: 0 0.5rem;
    border-radius: 50%;
    font-size: 1.2rem;
    color: $white-shade;
  }

  .facebook {
    background-color: #3c5998;
  }
  .twitter {
    background-color: #54acee;
  }
  .instagram {
    background-color: #3f729b;
  }
  .youtube {
    background-color: #cd201e;
  }
}
</style>