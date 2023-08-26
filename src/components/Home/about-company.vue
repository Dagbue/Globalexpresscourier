<template>
  <p class="about-text-1">About Company</p>
<div class="about-alpha" >

  <div class="about-section-1">
    <h4 class="about-header-1">Broad services for business shipping.</h4>
    <p class="about-text-2">From packages to pallets, and local to global, get flexible, reliable, and affordable shipping solutions that fit your business.</p>

    <div class="box">
    <div class="about-content">
      <i class='bx bx-task'></i>
      <div class="about-content-text">
        <h4>Putting the power of expert shipping to work.</h4>
        <p>Get one step ahead of your competition and reach your customers with the strength of the Global Express Courier global network. That's more than 400,000 people working across 220 countries or territories with one goal: making your parcel delivery services work to your logistical and competitive advantage.
          Whether you're an entrepreneur or enterprise, Global Express Courier tools and technologies will help you create efficiencies, centralize control, cut costs, and increase productivity. Explore the variety of our shipping services that can be tailored to your business needs. With more flexibility and better
          insight, you'll have peace of mind that you're shipping the best way for your business.</p>
      </div>
    </div>
    </div>

    <button class="header-button" @click="onPostClick">Read More</button>



  </div>

  <div class="about-section-2">
    <img alt="About-Image" src="@/assets/bus.png"  class="about-image" />
  </div>

</div>
</template>

<script>
export default {
  name: "about-company",
  methods: {
     onPostClick() {
      this.$router.push("/about");
      window.scrollTo(0, 0);
    },
  },
}
</script>

<style scoped>
.about-alpha{
  display: flex;
  padding-bottom: 5%;
}
.about-image{
  width: 82%;
  border-radius: 5px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
  margin-left: 10%;
  margin-top: 7%;
}
.about-content{
  display: flex;
  padding-top: 15px;
  padding-right: 25px;
}
.about-content-text{
  padding-left: 15px;
}

.about-content-text h4{
  font-weight: bold;
  margin-bottom: 2%;
}
.about-content-text p {
  font-size: 17px;
  line-height: 1.6;
}
.about-section-1{
  width: 95%;
  margin-left: 80px;
  color: #071333;
}

.box{
  /*box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);*/
  border-radius: 5px;
  margin-bottom: 12px;
}


.about-text-1{
  text-align: center;
  font-size: 28px;
  color: #071333;
  margin-top: 4%;
  margin-bottom: 2%;
}

.about-header-1{
  text-align: center;
  margin-bottom: 2%;
  font-size: 18px;
}
.about-text-2{
  font-size: 16px;
  margin-bottom: 2%;
  line-height: 1.3;
  text-align: center;
}

.about-section-2{
  /*padding-right: 20px;*/
}

.header-button{
  padding: 15px 55px;
  background-color: #ec2552;
  border: 1px solid #ec2552;
  border-radius: 5px;
  margin-top: 5px;
  color: white;
  font-size: 15px;
  margin-left: 40px;
}

.header-button:hover {
  background-color: white;
  border: 1px solid #ec2552;
  color: #ec2552;
  transition: 4ms ease-in;
}


i{
  font-size: 35px;
  color: #ec2552;;
  padding-right: 10px;
}

.about-content-text h4{
  font-size: 25px;
  color: #071333;
}

@media (max-width: 990px) {
  .about-alpha{
    display: flex;
    flex-direction: column-reverse;
  }
  .about-section-1{
    width: 100%;
    margin-left: unset;
    padding-left: 3%;
    padding-right: 3%;
  }
  .about-section-2{
    padding-right: unset;
    margin-left: 5%;
  }
  .about-image{
    margin-top: 2%;
    margin-bottom: 3%;
    width: 93%;
    margin-left: unset;
  }
  .about-text-2{
    text-align: center;
  }
  .header-button{
    display: block;
    margin-left: auto;
    margin-right: auto;
    margin-top: 5%;
  }
}
</style>



