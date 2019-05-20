<template>
	<div class="details">
		<div class="container">
			<div class="row">
				<div class="col-md-12" v-for="(product,index) in products" :key="index">
					<div v-if="proId == product.productId">
						<h1>{{product.productTitle}}</h1>
						<img :src="product.image" class="img-fluid">
					</div>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
	export default{
		name:'details',
		data(){
			return{
      proId: this.$route.params.Pid,
      title: "details",
      products: [
        {
          productTitle: "TRONCO S15 PLUS 02P",
          image: require("../assets/images/product1.png"),
          productId: 1
        },
        {
          productTitle: "TRONCO S15 2.8 D",
          image: require("../assets/images/product2.png"),
          productId: 2
        },
        {
          productTitle: "TRONCO S15 01P CP CC",
          image: require("../assets/images/product3.png"),
          productId: 3
        },
        {
          productTitle: "TRONCO TRADICIONAL",
          image: require("../assets/images/product4.png"),
          productId: 4
        },
        {
          productTitle: "TRONCO PADRÃO",
          image: require("../assets/images/product5.png"),
          productId: 5
        },
        {
          productTitle: "TRONCO VERSÁTIL 2.8 D",
          image: require("../assets/images/product6.png"),
          productId: 6
        }
      ]
    };
  }
};
</script>
