<template>
  <main
    class="qr-page"
    :style="{
      backgroundImage: `url(${backgroundImage})`,
    }"
  ></main>
</template>

<script setup>
import backgroundImage from '@/assets/home_background.png'
</script>

<style scoped>
.qr-page {
  position: relative;
  min-height: 100vh;

  display: flex;
  justify-content: center;
  align-items: center;

  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;

  overflow: hidden;
}

.overlay {
  position: absolute;
  inset: 0;

  background:
    radial-gradient(circle at top, rgba(34, 211, 238, 0.18), transparent 40%),
    linear-gradient(rgba(15, 23, 42, 0.75), rgba(15, 23, 42, 0.93));

  backdrop-filter: blur(5px);
}

.content {
  position: relative;
  z-index: 2;

  width: min(760px, 92vw);

  padding: 4rem 3rem;

  text-align: center;

  border-radius: 28px;

  background: rgba(15, 23, 42, 0.35);

  border: 1px solid rgba(255, 255, 255, 0.08);

  backdrop-filter: blur(20px);

  box-shadow:
    0 25px 80px rgba(0, 0, 0, 0.35),
    0 0 35px rgba(34, 211, 238, 0.08);
}

.logo {
  width: 340px;
  max-width: 90%;

  margin-bottom: 2rem;
}

.badge {
  display: inline-block;

  padding: 0.45rem 1rem;

  border-radius: 999px;

  background: rgba(34, 211, 238, 0.12);

  border: 1px solid rgba(34, 211, 238, 0.35);

  color: #67e8f9;

  font-size: 0.85rem;

  font-weight: 600;

  margin-bottom: 1.25rem;
}

h1 {
  font-size: clamp(2.5rem, 4vw, 4rem);

  margin-bottom: 1rem;

  color: white;
}

p {
  color: #cbd5e1;

  line-height: 1.8;

  font-size: 1.05rem;

  max-width: 650px;

  margin: auto auto 2.5rem;
}

.explore-btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;

  padding: 1rem 2.5rem;

  border-radius: 999px;

  text-decoration: none;

  color: white;

  font-weight: 700;

  background: linear-gradient(135deg, #06b6d4, #2563eb);

  transition: 0.25s;
}

.explore-btn:hover {
  transform: translateY(-3px);

  box-shadow:
    0 15px 35px rgba(37, 99, 235, 0.35),
    0 0 20px rgba(34, 211, 238, 0.35);
}

.divider {
  width: 90px;
  height: 2px;

  background: rgba(255, 255, 255, 0.15);

  margin: 3rem auto 1.5rem;
}

small {
  color: #94a3b8;

  font-size: 0.9rem;

  line-height: 1.6;
}

@media (max-width: 768px) {
  .content {
    padding: 3rem 1.5rem;
  }

  .logo {
    width: 240px;
  }

  h1 {
    font-size: 2.2rem;
  }

  p {
    font-size: 0.95rem;
  }
}
</style>
