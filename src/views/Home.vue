<template>
	<div class="wrap">
		<div class="header">
			<!-- 前端技术栈 -->
		</div>
		<swiper :options="swiperOption">
			<swiper-slide>
				<div class="item1">
					<swipperItem1/>
				</div>
			</swiper-slide>
			<swiper-slide>
				<div class="item2">
					2
				</div>
			</swiper-slide>
			<swiper-slide>
				<div class="item3">
					3
				</div>
			</swiper-slide>
			<swiper-slide>
				<div class="item4">
					4
				</div>
			</swiper-slide>
			<swiper-slide>
				<div class="item5">
					5
				</div>
			</swiper-slide>
			<div class="swiper-pagination" slot="pagination"></div>
		</swiper>
	</div>
</template>

<script>
  export default {
		name: 'carrousel',
		components:{
			swipperItem1:()=>import('@/components/swipperItem1')
		},
    data() {
      return {
        swiperOption: {
          pagination: {
            el: '.swiper-pagination'
          },
					direction:'vertical',
					mousewheel: true,
					paginationClickable: true,
        },
      }
    },
    mounted() {
      // setInterval(() => {
      //   console.log('simulate async data')
      //   if (this.swiperSlides.length < 10) {
      //     this.swiperSlides.push(this.swiperSlides.length + 1)
      //   }
      // }, 3000)
    }
  }
</script>
<style lang="scss">
.wrap{
	.header{
		position: fixed;
		width: 100%;
		height: 60px;
		line-height: 60px;
		left: 0;
		top: 0;
		background-color: #007D6B;
		z-index: 11;
		border-bottom: 1px solid #999;
	}
	.swiper-container {
		width: 100%;
		height: 100vh;
		
		.swiper-slide{
			&>div{
				width: 100%;
				height: 100%;
				padding-top:60px;
			}
		}
		.item1{
			// background-color: #87B0A5;
			background:url('../images/vue.jpg');
			background-size: 100% 100%;
			background-repeat:no-repeat;
		}
		.item2{
			background-color: #007B5D;
		}
		.item3{
			background-color: #4D5E8F;
		}
		.item4{
			background-color: #4A839E;
		}
		.item5{
			background-color: #8F5949;
		}
		
	}  
}
</style>