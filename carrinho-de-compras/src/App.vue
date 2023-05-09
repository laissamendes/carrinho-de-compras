<script setup>
import { ref, computed } from 'vue'

const produtos_mari = [
  {
    id: 1,
    nome: 'GingerGlow - Nude',
    preco: 85.0,
    quantidade: 0,
    imagem: 'paleta-1.png'
  },
  {
    id: 2,
    nome: 'GingerGlow - Color',
    preco: 85.0,
    quantidade: 0,
    imagem: 'paleta-2.png'
  },
  {
    id: 3,
    nome: 'Base - CoverUp',
    preco: 40.0,
    quantidade: 0,
    imagem: 'base-coverup.png'
  }
]
const produtos_bt = [
  {
    id: 1,
    nome: 'Base BT Skin',
    preco: 70.0,
    quantidade: 0,
    imagem: 'base-bt.jpg'
  },
  {
    id: 2,
    nome: 'Iluminador - BT Mirror',
    preco: 65.0,
    quantidade: 0,
    imagem: 'iluminador-bt.png'
  },
  {
    id: 3,
    nome: 'BT Elixir Facial Acqua Hydra',
    preco: 60.0,
    quantidade: 0,
    imagem: 'primer-bt.jpeg'
  }
]
const produtos_fran = [
  {
    id: 1,
    nome: 'Gloss Labial Pink Chilli',
    preco: 49.9,
    quantidade: 0,
    imagem: 'pink-chily.jpeg'
  },
  {
    id: 2,
    nome: 'Stick Balms By Fran',
    preco: 39.9,
    quantidade: 0,
    imagem: 'balm-fran.jpeg'
  },
  {
    id: 3,
    nome: 'Máscara Para Cílios Fran Maravicherry',
    preco: 55.0,
    quantidade: 0,
    imagem: 'mascara-fran.jpeg'
  }
]
const produtos_bocaRosa = [
  {
    id: 1,
    nome: 'Pó Boca Rosa Beauty',
    preco: 49.9,
    quantidade: 0,
    imagem: 'po-bocarosa.jpeg'
  },
  {
    id: 2,
    nome: 'Boca Rosa by Payot Tint',
    preco: 39.9,
    quantidade: 0,
    imagem: 'corretivo-bocarosa.jpg'
  },
  {
    id: 3,
    nome: 'Corretivo Líquido - Boca Rosa',
    preco: 40.0,
    quantidade: 0,
    imagem: 'boca-rosa-tint.jpeg'
  }
]
//*const mostrar = ref(true)

//function incrementar() {
//quantidade.value++
//}
//function decrementar(){
// quantidade.value--
//}
//function resetar() {
//quantidade.value = 0
//}
//const soma = computed(() => {
//    return contador1.value + contador2.value
//})
</script>

<template>
  <div id="loja-completa">
    <h1>Mendes MakeUp</h1>
    <div id="produtos">
      <div id="produtos-Mari" >
        <h2>Marimaria MakeUp</h2>
        <div class="marcas">
          <div v-for="(produto, index) in produtos_mari" :key="index">
          {{ produto.id }} {{ produto.nome }}
          <img :src="produto.imagem" alt="" width="200" />
          <button class="btn-adicionar" @click="incrementar">+</button>
          <img src="lixeira.png" alt="" width="25" class="btn-deletar" @click="resetar" />
          <button class="btn-decrmentar" @click="decrementar">-</button>

          <p>Quantidade de produto(s): {{ quantidade }}</p>
        </div>
        </div>
        
      </div>
      <div id="produtos-BT" >
        <h2>Bruna Tavares</h2>
        <div class="marcas">
          <div v-for="(produto, index) in produtos_bt" :key="index">
          {{ produto.id }} {{ produto.nome }}
          <img :src="produto.imagem" alt="" width="200" />
          <button class="btn-adicionar" @click="incrementar">+</button>
          <img src="lixeira.png" alt="" width="25" class="btn-deletar" @click="resetar" />
          <button class="btn-decrmentar" @click="decrementar">-</button>
          <p>Quantidade de produto(s): {{ contador }}</p>
        </div>
        </div>
        
      </div>
      <div id="produtos-Fran" >
        <h2>Fran</h2>
        <div class="marcas">
          <div v-for="(produto, index) in produtos_fran" :key="index" >
          {{ produto.id }} {{ produto.nome }}
          <img :src="produto.imagem" alt="" width="200" />
          <button class="btn-adicionar" @click="incrementar">+</button>
          <img src="lixeira.png" alt="" width="25" class="btn-deletar" @click="resetar" />
          <button class="btn-decrmentar" @click="decrementar">-</button>

          <p>Quantidade de produto(s): {{ contador }}</p>
        </div>
        </div>
        
      </div>
      <div id="produtos-bocaRosa">
        <h2>Boca Rosa Beauty</h2>
<div class="marcas"><div v-for="(produto, index) in produtos_bocaRosa" :key="index" >
          {{ produto.id }} {{ produto.nome }}
          <img :src="produto.imagem" alt="" width="200" />
          <button class="btn-adicionar" @click="incrementar">+</button>
          <img src="lixeira.png" alt="" width="25" class="btn-deletar" @click="resetar" />
          <button class="btn-decrmentar" @click="decrementar">-</button>

          <p>Quantidade de produto(s): {{ produto.quantidade }}</p>
        </div></div>
        
      </div>
    </div>
  </div>
</template>

<style scoped>
.marcas {
  display: flex;
  justify-content: space-around;
}

h1 {
  text-align: center;
  font-family: 'URW Chancery L, cursive';
  color: rgb(255, 0, 98);
  text-shadow: 5px 5px 5px rgba(0, 0, 0, 0.623);
}
h2 {
  text-align: left;
  color: rgb(255, 68, 140);
  margin: 5px;
}
p {
  text-align: center;
}
</style>
