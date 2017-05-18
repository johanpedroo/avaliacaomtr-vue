<template>
  <div class="barra-pesquisa container">
    <div class="logo">
      <a href="#">
        <img src="http://image.buscape.com/material/logo-buscape.svg" alt="logo"/>
      </a>
    </div>
    <div class="pesquisa">
      <form action="#" class="form-pesquisa">
        <i class="material-icons">search</i>
        <input type="text" class="campo-pesquisa" placeholder="Digite o produto, marca ou modelo e dá um busca!"/>
        <button type="submit" class="btn btn-pesquisa">BUSCAR</button>
      </form>
    </div>
    <div class="perfil">
      <div class="perfil-container">
        <div class="avatar">
          <img :src="avatar" alt="imagem do perfil"/>
          <i class="icone-avatar"> </i>
        </div>
        <div class="dropdown">
          <ul>
            <li>
              <a href="#" class="fav-ico">Meus favoritos</a>
            </li>
            <li>
              <a href="#" class="prot-ico">Buscapé te Protege</a>
            </li>
            <li>
              <a href="#" class="comp-ico">Minhas compras</a>
            </li>
            <li>
              <a href="#" class="perf-ico">Meu Perfil</a>
            </li>
            <li>
              <a href="#" class="sair-ico">Sair</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import avatar from '../assets/misc/avatar.jpg'

  export default {
    name: 'BarraPesquisa',
    data (){
      return {
        avatar
      }
    }
  }
</script>
