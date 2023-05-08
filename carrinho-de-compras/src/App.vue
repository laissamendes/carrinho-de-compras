<script setup>

import { ref, computed } from 'vue'

const produtos_mari = [
  {
    id: 1,
    nome: 'GingerGlow - Nude',
    preco: 85.0 , 
    quantidade: 0
  },
  {
    id: 2,
    nome: 'GingerGlow - Color',
    preco: 85.0 , 
    quantidade: 0
  },
  {
    id: 3,
    nome: 'Base - CoverUp',
    preco: 40.0 , 
    quantidade: 0
  }
]
const produtos_bt = [
  {
    id: 1,
    nome: 'Base BT Skin',
    preco: 70.0 , 
    quantidade: 0
  },
  {
    id: 2,
    nome: 'Iluminador - BT Mirror',
    preco: 65.0 , 
    quantidade: 0
  },
  {
    id: 3,
    nome: 'BT Elixir Facial Acqua Hydra',
    preco: 60.0 , 
    quantidade: 0
  }
]
const produtos_fran = [
  {
    id: 1,
    nome: 'Gloss Labial Pink Chilli',
    preco: 49.9 , 
    quantidade: 0
  },
  {
    id: 2,
    nome: 'Stick Balms By Fran',
    preco: 39.9 , 
    quantidade: 0
  },
  {
    id: 3,
    nome: 'Máscara Para Cílios Fran Maravicherry',
    preco: 55.0 , 
    quantidade: 0
  }
]
const produtos_bocaRosa = [
  {
    id: 1,
    nome: 'Pó Boca Rosa Beauty',
    preco: 49.9 , 
    quantidade: 0
  },
  {
    id: 2,
    nome: 'Boca Rosa by Payot Tint',
    preco: 39.9 , 
    quantidade: 0
  },
  {
    id: 3,
    nome: 'Corretivo Líquido - Boca Rosa',
    preco: 40.0 , 
    quantidade: 0
  }
]
const mostrar = ref(true)

function incrementar() {
  quantidade.value++
}
function decrementar(){
  quantidade.value--
}
function resetar() {
 quantidade.value = 0
}
const soma = computed(() => {
    return contador1.value + contador2.value
})
</script>

<template>
  <div id="loja-completa">
    <h1>Mendes MakeUp</h1>
  <div id="produtos">
<div id="produtos-Mari">
  <h2>Marimaria MakeUp</h2>
    <div v-for="(produto, index) in produtos_mari" :key="index" >  {{ produto.id }} {{  produto.nome }} {{ quantidade }}
      
      <button class="btn-adicionar" @click="incrementar">+</button>
      <button class="btn-decrmentar" @click="decrementar">-</button>
      <button class="btn-deletar" @click="resetar">C</button>
      <p>Quantidade de produto(s): {{ quantidade }}</p>
    </div>
    <img src="paleta-1.png" alt="" width="250">
    <img src="paleta-2.png" alt="" width="250">
    <img src="base-coverup.png" alt="" width="250">
</div>
<div id="produtos-BT">
  <h2>Bruna Tavares</h2>
  <div v-for="(produto, index) in produtos_bt" :key="index" >  {{ produto.id }} {{  produto.nome }} {{ quantidade }}
      <button class="btn-adicionar" @click="incrementar">+</button>
      <button class="btn-decrmentar" @click="decrementar">-</button>
      <button class="btn-deletar" @click="resetar">C</button>
      <p>Quantidade de produto(s): {{ contador }}</p>
      <img src="base-bt.jpg" alt="" width="250">
      <img src="iluminador-bt.png" alt="" width="250">
      <img src="primer-bt.jpeg" alt="" width="250">
    </div>
  </div>
<div id="produtos-Fran">
  <h2>Fran</h2>
  <div v-for="(produto, index) in produtos_fran" :key="index" >  {{ produto.id }}  {{  produto.nome }} {{ quantidade }}
      <button class="btn-adicionar" @click="incrementar">+</button>
      <button class="btn-decrmentar" @click="decrementar">-</button>
      <button class="btn-deletar" @click="resetar"><img src="lixeira.png" alt=""></button>
      <img src="balm-fran.jpeg" alt="" width="250">
      <img src="mascara-fran.jpeg" alt="" width="250">
      <img src="pink-chily.jpeg" alt="" width="250">
      <p>Quantidade de produto(s): {{ contador }}</p>
    </div>
</div>
<div id="produtos-bocaRosa">
<h2>Boca Rosa Beauty</h2>
  <div v-for="(produto, index) in produtos_bocaRosa" :key="index" >  {{ produto.id }} {{  produto.nome }} {{ quantidade }}
      <button class="btn-adicionar" @click="incrementar">+</button>
      <button class="btn-decrmentar" @click="decrementar">-</button>
      <button class="btn-deletar" @click="resetar">C</button>
      <p>Quantidade de produto(s): {{ contador }}</p>
      <img src="po-bocarosa.jpeg" alt="" width="250">
      <img src="corretivo-bocarosa.jpg" alt="" width="250">
      <img src="boca-rosa-tint.jpeg" alt="" width="250">
    </div>
</div>
  </div>
  </div>
  
  <div>
    {{  produtos_bt }}
    {{ produtos_mari }}
    {{  produtos_bocaRosa }}
    {{ produtos_fran }}
  </div>
</template>

<style scoped></style>
