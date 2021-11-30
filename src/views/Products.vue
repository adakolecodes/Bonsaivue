<template>
  <div class="container-fluid">
    <h1>Bonsai Trees</h1>

    <div class="container row mx-auto d-flex">
      <div v-for="product in products" :key="product.id" class="card col-sm-4 mt-3">
        <a :href="'/product-details/' + product.id" class="stretched-link">
          <img class="card-img-top" :src="product.productImage" />
        </a>
        <div class="card-body">
          <h5 class="card-title">{{product.productTitle}}</h5>
          <p class="card-text">{{product.productPrice}}</p>
          <a :href="'/product-details/' + product.id" class="btn btn-primary">More Info</a>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      products: [
        {
          id: 1,
          productTitle: 'Chinese Juniper Itagawa',
          productPrice: 2000,
          productDescription: 'Spectacular Itoigawa Chinese Juniper Tree, approximately 35-39cm tall and in a ceramic bonsai pot.',
          productImage: 'https://tbhpwebdevapi.azurewebsites.net/img/OutdoorBonsai/OutdoorBonsai_1.jpg',
          checkoutOptions: ['Tools', 'Soil', 'Care'],
        },
        {
          id: 2,
          productTitle: 'Large Chinese Juniper Itagawa',
          productPrice: 1495,
          productDescription: 'Lovely Large Itoigawa Chinese Juniper Tree, approximately 98-100cm tall.',
          productImage: 'https://tbhpwebdevapi.azurewebsites.net/img/OutdoorBonsai/OutdoorBonsai_2.jpg',
          checkoutOptions: ['Tools', 'Soil', 'Care'],
        },
        {
          id: 3,
          productTitle: '35-38cm Itagawa',
          productPrice: 3250,
          productDescription: 'Beautiful Chinese Itiogawa Juniper, approximately 35-38cm tall and planted in an oval ceramic bonsai pot.',
          productImage: 'https://tbhpwebdevapi.azurewebsites.net/img/OutdoorBonsai/OutdoorBonsai_3.jpg',
          checkoutOptions: ['Tools', 'Soil', 'Care'],
        },
        {
          id: 4,
          productTitle: 'Brussels Bonsai',
          productPrice: 195,
          productDescription: 'Lovely Brussels Bonsai Tree in a ceramic bonsai pot, approximately 27-29cm tall.',
          productImage: 'https://tbhpwebdevapi.azurewebsites.net/img/OutdoorBonsai/OutdoorBonsai_4.jpg',
          checkoutOptions: ['Tools', 'Care'],
        },
        {
          id: 5,
          productTitle: 'Satsuki Azalea ',
          productPrice: 595,
          productDescription: 'Gorgeous Satsuki Azalea  Bonsai Tree, approximately 28-33cm tall and planted in an unglazed oval ceramic bonsai pot.',
          productImage: 'https://tbhpwebdevapi.azurewebsites.net/img/OutdoorBonsai/OutdoorBonsai_5.jpg',
          checkoutOptions: ['Tools', 'Care'],
        },
      ],
    };
  },
};
</script>

<style scoped>
</style>