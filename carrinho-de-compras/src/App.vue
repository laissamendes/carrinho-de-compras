<script setup>
import { ref } from 'vue'

const produtos_mari = ref([
  {
    id: 1,
    nome: 'GingerGlow - Nude',
    preco: 85.0,
    quantidade: 0,
    imagem: 'https://www.sephora.com.br/dw/image/v2/BFJC_PRD/on/demandware.static/-/Sites-masterCatalog_Sephora/pt_BR/dwe3713136/images/Color%20BR/mari-maria/Ginger/Paletas/7896032681798_2.jpg?sw=400&sh=400&sm=fit'
  },
  {
    id: 2,
    nome: 'Base - CoverUp',
    preco: 40.0,
    quantidade: 0,
    imagem: 'https://tdc0tj.vtexassets.com/arquivos/ids/178368/7896032688391-Base-Liquida-Mari-Maria-Makeup-Cover-Up-MM011--2-.jpg?v=638113104831030000'
  },
  {
    id: 3,
    nome: 'GingerGlow - Color',
    preco: 85.0,
    quantidade: 0,
    imagem: 'https://www.sephora.com.br/dw/image/v2/BFJC_PRD/on/demandware.static/-/Sites-masterCatalog_Sephora/pt_BR/dw9bc24061/images/Color%20BR/mari-maria/Ginger/Paletas/7896032678132_2.jpg?sw=1200&sh=1200&sm=fit'
  }
])
function incrementar1(id) {
  console.log(produtos_mari.value[id])
  produtos_mari.value[id - 1].quantidade++
}
function decrementar1(id) {
  if (produtos_mari.value[id - 1].quantidade > 0) {
    produtos_mari.value[id - 1].quantidade--
  }
}

function adicionar1(id) {
  if (produtos_mari.value[id - 1].quantidade > 0) {
    carrinho.value.itens.push({
      ...produtos_mari.value[id - 1],
      preco: produtos_mari.value[id - 1].quantidade * produtos_mari.value[id - 1].preco
    })

    carrinho.value.total =
      carrinho.value.total +
      produtos_mari.value[id - 1].preco * produtos_mari.value[id - 1].quantidade
  }
}
const produtos_bt = ref([
  {
    id: 1,
    nome: 'Base BT Skin',
    preco: 70.0,
    quantidade: 0,
    imagem: 'https://d225afdvrjsxie.cloudfront.net/Custom/Content/Products/72/84/72846_base-liquida-bruna-tavares-bt-skin-l40_m1_637720528611787019.jpg'
  },
  {
    id: 2,
    nome: 'Iluminador - BT Mirror',
    preco: 65.0,
    quantidade: 0,
    imagem: 'https://www.sephora.com.br/dw/image/v2/BFJC_PRD/on/demandware.static/-/Sites-masterCatalog_Sephora/pt_BR/dwe82f3b03/images/Color%20BR/BT/7896032669383_4_1000px.jpg?sw=556&sh=680&sm=fit'
  },
  {
    id: 3,
    nome: 'BT Elixir Facial Acqua Hydra',
    preco: 60.0,
    quantidade: 0,
    imagem: 'https://epocacosmeticos.vteximg.com.br/arquivos/ids/429712-320-320/elixir-facial-bt-acqua-hydra--2-.jpg?v=637548140957470000'
  }
])
function incrementar2(id) {
  console.log(produtos_bt.value[id])
  produtos_bt.value[id - 1].quantidade++
}
function decrementar2(id) {
  if (produtos_bt.value[id - 1].quantidade > 0) {
    produtos_bt.value[id - 1].quantidade--
  }
}

function adicionar2(id) {
  if (produtos_bt.value[id - 1].quantidade > 0) {
    carrinho.value.itens.push({
      ...produtos_bt.value[id - 1],
      preco: produtos_bt.value[id - 1].quantidade * produtos_bt.value[id - 1].preco
    })

    carrinho.value.total =
      carrinho.value.total +
      produtos_bt.value[id - 1].preco * produtos_bt.value[id - 1].quantidade
  }
}
const produtos_fran = ref([
  {
    id: 1,
    nome: 'Gloss Labial Pink Chilli',
    preco: 49.9,
    quantidade: 0,
    imagem: 'https://www.atacadaodasmaquiagens.com.br/media/catalog/product/cache/1/image/420x420/9df78eab33525d08d6e5fb8d27136e95/g/l/gloss_aumenta_volume_gloss_hidratante_gloss_fran_gloss_aumento_volume_l_bios_fran_by_franciny_ehlke_pink_chilli_-_atacad_o_das_maquiagens_4_.png'
  },
  {
    id: 2,
    nome: 'Stick Balms By Fran',
    preco: 39.9,
    quantidade: 0,
    imagem: 'https://www.sephora.com.br/dw/image/v2/BFJC_PRD/on/demandware.static/-/Sites-masterCatalog_Sephora/pt_BR/dwe373a572/images/Color%20BR/FRAN/balm/7898969501903-0_1000px.jpg?sw=400&sh=400&sm=fit'
  },
  {
    id: 3,
    nome: 'Máscara Para Cílios Fran Maravicherry',
    preco: 55.0,
    quantidade: 0,
    imagem: 'https://www.sephora.com.br/dw/image/v2/BFJC_PRD/on/demandware.static/-/Sites-masterCatalog_Sephora/pt_BR/dw78571ce4/images/Color%20BR/FRAN/7898969501002_1_1000px.jpg?sw=400&sh=400&sm=fit'
  }
])
function incrementar3(id) {
  console.log(produtos_fran.value[id])
  produtos_fran.value[id - 1].quantidade++
}
function decrementar3(id) {
  if (produtos_fran.value[id - 1].quantidade > 0) {
    produtos_fran.value[id - 1].quantidade--
  }
}

function adicionar3(id) {
  if (produtos_fran.value[id - 1].quantidade > 0) {
    carrinho.value.itens.push({
      ...produtos_fran.value[id - 1],
      preco: produtos_fran.value[id - 1].quantidade * produtos_fran.value[id - 1].preco
    })

    carrinho.value.total =
      carrinho.value.total +
      produtos_fran.value[id - 1].preco * produtos_fran.value[id - 1].quantidade
  }
}
const produtos_bocaRosa = ref([
  {
    id: 1,
    nome: 'Pó Boca Rosa Beauty',
    preco: 49.9,
    quantidade: 0,
    imagem: 'https://www.dailymakeup.com.br/uploads/product_file/BIG98730b5ce4d9423ae4163b6440dc6955.jpg'
  },
  {
    id: 2,
    nome: 'Corretivo Líquido - Boca Rosa',
    preco: 40.0,
    quantidade: 0,
    imagem: 'https://cdn.awsli.com.br/2500x2500/1813/1813898/produto/87526337/210992df05.jpg'
  },
  {
    id: 3,
    nome: 'Boca Rosa by Payot Tint',
    preco: 39.9,
    quantidade: 0,
    imagem: 'https://payottatix.vteximg.com.br/arquivos/ids/157488-1000-1000/7896609543818-1.jpg?v=637831460192770000'
  }
])
function incrementar4(id) {
  console.log(produtos_bocaRosa.value[id])
  produtos_bocaRosa.value[id - 1].quantidade++
}
function decrementar4(id) {
  if (produtos_bocaRosa.value[id - 1].quantidade > 0) {
    produtos_bocaRosa.value[id - 1].quantidade--
  }
}

function adicionar4(id) {
  if (produtos_bocaRosa.value[id - 1].quantidade > 0) {
    carrinho.value.itens.push({
      ...produtos_bocaRosa.value[id - 1],
      preco: produtos_bocaRosa.value[id - 1].quantidade * produtos_bocaRosa.value[id - 1].preco
    })

    carrinho.value.total =
      carrinho.value.total +
      produtos_bocaRosa.value[id - 1].preco * produtos_bocaRosa.value[id - 1].quantidade
  }
}
const carrinho = ref({
  itens: [],
  total: 0
})

</script>

<template>
  <div id="loja-completa">
    <h1>Mendes MakeUp</h1>
    <div>
      <a href="#carrinho"><button class="btn-carrinho">Carrinho 🛒</button></a>
    </div>
    <div id="produtos">
      <div id="produtos-Mari">
        <h2>Marimaria MakeUp</h2>
        <div class="marcas">
          <div v-for="(produto, index) in produtos_mari" :key="index" class="produto">
            <h4>{{ produto.nome }}</h4>
            <img :src="produto.imagem" alt="" width="200" />
            <div class="informacoes">
              <h3>R${{ produto.preco.toFixed(2) }}</h3>
              <button class="btn-adicionar" @click="incrementar1(produto.id)">+</button>
              <img src="lixeira.png" alt="" width="25" class="btn-deletar" @click="resetar" />
              <button class="btn-decrmentar" @click="decrementar1(produto.id)">-</button>
              <p>Quantidade de produto(s): {{ produto.quantidade }}</p>
              <button class="btn-adicionar" @click="adicionar1(produto.id)">Adicionar ao Carrinho</button>
            </div>
          </div>
        </div>
      </div>
      <hr />
      <div id="produtos-BT">
        <h2>Bruna Tavares</h2>
        <div class="marcas">
          <div v-for="(produto, index) in produtos_bt" :key="index" class="produto">
            <h4>{{ produto.nome }}</h4>
            <img :src="produto.imagem" alt="" width="200" />
            <div class="informacoes">
              <h3>R${{ produto.preco.toFixed(2) }}</h3>
              <button class="btn-adicionar" @click="incrementar2(produto.id)">+</button>
              <img src="lixeira.png" alt="" width="25" class="btn-deletar" @click="resetar" />
              <button class="btn-decrmentar" @click="decrementar2(produto.id)">-</button>
              <p>Quantidade de produto(s): {{ produto.quantidade }}</p>
              <button class="btn-adicionar" @click="adicionar2(produto.id)">Adicionar ao Carrinho</button>
            </div>
          </div>
        </div>
      </div>
      <hr />
      <div id="produtos-Fran">
        <h2>Fran</h2>
        <div class="marcas">
          <div v-for="(produto, index) in produtos_fran" :key="index" class="produto">
            <h4>{{ produto.nome }}</h4>
            <img :src="produto.imagem" alt="" width="200" />
            <div class="informacoes">
              <h3>R${{ produto.preco.toFixed(2) }}</h3>
              <button class="btn-adicionar" @click="incrementar3(produto.id)">+</button>
              <img src="lixeira.png" alt="" width="25" class="btn-deletar" @click="resetar" />
              <button class="btn-decrmentar" @click="decrementar3(produto.id)">-</button>
              <p>Quantidade de produto(s): {{ produto.quantidade }}</p>
              <button class="btn-adicionar" @click="adicionar3(produto.id)">Adicionar ao Carrinho</button>
            </div>
          </div>
        </div>
      </div>
      <hr />
      <div id="produtos-bocaRosa">
        <h2>Boca Rosa Beauty</h2>
        <div class="marcas">
          <div v-for="(produto, index) in produtos_bocaRosa" :key="index" class="produto">
            <h4>{{ produto.nome }}</h4>
            <img :src="produto.imagem" alt="" width="200" />
            <div class="informacoes">
              <h3>R${{ produto.preco.toFixed(2) }}</h3>
              <button class="btn-adicionar" @click="incrementar4(produto.id)">+</button>
              <img src="lixeira.png" alt="" width="25" class="btn-deletar" @click="resetar" />
              <button class="btn-decrmentar" @click="decrementar4(produto.id)">-</button>
              <p>Quantidade de produto(s): {{ produto.quantidade }}</p>
              <button class="btn-adicionar" @click="adicionar4(produto.id)">Adicionar ao Carrinho</button>
            </div>
          </div>
        </div>
      </div>
      <hr>
    </div>
    <div id="carrinho">
     <h2>Carrinho de Compras 🛍️</h2>

    </div>
  </div>
</template>

<style scoped>
.marcas {
  display: flex;
  justify-content: space-between;
  text-align: center;
  flex-direction: row;
  height: 450px;
}

.produto {
  margin: 25px;
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
img {
  border-radius: 50%;
  box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.473);
}
img > .btn-deletar {
  box-shadow: none;
}
h4 {
  color: white;
  text-align: center;
  font-size: 20px;
  margin-bottom: 10px;
}
h3 {
  text-shadow: 5px 5px 10px rgb(255, 0, 106);
  color: rgb(255, 0, 98);
}
button {
  color: white;
  background-color: rgb(228, 145, 172);
  border-color: white;
  border-style: double;
  border-radius: 5px;
}
button:hover {
  background-color: rgb(201, 83, 122);
  box-shadow: 2px 2px 5px rgba(223, 37, 130, 0.473);
}
hr {
  border-style: solid;
  color: white;
  margin: 10px;
}
.informacoes{
  position: absolute;
  bottom: 0%;
}
.btn-carrinho{
  font-size:25px;
}
.marcas > img{
  position: absolute;
  bottom: 0%;
}
#carrinho>h2{
  color: white;
 text-decoration: underline;
}
</style>
