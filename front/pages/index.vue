<template>
  <v-container>
    <section class="mb-3 text-xs-center">
      <img class="logo" alt="ezMESURE" src="/images/logo-ezMESURE-slogan.png">
    </section>

    <section class="mb-3">
      <v-card class="px-2 py-4">
        <v-card-text>
          <div class="headline mb-4 text-xs-center">Qu'est-ce qu'ezMESURE ?</div>

          <p class="ezmesure-description">
            ezMESURE est un entrepôt national centralisant les statistiques d'usage 
            de la documentation scientifique numérique des établissements de l'enseignement 
            supérieur et de la recherche (ESR).
            ezMESURE propose une interface en ligne de visualisation dynamique, consolidée et
            comparative des données de consultation.
            Ces données sont produites par les installations 
            <a href="http://www.ezpaarse.org">ezPAARSE</a> des
            établissements de l’ESR puis elles sont agrégées dans ezMESURE. 
          </p>
        </v-card-text>
      </v-card>
    </section>

    <section class="mb-3">
      <v-card class="px-2 py-4">
        <v-card-text>
          <div class="headline mb-4 text-xs-center">Projet soutenu par :</div>

          <v-layout row wrap align-center justify-space-around>
            <v-flex xs12 md3 class="text-xs-center" v-for="logo in logos" :key="logo.name">
              <a :href="logo.link" :title="logo.name">
                <img class="partner-logo mb-3" :alt="logo.name" :src="logo.src">
              </a>
            </v-flex>

            <v-flex xs12 class="text-xs-center">
              <v-btn to="/partners" large class="white primary--text">
                Découvrez nos partenaires
              </v-btn>
            </v-flex>
          </v-layout>
        </v-card-text>
      </v-card>
    </section>
  </v-container>
</template>

<script>
export default {
  data () {
    return {
      logos: [
        {
          name: 'CNRS',
          src: '/images/logo-cnrs.jpg',
          link: 'http://www.cnrs.fr/'
        },
        {
          name: 'Couperin',
          src: '/images/logo-couperin.png',
          link: 'http://www.couperin.org/'
        },
        {
          name: 'MESRI',
          src: '/images/logo-mesri.jpg',
          link: 'http://www.enseignementsup-recherche.gouv.fr/'
        },
        {
          name: 'BSN',
          src: '/images/logo-bsn.png',
          link: 'http://www.bibliothequescientifiquenumerique.fr/'
        }
      ]
    }
  }
}
</script>


<style scoped>
.logo {
  max-width: 100%
}
.partner-logo {
  max-width: 100%;
  max-height: 70px;
}
.headline {
  color: #767676;
}
p {
  text-align: justify;
}
p.ezmesure-description {
  font-size: 1.6rem;
}
</style>
