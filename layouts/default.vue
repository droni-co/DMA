<template>
  <div class="
    bg-slate-200
    flex flex-col
    min-h-screen
    bg-gradient-to-br
    dark:from-slate-900
    dark:to-slate-950
    dark:text-slate-100">
    <main class="grow">
      <UiFormButton @click="toggleColorMode" class="fixed top-4 right-4">
        {{ colorMode.value === 'dark' ? '🌞' : '🌙'  }}
      </UiFormButton>
      <slot />
    </main>
    <footer class="bg-slate-800 text-slate-100 py-4">
      <div class="container mx-auto">
        <p>
          Construido con trabajo duro y mucho café por el equipo de <a href="https://droni.co">Droni.co</a>.
        </p>
      </div>
    </footer>
  </div>
</template>
<script setup lang="ts">
const colorMode = useColorMode()

const toggleColorMode = () => {
  colorMode.preference = colorMode.value === 'dark' ? 'light' : 'dark'
}

</script>