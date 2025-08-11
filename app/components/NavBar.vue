<template>
  <header class="navbar">
    <NuxtLink to="/" class="logo-link">
      <img src="/logo.png" alt="Logo de l'application" class="logo" >
    </NuxtLink>

    <nav class="nav-links">
      <NuxtLink to="#" class="nav-item">À propos</NuxtLink>
      <NuxtLink to="#" class="nav-item">
        <button class="btn-login">Connexion</button>
      </NuxtLink>
    </nav>
  </header>
</template>

<style scoped>
/* ======== NAVBAR ======== */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #512bda;
  height: 90px;
  width: 100%;
  height: auto;
  color: white;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  position: relative;
  z-index: 10;
}

/* ======== LOGO ======== */
.logo-link {
  display: flex;
  align-items: center;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  width: 50%;
  justify-content: center;
  background-image: url('/logo.png');
}

.logo-link:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
}

.logo {
  height: 100px;
  width: auto;
}

/* ======== NAVIGATION ======== */
.nav-links {
  display: flex;
  align-items: center;
  gap: 2rem;
  width: 50%;
  justify-content: center;
}

.nav-item {
  color: white;
  text-decoration: none;
  font-weight: bold;
  font-size: 20px;
  padding: 0.4rem 0.8rem;
  border-radius: 8px;
  transition: background 0.3s ease, color 0.3s ease, transform 0.3s ease;
}

.nav-item:hover {
  background-color: rgba(255, 255, 255, 0.1);
  color: #d6d1ff;
  transform: translateY(-2px);
}

/* ======== BOUTON DE CONNEXION ======== */
.btn-login {
  background: linear-gradient(135deg, #ffffff, #f0f0f0);
  color: #512bda;
  border: none;
  border-radius: 25px;
  font-size: 0.95rem;
  font-weight: 600;
  padding: 0.5rem 1.2rem;
  cursor: pointer;
  transition: all 0.3s ease;
  box-shadow: 0 3px 10px rgba(0, 0, 0, 0.1);
}

.btn-login:hover {
  background: linear-gradient(135deg, #f8f8f8, #e8e8e8);
  color: #3816a8;
  transform: translateY(-1px);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.15);
}

/* ======== RESPONSIVE ======== */
@media (max-width: 768px) {
  .navbar {
    flex-direction: column;
    height: auto;
    padding: 1rem;
  }

  .logo {
    height: 60px;
    margin-bottom: 1rem;
  }

  .nav-links {
    flex-direction: column;
    gap: 1rem;
  }

  .btn-login {
    width: 100%;
    min-width: 180px;
    text-align: center;
  }
}
</style>
