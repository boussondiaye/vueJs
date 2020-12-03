<template>
  <v-app>
   
      <h1 style=" margin: 0px  10px  0px 71px; "> Bienvenue dans Niagara</h1>
    <v-container>
      <v-row class="text-center">
        <v-col class="mb-1"    >
          <div id='dropdownlist' style="margin:50px auto 0; width:100px;" > 
            <ejs-dropdownlist :dataSource='FiltrerPar'   placeholder="Filtres"   >
            </ejs-dropdownlist>
          </div>
       </v-col>
        <v-col class="mb-5"></v-col>
      <v-col class="mb-6">
        <v-btn  style="margin:50px auto 0; width:auto;" color="primary">
          + Ajouter une source
        </v-btn>
      </v-col>
    </v-row>
    
  </v-container>
    <v-main>
      <HelloWorld/>
      <partie1/>
        <vue2Dropzone/>
    </v-main>
      <vue-dropzone
        ref="myVueDropzone"
        :useCustomSlot="true"
        id="dropzone"
        @vdropzone-upload-progress="uploadProgress"
        :options="dropzoneOptions"
        @vdropzone-file-added="fileAdded"
        @vdropzone-sending-multiple="sendingFiles"
        @vdropzone-success-multiple="success"
      ></vue-dropzone>
  </v-app>
</template>

<script>
import Vue from 'vue';
import HelloWorld from './components/HelloWorld';
import partie1 from './components/partie1';
import { DropDownListPlugin } from '@syncfusion/ej2-vue-dropdowns';
import vue2Dropzone from 'vue2-dropzone';
import 'vue2-dropzone/dist/vue2Dropzone.min.css';
Vue.use(DropDownListPlugin);
export default {
  name: 'App',

  components: {
    HelloWorld,
    partie1,
    vueDropzone: vue2Dropzone,
},
  data: () => ({
  FiltrerPar:  ['Logistique', 'Production', 'Qualité', 'Maintenance'],
   
  }),
};
</script>
 <style>
@import url(https://cdn.syncfusion.com/ej2/material.css);

</style>