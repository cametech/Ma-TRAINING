<template>
  <section id="about" class="about">
    <div class="container">
      <!-- Colonne texte -->
      <div class="about-text">
        <span class="eyebrow">À propos</span>
        <h2 class="heading">
          Une plateforme pensée pour <span class="accent">apprendre</span> et <span class="accent">progresser</span>
        </h2>
        <p class="lead">
          MaTrain vous aide à développer des compétences pratiques grâce à des parcours
          structurés, des évaluations authentiques et des projets guidés par des experts.
        </p>

        <!-- Stats -->
        <div class="stats">
          <div class="stat">
            <strong>5 800+</strong>
            <span>Cours & parcours</span>
          </div>
          <div class="stat">
            <strong>120+</strong>
            <span>Partenaires</span>
          </div>
          <div class="stat">
            <strong>98%</strong>
            <span>Utilisateurs satisfaits</span>
          </div>
        </div>

        <!-- Points clés -->
        <div class="features">
          <div class="card">
            <div class="icon" aria-hidden="true">
              <!-- livre -->
              <svg viewBox="0 0 24 24"><path d="M4 5a2 2 0 0 1 2-2h12v16H6a2 2 0 0 0-2 2V5zM18 19V3" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round"/></svg>
            </div>
            <h3>Contenu de qualité</h3>
            <p>Cours clairs, à jour, et centrés sur la pratique.</p>
          </div>
          <div class="card">
            <div class="icon" aria-hidden="true">
              <!-- médaille -->
              <svg viewBox="0 0 24 24"><path d="M12 3v8m0 0l-3 5 3-2 3 2-3-5zM6 21h12" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"/></svg>
            </div>
            <h3>Évaluations crédibles</h3>
            <p>Certificats et badges pour prouver vos aptitudes.</p>
          </div>
          <div class="card">
            <div class="icon" aria-hidden="true">
              <!-- horloge -->
              <svg viewBox="0 0 24 24"><circle cx="12" cy="12" r="9" fill="none" stroke="currentColor" stroke-width="1.6"/><path d="M12 7v5l3 2" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round"/></svg>
            </div>
            <h3>Rythme flexible</h3>
            <p>Apprenez à votre rythme, où que vous soyez.</p>
          </div>
        </div>
      </div>

      <!-- Colonne visuelle -->
      <div class="about-visual">
        <div class="blob"/>
        <img src="/about.jpg" alt="Apprenants en formation" class="photo">
      </div>
    </div>
  </section>
</template>

<style scoped>
.about {
  padding: 4rem 1.5rem 5rem;
  background: #fff;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1.1fr 0.9fr;
  gap: 3rem;
  align-items: center;
}

.eyebrow {
  display: inline-block;
  font-size: 0.85rem;
  font-weight: 700;
  letter-spacing: .08em;
  text-transform: uppercase;
  color: #512bda;
  background: rgba(81, 43, 218, 0.08);
  padding: .35rem .6rem;
  border-radius: 999px;
  margin-bottom: .8rem;
}

.heading {
  font-size: clamp(1.8rem, 2.2vw + 1rem, 2.6rem);
  line-height: 1.2;
  margin: 0 0 1rem;
  font-weight: 800;
}
.accent { color: #512bda; }

.lead {
  color: #333;
  font-size: 1.05rem;
  margin-bottom: 1.5rem;
  max-width: 56ch;
}

.stats {
  display: grid;
  grid-template-columns: repeat(3, minmax(0,1fr));
  gap: 1rem;
  margin: 1.25rem 0 2rem;
}
.stat {
  background: linear-gradient(0deg, rgba(81,43,218,0.06), rgba(81,43,218,0.06));
  border: 1px solid rgba(81,43,218,0.15);
  border-radius: 14px;
  padding: 1rem;
  text-align: center;
}
.stat strong {
  display: block;
  font-size: 1.4rem;
  font-weight: 800;
  color: #512bda;
}
.stat span {
  font-size: .95rem;
  color: #333;
}

.features {
  display: grid;
  grid-template-columns: repeat(3, minmax(0,1fr));
  gap: 1rem;
}
.card {
  background: #fff;
  border: 1px solid rgba(0,0,0,.06);
  border-radius: 14px;
  padding: 1rem;
  transition: transform .25s ease, box-shadow .25s ease;
}
.card:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 24px rgba(0,0,0,.06);
}
.icon {
  width: 42px; height: 42px;
  display: grid; place-items: center;
  color: #512bda;
  background: rgba(81,43,218,.1);
  border-radius: 10px;
  margin-bottom: .6rem;
}
.icon svg { width: 22px; height: 22px; }
.card h3 { margin: 0 0 .25rem; font-size: 1.05rem; }
.card p  { margin: 0; color: #444; font-size: .98rem; }

.about-visual {
  position: relative;
  min-height: 360px;
}
.blob {
  position: absolute;
  inset: 0;
  background: radial-gradient(60% 60% at 70% 40%, rgba(81,43,218,.18), transparent 60%),
              radial-gradient(50% 50% at 20% 70%, rgba(81,43,218,.12), transparent 60%);
  border-radius: 28px;
  filter: blur(4px);
}
.photo {
  position: relative;
  z-index: 1;
  width: 100%;
  max-width: 480px;
  border-radius: 22px;
  box-shadow: 0 18px 40px rgba(0,0,0,.16);
  border: 6px solid #fff;
  object-fit: cover;
}

/* Responsive */
@media (max-width: 980px) {
  .container { grid-template-columns: 1fr; }
  .about-visual { order: -1; }
  .features { grid-template-columns: 1fr 1fr; }
  .stats { grid-template-columns: 1fr 1fr 1fr; }
}
@media (max-width: 640px) {
  .features { grid-template-columns: 1fr; }
  .stats { grid-template-columns: 1fr 1fr; }
}
</style>
