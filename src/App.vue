<script setup>
import HeaderTop from './components/Header.vue';

import Hero from './components/Hero.vue';
import DoSection from './components/base/DoSection.vue';
import Highlight from './components/Highlight.vue';
import OtherWorks from './components/OtherWorks.vue';
import Skills from './components/Skills.vue';
import Contact from './components/Contact.vue';


import Footer from './components/Footer.vue';

</script>


<template>
  <header>
    <HeaderTop />
  </header>
  
  <main>
    <Hero />
    <section id="Overview">
      <h1>Ce que je sais faire</h1>
      <main>
        <DoSection>
        </DoSection>
        <DoSection>
          <template v-slot:icon>
            <img width="100" height="100" src="https://img.icons8.com/clouds/100/web-settings.png" alt="web-settings"/>
          </template>
          <template v-slot:title>
            Côté serveur
          </template>
          <template v-slot:text>
            Passionné par le <strong>JavaScript</strong>, je sais développer des back-ends robustes et performants.
            <br><br>
            Je sais créer des <strong>API REST</strong> avec Node et Express, et gérer des bases de données <strong>SQL</strong> comme MySQL ou <strong>NoSQL</strong> comme MongoDB.
            <br><br>
            Je maîtrise également <strong>PHP</strong> avec l'architecture <strong>MVC</strong>, pour des projets nécessitant une approche plus traditionnelle.
          </template>
        </DoSection>
        <DoSection>
          <template v-slot:icon>
            <img width="100" height="100" src="https://img.icons8.com/clouds/100/learning.png" alt="learning"/>
          </template>
          <template v-slot:title>
            Compétences variées
          </template>
          <template v-slot:text>
            Je sais créer des sites web avec des <strong>CMS</strong> comme <strong>WordPress</strong> pour proposer des solutions rapides et personnalisées.
            <br><br>
            J’aime apprendre et utiliser tous les outils à ma disposition pour créer, j’ai donc appris la <strong>modélisation 3D, le motion design et les dessins vectoriels</strong>, afin de donner vie à mes idées avec des visuels uniques.
            <br><br>
            Grâce à mes compétences variées, je peux offrir des résultats à la fois créatifs et professionnels.
          </template>
        </DoSection>
      </main>
    </section>
    <Highlight></Highlight>
    <OtherWorks></OtherWorks>
    <Skills></Skills>
    <Contact></Contact>
  </main>

  <Footer />

</template>


<style lang='scss' scoped>
header{
  padding: 0px 150px;
  width: 100%;
  @media screen and (max-width: 1000px) {
    padding: 0px 30px;
  }
  @media screen and (max-width: 440px) {
    padding: 0px 15px;
  }
}
main{
  display: flex;
  flex-direction: column;
  gap: 85px;
  padding: 0px 150px;
  #Overview{
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 50px;
    main{
      display: flex;
      flex-direction: row;
      gap: 35px;
      padding: 0px;
      flex-wrap: wrap;
      justify-content: center
    }
  }



  // Responsive
  @media screen and (max-width: 1000px) {
    padding: 0px 30px;
  }
  @media screen and (max-width: 440px) {
    padding: 0px 15px;
  }
}

</style>