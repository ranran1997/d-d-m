<template>
	<div class="head">
		<div class="header_wrap">
			<ul class="pict_list">
				<li class="pict_one"><a href=""></a></li>
				<li class="pict_two"><a href=""></a></li>
				<li class="pict_three" v-on:click="menueFn"><a href="javascript:;"></a></li>	
			</ul>
			<div class="full_screen" v-show="menue">
				<div class="content_list">
					<ul >
						<li><a href="javascript:;"></a></li>
						<li><a href="/#/">首页</a></li>
						<!-- <li><a href="">预约维修</a></li> -->
						<li><a href="/#/recruit">师傅招募</a></li>
						<li><a href="/#/aboutus">关于叮叮</a></li>
					</ul>
				</div>
			</div>
		</div>
	</div>

</template>

<script>
export default {
  name: 'head',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      menue:false
    }
  },
  mounted:function(){

    
  },
  methods:{
  	menueFn:function(){
  		this.menue = !this.menue
  	}
  }
}
</script>


<style scoped>
.head .header_wrap{
	height:1.173rem;
	width: 100%;
	line-height: 1.173rem;
/*	background-color: red;*/
}
.head .pict_list li{
	display: inline-block;
}
.head .header_wrap .pict_list {
	position: fixed;
	width: 100%;
	z-index: 12;
}
.head .header_wrap ul .pict_one{
	width: 1.84rem;
	height: 0.4rem;
	background:url(./img/logo.png) no-repeat;
	background-size: 1.84rem;
	margin-left: 0.267rem;

}
.head .header_wrap ul .pict_two{
/*    width: 1.44rem;
    height: 0.213rem;
	background:url(./img/font.png) no-repeat;
	background-size: 1.44rem;*/
	width: 4rem;
    height: 0.39rem;
    background-size: 4rem;
    margin-left: 0.2rem;
	background: url(./img/font_one.png) no-repeat;
}
.head .header_wrap ul .pict_three{
    width: 1.28rem/* 96px */;
    height: 1.28rem/* 96px */;
	background:url(./img/nav_icon.png) no-repeat;
	background-size: 1.28rem;
	position:absolute;
    right: 0.533rem;
    z-index: 10;
}
.head .header_wrap .full_screen{
	position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    z-index: 10;
}
.head .header_wrap .content_list{
	height: 100%;
	position: absolute;
	right: 0;
	top: 0;
   	background-color: rgba(215,213,206,0.5);
   	z-index: 10;
 }
.head .header_wrap .content_list li{
	text-align: center;
	width: 4rem;
	font-family: "Microsof Yahei";
/*	background-color: orange;*/
}
.head .header_wrap .content_list li a{
	display: inline-block;
    width: 100%;
    height: 100%;
}
</style>

