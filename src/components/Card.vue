<template>
  <div class="card">
    <div class="card-link">
      <div class="card-favorito tooltip" :class="{'open': openTooltip}" @click="favoritar">
      <span class="tooltip-text">{{favorito ? "Favorito adicionado!" : "Favorito removido!"}}</span>
      <svg viewBox="0 0 21 20" width="20" height="20">
        <path class="coracao" :class="{'active': favorito}"
              d="M6.14 1C3.336 1 1.053 3.46 1.032 6.492c-.04.473-.13 3.225 2.993 5.734 2.936 2.36 5.674 5.26 5.7 5.29l.673.713.67-.715c.03-.03 2.763-2.93 5.7-5.29 3.122-2.508 3.033-5.26 2.99-5.733C19.74 3.46 17.456 1 14.652 1c-1.763 0-3.324.956-4.254 2.41C9.466 1.957 7.906 1 6.14 1" strokeWidth="2" stroke="#FEC53A" fill="none">
        </path>
      </svg>
    </div>
    <div class="card-imagem">
      <img :src="card.foto" :alt="card.descricao"/>
    </div>
    <div class="card-descricao">
      {{card.descricao}}
    </div>
  </div>
  <a href="#" class="link-azul">Veja preços em mais lojas</a>
  <div class="card-preco">
    <div class="card-preco-container">
      <a href="#" class="card-melhor-preco">MELHOR PREÇO</a>
      <span class="verde card-preco-parcelado">{{card.parcelado}}</span>
      <span class="verde card-preco-avista">{{card.aVista}}</span>
      <a href="#" class="link-azul">{{card.loja}}</a>
    </div>
    <button class="btn btn-card-ver">
      <i class="icone-flecha"/>
    </button>
  </div>
  </div>
</template>

<script>
  export default {
    name: 'Card',
    props:[
      'card'
    ],
    data(){
      return {
        openTooltip: false,
        favorito: false
      }
    },
    methods: {
      favoritar : function(){
        this.favorito = !this.favorito;
        this.openTooltip = true;
        setTimeout(() => {
          this.openTooltip = false
        }, 2000)
      }
    }
  }
</script>
