<template>
  <div class="bg-slate-200 flex flex-col min-h-screen">
    <main class="grow">
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