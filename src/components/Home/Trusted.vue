<template>
<div class="trusted-alpha">
  <h2 class="trust-header">Our Services</h2>
  <p class="trust-text">Globally known for our ability to handle every last detail of our customers’ particular logistics and forwarding needs, Global Express Courier Special Services team takes care of all your logistics.</p>

  <div class="section-1">
    <div class="section">
      <img class="image-2" src="https://images.unsplash.com/photo-1591768793355-74d04bb6608f?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1172&q=80">
      <h2>Road Freight</h2>
      <p class="text-1">Our Road Freight Products offer high quality road transportation, from standard services such as LTL (Less-than-Truck Load), PTL (Part) or FTL (Full-Truck Load) shipments to temperature controlled and highly secured transports.</p>
      <button class="header-button" @click="onPostClick">Read More</button>
    </div>
    <div class="section">
      <img class="image-3" src="https://images.unsplash.com/photo-1617952739858-28043cecdae3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1770&q=80">
      <h2>Sea Freight</h2>
      <p class="text-2">With our broad product range we cover different equipment types and consolidation services to ensure your cargo reaches the right place, at the right time in a cost-efficient way. In order to deliver highest reliability we have planned space protection from every major container port in the world.</p>
      <button class="header-button" @click="onPostClick">Read More</button>
    </div>
    <div class="section">
      <img class="image-4" src="https://images.unsplash.com/photo-1486556813609-9a827fdc306f?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1169&q=80">
      <h2>Air Freight</h2>
      <p class="text-3">Express shipping. 4.55$/km Weigh above 4,554 pounds cost additional charges.10Years Experience We are servicing in the market for the last 10 years with a wide range of services. 10.4K Customers Served We proudly announce that we have more than 10.4k highly satisfied clients. 120 Cities Delivered Our services are provided in more than 120 cities with timely delivery.</p>
      <button class="header-button" @click="onPostClick">Read More</button>
    </div>
  </div>


</div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Trusted",
  methods: {
    onPostClick() {
      this.$router.push("/services");
      window.scrollTo(0, 0);
    },
  },
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

