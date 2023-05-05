<script setup>
const produtos_mari = [
  {
    id: 1,
    nome: 'GingerGlow - Nude',
    preco: 85.0
  },
  {
    id: 2,
    nome: 'GingerGlow - Color',
    preco: 85.0
  },
  {
    id: 3,
    nome: 'Base - CoverUp',
    preco: 40.0
  }
]
const produtos_bt = [
  {
    id: 1,
    nome: 'Base BT Skin',
    preco: 70.0
  },
  {
    id: 2,
    nome: 'Iluminador - BT Mirror',
    preco: 65.0
  },
  {
    id: 3,
    nome: 'BT Elixir Facial Acqua Hydra',
    preco: 60.0
  }
]
const produtos_fran = [
  {
    id: 1,
    nome: 'Gloss Labial Pink Chilli',
    preco: 49.9
  },
  {
    id: 2,
    nome: 'Stick Balms By Fran',
    preco: 39.9
  },
  {
    id: 3,
    nome: 'Máscara Para Cílios Fran Maravicherry',
    preco: 55.0
  }
]
const produtos_bocaRosa = [
  {
    id: 1,
    nome: 'Pó Boca Rosa Beauty',
    preco: 49.9
  },
  {
    id: 2,
    nome: 'Boca Rosa by Payot Tint',
    preco: 39.9
  },
  {
    id: 3,
    nome: 'Corretivo Líquido - Boca Rosa',
    preco: 40.0
  }
]
</script>

<template>
  <div>
    {{  produtos_bt }}
    {{ produtos_mari }}
    {{  produtos_bocaRosa }}
    {{ produtos_fran }}
  </div>
</template>

<style scoped></style>
