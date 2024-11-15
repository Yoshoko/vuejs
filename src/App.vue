<template>
  <div id="app" class="container-fluid">
    <div class="row">
      <div class="col-3 ">
        <Logo />
        <Menu />
        <SocialLinks :links="socialLinks" />
      </div>

      <div class="col-9 ">
        <img :src="image1" alt="Image Principale" class="img-fluid mb-4" />

        <div class="d-flex align-items-start mb-4">
          <Card :main="false" :title="aboutCard.title" :description="aboutCard.description" :src="aboutCard.src">
            <Button text="Lire la suite" />
          </Card>
          <Quatuor :images="artImages" />
        </div>

        <h2 class="blog">Mon Blog</h2>
        <div class="d-flex justify-content-between">
          <Card v-for="(card, index) in blogCards" :key="index" :main="card.main" :title="card.title"
            :description="card.description" :src="card.src">
            <Button text="Lire la suite" />
          </Card>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from './components/Logo.vue';
import Menu from './components/Menu.vue';
import Card from './components/Card.vue';
import Quatuor from './components/Quatuor.vue';
import SocialLinks from './components/SocialLinks.vue';
import Button from './components/Button.vue';
import image1 from './assets/image1.jpeg';
import image2 from './assets/image2.jpeg';
import image3 from './assets/image3.jpeg';
import image4 from './assets/image4.jpeg';
import image5 from './assets/image5.jpeg';
import image6 from './assets/image6.jpeg';
import image7 from './assets/image7.jpeg';


export default {
  components: {
    Logo,
    Menu,
    Card,
    Quatuor,
    SocialLinks,
    Button
  },
  data() {
    return {
      artImages: [image2, image7, image4, image1], 
      socialLinks: [
        { name: 'Instagram', url: 'https://instagram.com' },
        { name: 'Facebook', url: 'https://facebook.com' }
      ],
      image1,
     aboutCard: {
        title: 'À propos de Seurat',
        description: 'Georges Seurat, un pionnier du néo-impressionnisme, connu pour sa technique révolutionnaire du pointillisme.',
        src: image5
      },
      blogCards: [
        {
          main: true,
          title: 'Un Dimanche Après-midi',
          description: 'Une exploration de la célèbre œuvre "Un Dimanche Après-midi à l\'Île de la Grande Jatte", symbole du pointillisme.',
          src: image2
        },
        {
          main: true,
          title: 'Le Cirque',
          description: 'Analyse de "Le Cirque", une œuvre inachevée montrant l\'intérêt de Seurat pour le mouvement et la lumière.',
          src: image3
        },
        {
          main: true,
          title: 'La Parade',
          description: 'Découverte de "La Parade de Cirque", une représentation de la vie nocturne et des lumières artificielles.',
          src: image6
        }
      ]

    };
  }
};
</script>

<style>
body {
  background-color: #f8f9fa;
}
.blog{
  text-align: center;
}
</style>
