<template>

<div>
  <section class="hero is-dark is-large">
    <div class="hero-body">
      <div class="container">
        <div class="logo">
          <Logo style="fill:white" />
        </div>
        <h2 class="subtitle has-text-centered">
          The natural kitchen <em>essential</em> for garlic lovers
        </h2>
      </div>
    </div>
  </section>
  <UpArrow />
  <section class="section" id="how-to">
    <div class="container">
      <h2 class="title has-text-centered">How To Use</h2>
      <TwoLines />
      <HowTo />
    </div>
  </section>
  <ArrowsDown color="#FFF" />
  <section class="section section-invert" id="why">
    <div class="container">
      <h2 class="title has-text-centered">Why A Rock?</h2>
      <TwoLines />
      <Why />
    </div>
  </section>
  <ArrowsDown color="hsl(0, 0%, 86%)"/>
  <section class="section" id="about">
    <div class="container">
      <h2 class="title has-text-centered">About Us</h2>
      <TwoLines />
      <About />
    </div>
  </section>
  <footer class="footer">
    <div>Brought to you by <strong>Terri Tutt Essentials, LLC</strong></div>
  </footer>
</div>

</template>

<script>
import Logo from '@/assets/garlic_rock_logo.svg';
import Why from '@/components/Why';
import HowTo from '@/components/HowTo';
import About from '@/components/About';
import UpArrow from '@/components/UpArrow';
import TwoLines from '@/components/TwoLines';
import ArrowsDown from '@/components/ArrowsDown';
import TopCurve from '@/components/TopCurve';

export default {
  name: 'Landing',
  components: { Logo, Why, HowTo, About, UpArrow, TwoLines, ArrowsDown, TopCurve },
  data() {
    return {
      Logo,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
@import '../../static/_main';
h2 {
  margin-bottom: 1.5rem !important;
}

.subtitle {
  font-weight: 600;
  margin: 0 auto;
  padding: 1rem 0;
}

.hero {
  background-size: cover;
  background-image: url('https://firebasestorage.googleapis.com/v0/b/garlic-rock.appspot.com/o/BackgroundPhoto_v6.jpg?alt=media&token=64c69fd9-52b6-4925-a81e-6b2d26dd941c');
}

.hero-body {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.logo {
  max-width: 800px;
  margin: 0 auto;
}

.section-invert {
  background-color: $white;
}

.footer {
  background-color: $black;
  color: $white;
  strong {
    color: $white;
  }
}

@media (max-width: $tablet) {
  .hero {
    height: 100vh;
    max-height: 800px;
  }

  .footer {
    text-align: center;
  }
}
</style>
