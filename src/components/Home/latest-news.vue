<template>
  <div class="trusted-alpha">
    <h2 class="trust-header">Latest News And Events</h2>


    <div class="section-1">
      <div class="section">
<!--        <p class="topmost">January 5, 2020</p>-->
        <img class="image-2" src="https://images.unsplash.com/photo-1571569481471-1753fb013630?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80">
        <h2>Green Logistics</h2>
        <p class="text-1">By the year 2050 we want to reduce all logistics-related emissions to zero – a highly ambitious goal. Our mission as the leading mail and logistics company is to connect people and improve lives.</p>
        <button class="header-button" @click="onPostClick">Find Out More</button>
      </div>
      <div class="section">
<!--        <p class="topmost">January 6, 2021</p>-->
        <img class="image-2" src="https://images.unsplash.com/photo-1590504805643-bb1f94cde7fd?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80">
        <h2>Our Divisions</h2>
        <p class="text-2">Global Express Courier connects people in over 220 countries and territories worldwide. Driven by the power of more than 380,000 employees, we deliver integrated services and tailored solutions for managing and transporting letters, goods and information.</p>
        <button class="header-button" @click="onPostClick">Find Out More</button>
      </div>
      <div class="section">
<!--        <p class="topmost">January 28, 2022</p>-->
        <img class="image-2" src="https://images.unsplash.com/photo-1529854140025-25995121f16f?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80">
        <h2>Insights and Innovation</h2>
        <p class="text-3">To enable collaboration, the company brings together customers, research and academic institutions, industry partners, and logistics experts within the Global Express Courier business divisions. As a thought leader in the logistics industry, Global Express Courier structurally invests in trend research and solution development.</p>
        <button class="header-button" @click="onPostClick">Find Out More</button>
      </div>
    </div>


  </div>
</template>

<script>
export default {
  name: "latest-news"
}
</script>

<style scoped>

.section-1{
  display: flex;
  margin-left: 3%;
  margin-right: 3%;
  justify-content: space-around;
}
.trust-header{
  text-align: center;
  padding-bottom: 10px;
  color: #071333;
  font-size: 30px;
  font-weight: bold;
  margin-top: 3%;
  margin-bottom: 2%;
}

.trust-text{
  text-align: center;
  margin-left: auto;
  margin-right: auto;
  width: 55%;
  padding-bottom: 30px;
  padding-top: 2px;
  font-size: 18px;
  color: #071333;

}

.image-2{
  width: 90%;
  display: block;
  margin-right: auto;
  margin-left: auto;
}

.image-3{
  width: 90%;
  display: block;
  margin-right: auto;
  margin-left: auto;
}

.image-4{
  width: 90%;
  display: block;
  margin-right: auto;
  margin-left: auto;
}

.section{
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.15);
  display: flex;
  justify-content: center;
  flex-direction: column;
  margin-left: 2%;
  margin-right: 2%;
  border-radius: 5px;
  padding: 40px 15px;
  width: 100%;
}
.section h2{
  text-align: center;
  padding-top: 20px;
  color: #071333;
  margin-bottom: 1%;
}

.section p{
  /*text-align: center;*/
  /*margin-right: auto;*/
  /*margin-left: auto;*/
  /*width: 90%;*/
  /*color: #071333;*/
  /*font-size: 18px;*/
}

.text-1{
  text-align: center;
  margin-right: auto;
  margin-left: auto;
  width: 90%;
  color: #071333;
  font-size: 16px;
}

.text-2{
  text-align: center;
  margin-right: auto;
  margin-left: auto;
  width: 90%;
  color: #071333;
  font-size: 16px;
}

.text-3{
  text-align: center;
  margin-right: auto;
  margin-left: auto;
  width: 90%;
  color: #071333;
  font-size: 16px;
}

.trusted-alpha{
  padding-bottom: 3%;
}
.header-button{
  padding: 15px 10px;
  background-color: #ec2552;
  border: 1px solid #ec2552;
  border-radius: 5px;
  margin-top: 5%;
  margin-left: 15%;
  margin-right: 15%;
  color: white;
}

.header-button:hover {
  background-color: white;
  border: 1px solid #ec2552;
  color: #ec2552;
  transition: 4ms ease-in;
}

@media (max-width: 990px) {
  .trust-text{
    width: 80%;
  }

  .section-1{
    display: block;
    margin-left: 10%;
    margin-right: 10%;
    justify-content: space-between;
  }

  .section{
    margin-left: 2%;
    margin-right: 2%;
    margin-bottom: 3%;
  }
}
@media (max-width: 500px) {
  .section-1{
    display: flex;
    justify-content: center;
    flex-direction: column;
  }
  .section{
    margin-bottom: 7%;
  }
}

</style>