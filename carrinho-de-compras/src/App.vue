<script setup>
import { ref } from 'vue'

const produtos_mari = ref([
  {
    id: 1,
    nome: 'GingerGlow - Nude',
    preco: 85.0,
    quantidade: 0,
    imagem: 'paleta-1.png'
  },
  {
    id: 2,
    nome: 'Base - CoverUp',
    preco: 40.0,
    quantidade: 0,
    imagem: 'base-coverup.png'
  },
  {
    id: 3,
    nome: 'GingerGlow - Color',
    preco: 85.0,
    quantidade: 0,
    imagem: 'paleta-2.png'
  }
])
const produtos_bt = ref([
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
])
const produtos_fran = ref([
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
])
const produtos_bocaRosa = ref([
  {
    id: 1,
    nome: 'Pó Boca Rosa Beauty',
    preco: 49.9,
    quantidade: 0,
    imagem: 'po-bocarosa.jpeg'
  },
  {
    id: 2,
    nome: 'Corretivo Líquido - Boca Rosa',
    preco: 40.0,
    quantidade: 0,
    imagem: 'boca-rosa-tint.jpeg'
    
  },
  {
    id: 3,
    nome: 'Boca Rosa by Payot Tint',
    preco: 39.9,
    quantidade: 0,
    imagem: 'corretivo-bocarosa.png'
  }
])
const quantidade = 0
const carrinho = ref({
  itens: [],
  total: 0,
    
})
function incrementar(index) {
    produtos_mari.value[index].quantidade++
  }
  function decrementar(index) {
    if(produtos_mari.value[index].quantidade > 0){
      produtos_mari.value[index].quantidade--
    }
  }
  
  function adicionar(index) {
    if(produtos_mari.value[index].quantidade > 0){
      
      carrinho.value.itens.push(
        {...produtos_mari.value[index], preco: produtos_mari.value[index].quantidade * produtos_mari.value[index].preco}
      );
      
      carrinho.value.total = carrinho.value.total + produtos_mari.value[index].preco * produtos_mari.value[index].quantidade
       
    }
    
  }
</script>

<template>
  <div id="loja-completa">
    <h1>Mendes MakeUp</h1>
<div>
  <button>Carrinho</button>
</div>
    <div id="produtos">
      <div id="produtos-Mari" >
        <h2>Marimaria MakeUp</h2>
        <div class="marcas">
          <div v-for="(produto, index) in produtos_mari" :key="index">
            <h4>{{ produto.nome }}</h4>
          <img :src="produto.imagem" alt="" width="200" />
          <h3>R${{ produto.preco.toFixed(2) }}</h3>
          <button class="btn-adicionar" @click="incrementar(index)">+</button>
          <img src="lixeira.png" alt="" width="25" class="btn-deletar" @click="resetar" />
          <button class="btn-decrmentar" @click="decrementar(index)">-</button>
          <p>Quantidade de produto(s): {{ quantidade }}</p>
          <button class="btn-adicionar" @click="adicionar">Adicionar ao Carrinho</button>
        </div>
        </div>
        
      </div>
      <hr>
      <div id="produtos-BT" >
        <h2>Bruna Tavares</h2>
        <div class="marcas">
          <div v-for="(produto, index) in produtos_bt" :key="index">
            <h4>{{ produto.nome }}</h4>
          <img :src="produto.imagem" alt="" width="200" />
          <h3>R${{ produto.preco.toFixed(2) }}</h3>
          <button class="btn-adicionar" @click="incrementar">+</button>
          <img src="lixeira.png" alt="" width="25" class="btn-deletar" @click="resetar" />
          <button class="btn-decrmentar" @click="decrementar">-</button>
          <p>Quantidade de produto(s): {{ contador }}</p>
          <button class="btn-adicionar" @click="adicionar">Adicionar ao Carrinho</button>

        </div>
        </div>
        
      </div>
      <hr>
      <div id="produtos-Fran" >
        <h2>Fran</h2>
        <div class="marcas">
          <div v-for="(produto, index) in produtos_fran" :key="index" >
            <h4>{{ produto.nome }}</h4>
          <img :src="produto.imagem" alt="" width="200" />
          <h3>R${{ produto.preco.toFixed(2) }}</h3>
          <button class="btn-adicionar" @click="incrementar">+</button>
          <img src="lixeira.png" alt="" width="25" class="btn-deletar" @click="resetar" />
          <button class="btn-decrmentar" @click="decrementar">-</button>
          <p>Quantidade de produto(s): {{ contador }}</p>
          <button class="btn-adicionar" @click="adicionar">Adicionar ao Carrinho</button>

        </div>
        </div>
        
      </div>
      <hr>
      <div id="produtos-bocaRosa">
        <h2>Boca Rosa Beauty</h2>
<div class="marcas"><div v-for="(produto, index) in produtos_bocaRosa" :key="index" >
  <h4>{{ produto.nome }}</h4>
          <img :src="produto.imagem" alt="" width="200" />
          <h3>R${{ produto.preco.toFixed(2) }}</h3>
          <button class="btn-adicionar" @click="incrementar">+</button>
          <img src="lixeira.png" alt="" width="25" class="btn-deletar" @click="resetar" />
          <button class="btn-decrmentar" @click="decrementar">-</button>
          <p>Quantidade de produto(s): {{ produto.quantidade }}</p>
          <button class="btn-adicionar" @click="adicionar">Adicionar ao Carrinho</button>
        </div></div>
        
      </div>
    </div>
  </div>
</template>

<style scoped>
.marcas {
  display: flex;
  justify-content: space-between;
  text-align: center;
  flex-direction: row;
}

h1 {
  text-align: center;
  font-family: 'URW Chancery L, cursive';
  color: rgb(255, 255, 255);
  text-shadow: 5px 5px 5px rgb(73, 6, 37);
}
h2 {
  text-align: left;
  color: rgb(255, 0, 98);
  margin: 5px;
}
p {
  text-align: center;
  color: rgb(97, 4, 40);
}
img{
  border-radius: 50%;
  box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.473);
}
img > .btn-deletar{
  box-shadow: none;
}
h4{
  color: white;
  text-align: center;
  font-size: 20px;
}
h3{
text-shadow:5px 5px 10px rgb(255, 0, 106) ;
  color: rgb(255, 0, 98);
}
button{
  color: white;
  background-color: rgb(228, 145, 172);
  border-color: white;
  border-style:double;
  border-radius: 5px;
}
button:hover{
  background-color: rgb(201, 83, 122);
  box-shadow: 2px 2px 5px rgba(223, 37, 130, 0.473);
}
hr{
  border-style: solid;
  color: white;
  margin: 10px;
}
</style>
