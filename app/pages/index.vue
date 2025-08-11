<template>
  <div>
    <section class="hero">
    <div class="hero-content">
      <div class="text-content">
        <h1 class="title">APPRENEZ<br>SANS LIMITES</h1>
        <p class="subtitle">
          Commencez, réorientez ou faites progresser votre carrière grâce à plus de
          5 800 cours, Certificats Professionnels et diplômes d’universités et d’entreprises
          de renommée internationale.
        </p>

        <div class="buttons">
          <button class="btn primary">Inscrivez-vous gratuitement</button>
          <button class="btn secondary">Essayez MaTrain pour prouver vos aptidudes</button>
        </div>
      </div>

      <div class="image-wrapper">
        <img src="/hero.png" alt="Formation" class="hero-img">
      </div>
    </div>
  </section>
  <AboutSection />
  </div>
</template>

<script setup>
import AboutSection from '~/components/AboutSection.vue'
</script>

<style scoped>
.hero {
  width: 100%;
  background-color: #ffffff;
  padding: 8rem 0rem 2rem 0rem;
  display: flex;
  justify-content: center;
}

.hero-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1200px;
  width: 100%;
  gap: 3rem;
  flex-wrap: wrap;
  margin-left: 190px;
}

.text-content {
  flex: 1;
  width: 50%;
}

.title {
  font-size: 3rem;
  font-weight: 800;
  margin-bottom: 1.5rem;
  line-height: 1.2;
}

.subtitle {
  font-size: 1rem;
  color: #333;
  margin-bottom: 2rem;
  max-width: 550px;
}

.buttons {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
}

.btn {
  padding: 0.8rem 1.6rem;
  border-radius: 6px;
  font-weight: 600;
  font-size: 1rem;
  cursor: pointer;
  transition: all 0.3s ease;
  white-space: nowrap;
}

.primary {
  background-color: #512bda;
  color: white;
  border: none;
}

.primary:hover {
  background-color: #3d20ad;
}

.secondary {
  background: white;
  color: #512bda;
  border: 2px solid #512bda;
}

.secondary:hover {
  background-color: #f1f1ff;
}

.image-wrapper {
  position: relative;
  width: 50%;
  height: 250px;
  flex-shrink: 0;
}


.hero-img {
  position: absolute;
  top: 50%;
  left: 50%;
  z-index: 1;
  transform: translate(-50%, -50%);
  width: 400px;
  height: auto;
  border-radius: 50%;
  object-fit: cover;
  background-color: white;
}
</style>
