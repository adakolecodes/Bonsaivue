<template>
    <div class="container content">
        <h1>{{products[idAsInt].productTitle}}</h1>
        <h4>{{products[idAsInt].productPrice}}</h4>
        <p>{{products[idAsInt].productDescription}}</p>
        <img :src="products[idAsInt].productImage" alt="" class="img-fluid">
    </div>
</template>

<script>
    export default {
        props: {
            id: {
                type: String,
            }
        },

        computed: {
            idAsInt() {
                return parseInt(this.id)
            }
        },

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
    }
</script>

<style scoped>
.content{
    text-align: left;
}
</style>