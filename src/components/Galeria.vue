<template>
  <div class="galeria">
    <div class="galeria-container" :style="styleGaleria">
      <div v-for="(foto, i) in fotosG" class="galeria-item">
        <img class="foto" :src="foto" :alt="nome"/>
      </div>
    </div>
    <div class="nav-fotos">
      <span v-for="(foto, i) in fotos" :class="{'active' : indexFoto === i + 1}"
            @click="setTransform(i + 1)"></span>
    </div>
    <i class="material-icons nav-galeria anterior" @click="anterior">chevron_left</i>
    <i class="material-icons nav-galeria proximo" @click="proximo">chevron_right</i>
  </div>
</template>

<script>

  export default {
    name: 'Galeria',
    props:[
      'nome',
      'fotos'
    ],
    data(){
      return {
        fotosG: [],
        indexFoto: 1,
        fotosLen: null,
        styleGaleria: {
          transform: "translate3d(-272px,0,0)",
          transitionDuration: ".3s"
        }
      }
    },
    mounted(){
      this.fotosLen = this.fotos.length;

      this.fotosG.push(this.fotos[this.fotosLen-1]);
      for(let foto of this.fotos){
        this.fotosG.push(foto)
      }
      this.fotosG.push(this.fotos[0]);
    },
    methods: {
      setTransform: function (translate, duration = .3) {
        this.indexFoto = translate;
        this.styleGaleria = {
          transform: `translate3d(${-272 * translate}px,0,0)`,
          transitionDuration: `${duration}s`
        }
        console.log(this.indexFoto)
      },
    proximo: function () {
        if (this.indexFoto === this.fotosLen) {
          this.setTransform(0, 0);
          setTimeout(() => {
            this.setTransform(1, .3);
          }, 10)
        } else {
          this.setTransform(this.indexFoto + 1, .3)
        }
      },
      anterior : function () {
        if (this.indexFoto === 1) {
          this.setTransform(6, 0);
          setTimeout(() => {
            this.setTransform(5, .3);
          }, 10)
        } else {
          this.setTransform(this.indexFoto - 1, .3)
        }
      }
    }
  }
</script>
