<template>
	<div class="product">
		<HeaderShayna />
		<!-- Breadcrumb Section Begin -->
		<div class="breacrumb-section text-left">
			<div class="container">
				<div class="row">
					<div class="col-lg-12">
						<div class="breadcrumb-text product-more">
							<router-link to="/"><i class="fa fa-home"></i> Home</router-link>
							<span>Detail</span>
						</div>
					</div>
				</div>
			</div>
		</div>
		<!-- Breadcrumb Section Begin -->

		<!-- Product Shop Section Begin -->
		<section class="product-shop spad page-details">
			<div class="container">
				<div class="row">
					<div class="col-lg-12">
						<div class="row">
							<div class="col-lg-6">
								<div class="product-pic-zoom">
									<img class="product-big-img" :src="gambar_default" alt="" />
								</div>
								<div class="product-thumbs">
									<carousel class="product-thumbs-track ps-slider" :nav="false" :dots="false">
										<div class="pt" @click="changeImage(gambar[0])" :class="gambar[0] == gambar_default ? 'active' : ''">
											<img src="img/mickey1.jpg" alt="" />
										</div>

										<div class="pt"  @click="changeImage(gambar[1])" :class="gambar[1] == gambar_default ? 'active' : ''">
											<img src="img/mickey2.jpg" alt="" />
										</div>

										<div class="pt"  @click="changeImage(gambar[2])" :class="gambar[2] == gambar_default ? 'active' : ''">
											<img src="img/mickey3.jpg" alt="" />
										</div>

										<div class="pt"  @click="changeImage(gambar[3])" :class="gambar[3] == gambar_default ? 'active' : ''">
											<img src="img/mickey4.jpg" alt="" />
										</div>
									</carousel>
								</div>
							</div>
							<div class="col-lg-6">
								<div class="product-details text-left">
									<div class="pd-title">
										<span>oranges</span>
										<h3>Pure Pineapple</h3>
									</div>
									<div class="pd-desc">
										<p>
											Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis, error officia. Rem aperiam laborum voluptatum vel, pariatur modi hic provident eum iure natus quos non a sequi, id accusantium! Autem.
										</p>
										<p>
											Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quam possimus quisquam animi, commodi, nihil voluptate nostrum neque architecto illo officiis doloremque et corrupti cupiditate voluptatibus error illum. Commodi expedita animi nulla aspernatur.
											Id asperiores blanditiis, omnis repudiandae iste inventore cum, quam sint molestiae accusamus voluptates ex tempora illum sit perspiciatis. Nostrum dolor tenetur amet, illo natus magni veniam quia sit nihil dolores.
											Commodi ratione distinctio harum voluptatum velit facilis voluptas animi non laudantium, id dolorem atque perferendis enim ducimus? A exercitationem recusandae aliquam quod. Itaque inventore obcaecati, unde quam
											impedit praesentium veritatis quis beatae ea atque perferendis voluptates velit architecto?
										</p>
										<h4>$495.00</h4>
									</div>
									<div class="quantity">
										<router-link to="shoppingcart"><a href="shopping-cart.html" class="primary-btn pd-cart">Add To Cart</a></router-link>
									</div>
								</div>
							</div>
						</div>
					</div>
				</div>
			</div>
		</section>
		<RelateShayna />
		<FooterShayna />
	</div>
</template>

<script>
// @ is an alias to /src
import HeaderShayna from '@/components/HeaderShayna.vue';
import RelateShayna from '@/components/RelateShayna.vue';
import FooterShayna from '@/components/FooterShayna.vue';

import carousel from "vue-owl-carousel";


export default {
	name: 'Product',
	components: {
		HeaderShayna,
		RelateShayna,
		FooterShayna,
		carousel
	},
	data(){
		return{
			gambar_default: "img/mickey1.jpg",
			gambar: [
				"img/mickey1.jpg",
				"img/mickey2.jpg",
				"img/mickey3.jpg",
				"img/mickey4.jpg"
			]
		}
	},
	methods: {
		changeImage(urlImage){
			this.gambar_default = urlImage;
		}
	} 
};
</script>

<style>
	.product-thumbs .pt{
		margin-right: 14px;
	}
</style>