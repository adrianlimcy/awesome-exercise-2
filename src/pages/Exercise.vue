<template>
<!--
	Awesome Exercise 2 - Vue.js Lists & Components

	1) Create an array for the food items you see on the page. Each object in the array should contain properties for the image url, name, description and deliciousness
	2) Create a v-for loop that displays these food items onto the page, with all the data coming from the food array (hint: for the image src, use :src)
	3) Add your own food item to the list
	4) Create a child component and use it to display each of your items (don't use the components/Solution/Food.vue file)
	5) Add unique id's to the food array for each item, and apply these to a :key property on your v-for loop

	-->
<q-page padding>
  <div class="q-pa-md row items-stretch">
    <food v-for="food in foods" :key="food.id" :food="food">
    </food>
    <!-- <div class="card shadow-1" v-for="food in foods">
        <img :src="food.url" width="198" height="180">
        <div class="card-content">
          <h1 class="text-primary">{{food.name}}</h1>
          <p>{{food.description}}</p>
          <p>
            <small>
              <b>Delicousness</b>
            </small>
            <b class="text-primary">
              {{food.deliciousness}}
            </b>
          </p>
        </div>
      </div> -->

    <!-- <div class="card shadow-1">
  	  	<img src="https://i.imgur.com/0umadnY.jpg" width="198" height="180">
  	  	<div class="card-content">
  	  		<h1 class="text-primary">Burger</h1>
  	  		<p>A burger is a sandwich consisting of one or more cooked patties of ground meat, usually beef, placed inside a sliced bread roll or bun. </p>
  	  		<p>
	  	  		<small>
	  	  			<b>Delicousness:</b>
	  	  		</small>
	  	  		<b class="text-primary">
		  	  		4/5
	  	  		</b>
  	  		</p>
  	  	</div>
  	  </div>
  	  <div class="card shadow-1">
  	  	<img src="https://i.imgur.com/b9zDbyb.jpg"
  	  	 width="198" height="180">
  	  	<div class="card-content">
  	  		<h1 class="text-primary">Pizza</h1>
  	  		<p>Pizza is a savory dish of Italian origin, consisting of a usually round, flattened base of leavened wheat-based dough.</p>
  	  		<p>
	  	  		<small>
	  	  			<b>Delicousness:</b>
	  	  		</small>
	  	  		<b class="text-primary">
		  	  		5/5
	  	  		</b>
  	  		</p>
  	  	</div>
  	  </div>
  	  <div class="card shadow-1">
  	  	<img src="https://i.imgur.com/RbKjUjB.jpg"
  	  	 width="198" height="180">
  	  	<div class="card-content">
  	  		<h1 class="text-primary">Sprouts</h1>
  	  		<p>The Brussels sprout is a member of the Gemmifera Group of cabbages, grown for its edible buds.</p>
  	  		<p>
	  	  		<small>
	  	  			<b>Delicousness:</b>
	  	  		</small>
	  	  		<b class="text-primary">
		  	  		1/5
	  	  		</b>
  	  		</p>
  	  	</div>
  	  </div> -->

  </div>
</q-page>
</template>

<script>
export default {
  data() {
    return {
      foods: [
        // food objects go here
        {
          id: 1,
          url: 'https://i.imgur.com/0umadnY.jpg',
          name: 'Burger',
          description: 'A burger is a sandwich consisting of one or more cooked patties of ground meat, usually beef, placed inside a sliced bread roll or bun.',
          deliciousness: '4/5'
        },
        {
          id: 2,
          url: 'https://i.imgur.com/b9zDbyb.jpg',
          name: 'Pizza',
          description: 'Pizza is a savory dish of Italian origin, consisting of a usually round, flattened base of leavened wheat-based dough.',
          deliciousness: '5/5'
        },
        {
          id: 3,
          url: 'https://i.imgur.com/RbKjUjB.jpg',
          name: 'Sprouts',
          description: 'The Brussels sprout is a member of the Gemmifera Group of cabbages, grown for its edible buds.',
          deliciousness: '1/5'
        },
        {
          id: 4,
          url: 'https://i.imgur.com/tASMPby.jpeg',
          name: 'Pasta',
          description: 'fettuccine-creamy-tomato-sauce',
          deliciousness: '3/5'
        }
      ]
    }
  },
  components: {
    'food': require('components/FoodList.vue').default
  }
}
</script>

<style>
.card {
  flex-basis: 210px;
  border: 1px solid #ccc;
  border-radius: 5px;
  padding: 5px;
  margin-right: 10px;
  margin-bottom: 10px;
}

.card img {
  max-width: 100%;
}

.card-content {
  padding: 0 10px;
}

h1 {
  font-size: 23px;
}

p {
  font-size: 14px;
}
</style>
