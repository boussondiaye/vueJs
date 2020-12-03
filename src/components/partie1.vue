<template>
  <v-container>
   <!--  <v-row class="text-center"><div style="margin:50px auto 0; width:100%; ">
         <v-text-field label="ici sera affiché le nom" outlined   ></v-text-field> -->
        <!--  <v-img
               :aspect-ratio="16/9"
                :width="width"
                src="./assets/logo.png"
></v-img> -->
    <v-btn
        :loading="loading3"
        :disabled="loading3"
        color="blue-grey"
        class="ma-2 white--text"
        @click="loader = 'loading3'"
        >
        Fichier
      <v-icon
        right
        dark
      >
        mdi-cloud-upload
      </v-icon>
    </v-btn>
    <v-btn
        :loading="loading3"
        :disabled="loading3"
        color="blue-grey"
        class="ma-2 white--text"
        @click="loader = 'loading3'"
        >
        Application
      <v-icon
        right
        dark
      >
        mdi-cloud-upload
      </v-icon>
    </v-btn><v-btn
        :loading="loading3"
        :disabled="loading3"
        color="blue-grey"
        class="ma-2 white--text"
        @click="loader = 'loading3'"
        >
        API
      <v-icon
        right
        dark
      >
        mdi-cloud-upload
      </v-icon>
    </v-btn>
     <!--  </div> 
    </v-row>-->
  </v-container>
</template>

<script>
  export default {
    name: 'partie1',

    data: () => ({  }),
  }
</script>
