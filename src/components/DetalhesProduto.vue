<template>
  <article class="detalhes">
    <h1 class="nome">{{produto.nome}}</h1>
    <div class="infos">
          <span class="texto-preco">
            A partir de:
            <span class="preco">
              R$
              <span class="preco-inteiro">
                1.187
              </span>
              ,10
            </span>
          </span>
      <div class="historico-preco">
        <a href="#" class="link-azul">Veja o histórico de preços de até 1 ano</a>
      </div>
    </div>
    <div class="avaliacao">
      <div class="rating">
        <span class="estrela"> </span>
        <span class="estrela"> </span>
        <span class="estrela"> </span>
        <span class="estrela"> </span>
        <span class="meia-estrela"> </span>
        <a href="#" class="link-azul">399 Consumidores avaliaram</a>
      </div>
      <div class="enviar-avaliacao">
        <a href="#" class="link-azul">Enviar avaliação</a>
      </div>
    </div>
  </article>
</template>

<script>
  export default {
    name: 'DetalhesProduto',
    props: [
      'produto'
    ]
  }
</script>
