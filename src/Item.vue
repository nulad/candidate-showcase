<template>
    <div class="col-md-3">
        <div class="card">
          <img :src="image" :alt="name" class="card-img-top">
          <div class="card-body">
            <h4 class="card-title">{{ name }}</h4>
            <div class="card-text">Dapil: {{ dapil }}</div>
            <div class="card-text">Komisi: {{ komisi }}</div>
            <div class="card-text">{{ summary }}</div>
          </div>
        </div>
      </div>
</template>

<script>
export default {
  name: 'item',
  props: ['id', 'name', 'image', 'dapil', 'komisi', 'summary']
};
</script>

