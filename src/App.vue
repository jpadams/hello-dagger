<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <div class="wrapper">
      <HelloWorld msg="Hello AppDeveloperCon!" />
      <pre>
dagger -m github.com/jpadams/qr call \
  generate-ascii-qr --data https://docs.dagger.io/quickstart #remote mod

dagger call build        #context dir for source

dagger call build --source .

dagger call build --source https://github.com/dagger/hello-dagger\#1c4f2ac2ecbf34cb30ed3c9815f9f9b060415c8b publish ttl.sh/appdevcon

dagger call build -i # --interactive

export NGROK_TOKEN=$(op read "op://Private/ngrok/token" -n)
dagger call share --ngrok-token=env:NGROK_TOKEN up

dagger call share --ngrok-token=cmd:'op read "op://Private/ngrok/token" -n'

dagger call qr --api-token cmd:'op read "op://Private/ngrok/api" -n'
      </pre>
    </div>
  </header>
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
