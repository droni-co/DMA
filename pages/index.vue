<template>
  <div class="md:flex container mx-auto">
    <div class="text-center md:w-1/2">
      <img src="~/assets/img/logo.png" alt="DMA" class="mx-auto" />
    </div>
    <div class="py-20 text-slate-800 max-w-[500px] dark:text-slate-200">
      <h2 class="text-4xl font-bold text-balance">
        Bachillerato virtual DMA
      </h2>
      <p class="text-slate-400">
        Estudia desde cualquier lugar.
      </p>

      <p class="text-xl my-4">
        Con la plataforma de bachillerato virtual DMA, puedes estudiar desde cualquier lugar y a tu propio ritmo.
        No pierdas la oportunidad de <strong>terminar tus estudios de bachillerato en un menor tiempo</strong>.
      </p>

      <p class="text-xl my-4">
        <strong>¡Inscríbete ya!</strong>
      </p>

      <form class="my-4">
        <UiFormInput v-model="lead.name" placeholder="Nombre completo" class="mb-3" />
        <UiFormInput v-model="lead.email" placeholder="Email" type="email" class="mb-3" />
        <UiFormInput v-model="lead.phone" placeholder="Teléfono" class="mb-3" />
        <UiFormInput v-model="lead.birthdate" placeholder="Fecha de nacimiento" type="date" class="mb-3" />
        <UiFormSelect
          v-model="lead.last_course"
          :options="courses"
          itemValue="id"
          itemLabel="name"
          placeholder="Último curso aprobado"
          class="mb-3"
        />
        <UiFormSwitch v-model="lead.terms" label="Acepto los términos y condiciones" required />
        <UiFormButton type="submit">
          <i class="mdi mdi-rocket-launch-outline"></i>
          Inscribirme
        </UiFormButton>
      </form>
      {{ lead }}
    </div>
  </div>
  <div class="container mx-auto my-8">
    <h2 class="text-3xl font-bold text-balance text-center">
      ¿Cómo funciona?
    </h2>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
      <div class="p-4 text-center">
        <i class="mdi mdi-account-plus-outline text-5xl"></i>
        <h3 class="text-xl font-bold text-balance">Inscríbete</h3>
        <p>
          Regístrate en la plataforma y selecciona el plan de estudios que más se ajuste a tus necesidades.
        </p>
      </div>
      <div class="p-4 text-center">
        <i class="mdi mdi-cast-education text-5xl"></i>
        <h3 class="text-xl font-bold text-balance">Estudia</h3>
        <p>
          Accede a los contenidos de las materias y estudia a tu propio ritmo.
        </p>
      </div>
      <div class="p-4 text-center">
        <i class="mdi mdi-book-education-outline text-5xl"></i>
        <h3 class="text-xl font-bold text-balance">Certifícate</h3>
        <p>
          Al finalizar tus estudios, obtén tu certificado de bachillerato.
        </p>
      </div>
    </div>
  </div>
  <div class="container mx-auto flex">
    <div class="w-1/2">
      <div class="p-5">
        <iframe class="w-full aspect-video shadow-lg" src="https://www.youtube.com/embed/lQmjUTzsrj4?si=A6I2uuHqO3KcHaiD" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
useSeoMeta({
  title: 'DMA | Bachillerato virtual',
  ogTitle: 'DMA | Bachillerato virtual',
  description: 'DMA es una plataforma de bachillerato virtual que te permite estudiar desde cualquier lugar.',
  ogDescription: 'DMA es una plataforma de bachillerato virtual que te permite estudiar desde cualquier lugar.',
  ogImage: 'https://dma-edu.co/image.png',
  twitterCard: 'summary_large_image',
})

const lead = ref({
  name: '',
  email: '',
  phone: '',
  birthdate: '',
  last_course: '',
  terms: false,
})

const courses = ref([
  { id: 0, name: 'Último curso aprobado' },
  { id: 5, name: 'Quito de primaria' },
  { id: 6, name: 'Sexto de bachillerato' },
  { id: 7, name: 'Séptimo de bachillerato' },
  { id: 8, name: 'Octavo de bachillerato' },
  { id: 9, name: 'Noveno de bachillerato' },
  { id: 10, name: 'Décimo de bachillerato' },
])
</script>
