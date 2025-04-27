<script setup>
import { ref } from 'vue';
import Recipe from './Recipe.vue';

let selectedProduce = ref('');
const recipies = {
  's-pot': {
    name: 'Sweet Potato',
    choices: [
      {
        source: 'https://www.forksoverknives.com/recipes/vegan-baked-stuffed/sweet-potato-bread/',
        title: 'Sweet Potato Bread from Forks Over Knives',
        desc: 'This extra-moist sweet potato bread is packed full of tart dried fruit and infused with warm pumpkin pie spices. A crunchy topping of pumpkin seeds adds a tasty contrasting texture to the rich, dense dough. Enjoy this heavenly loaf toasted or untoasted, plain or with a slather of creamy corn butter or your favorite vegan jam.',
        ingredients: [
          '12 oz. sweet potatoes (1 large sweet potato), peeled and cut into 1-inch chunks',
          '½ cup unsweetened applesauce',
          '2 tablespoons flaxseed meal',
          '1 teaspoon pure vanilla extract',
          '1¾ cups flour',
          '½ cup sugar',
          '2 teaspoons pumpkin pie spice',
          '1 teaspoon baking powder',
          '½ teaspoon sea salt',
          '½ cup dried fruit, chopped',
          '2 tablespoons pumpkin seeds',
        ],
        directions: [
          'Place potatoes in a medium saucepan with enough water to cover potatoes. Cover pan and cook over medium heat for 15 to 20 minutes, until tender. Drain well. Mash potatoes. Measure 1 cup mashed potatoes.',
          'Preheat oven to 350°F. In a bowl stir together the 1 cup mashed potatoes, the applesauce, flaxseed meal, vanilla, and ⅓ cup water. Let stand 5 minutes.',
          'In a large bowl whisk together the next five ingredients (through sea salt). Add sweet potato mixture to flour mixture; stir just until combined. Fold in dried fruit. Spoon batter into an 8x4-inch nonstick or silicone loaf pan. Top with pumpkin seeds.',
          'Bake 45 to 55 minutes or until a toothpick inserted in center comes out clean. Cool in pan on a wire rack 10 minutes. Remove loaf from pan. Cool 30 minutes before slicing.',
        ],
        nutrition: {
          calories: '196',
          fat: '2g',
          protien: '4g',
          carbs: '45g',
          sugar: '22g',
          fiber: '5g',
        },
        yeild: '1 loaf/12 slices',
        rating: '4/5',
      },
      {
        source: 'https://www.allrecipes.com/recipe/6666/sweet-potato-bread-i/',
        title: 'Sweet Potato Bread from All Recipes',
        desc: 'This sweet potato bread is made with cooked and mashed sweet potatoes, pecans, and spices for a Southern delight — one bite, and you want more!',
        ingredients: [
          '1 cup mashed sweet potatoes (1 large sweet potato)',
          '1 ¾ cups sifted all-purpose flour',
          '1 ½ cups white sugar',
          '1 teaspoon baking powder',
          '1 teaspoon cinnamon',
          '½ teaspoon nutmeg',
          '¼ teaspoon salt',
          '½ cup vegetable oil',
          '2 eggs',
          '½ cup chopped pecans',
          '⅓ cup water',
        ],
        directions: [
          'Gather the ingredients. Preheat the oven to 350 degrees F (175 degrees C). Grease a 9x5-inch loaf pan.',
          'Combine sugar and oil in a large bowl; beat well. Add eggs and beat until well combined. Combine flour, baking soda, cinnamon, nutmeg, and salt in a separate bowl. Stir flour mixture into egg mixture alternately with water. Stir in sweet potatoes and chopped nuts. Pour batter into the prepared loaf pan.',
          'Bake in the preheated oven until a toothpick inserted into the center comes out clean, about 1 hour.',
        ],
        nutrition: {
          calories: '196',
          fat: '14g',
          protien: '4g',
          carbs: '43g',
          sugar: '26g',
          fiber: '2g',
        },
        yeild: '1 loaf/12 slices',
        rating: '4.8/5',
      },
    ],
    id: 1,
  },
  banana: {
    name: 'Banana',
    choices: [
      {
        source: 'https://www.allrecipes.com/recipe/20144/banana-banana-bread/',
        title: 'Banana Banana Bread from All Recipes',
        desc: "This banana bread recipe creates the most delicious, moist loaf with loads of banana flavor. Why compromise the banana flavor? Friends and family love my recipe and say it's by far the best! It tastes wonderful toasted. Enjoy!",
        ingredients: [
          '2 ⅓ cups mashed overripe bananas (4-5 large bananas)',
          '2 cups all-purpose flour',
          '1 teaspoon baking soda',
          '¼ teaspoon salt',
          '¾ cup brown sugar',
          '½ cup butter',
          '2 large eggs, beaten',
        ],
        directions: [
          'Preheat the oven to 350 degrees F (175 degrees C). Lightly grease a 9x5-inch loaf pan.',
          'Combine flour, baking soda, and salt in a large bowl. Beat brown sugar and butter with an electric mixer in a separate large bowl until smooth. Stir in eggs and mashed bananas until well blended. Stir banana mixture into flour mixture until just combined. Pour batter into the prepared loaf pan.',
          'Bake in the preheated oven until a toothpick inserted into the center comes out clean, about 60 minutes. Let bread cool in pan for 10 minutes, then turn out onto a wire rack to cool completely.',
        ],
        nutrition: {
          calories: '231',
          fat: '9g',
          protien: '4g',
          carbs: '35g',
          sugar: '16g',
          fiber: '2g',
        },
        yeild: '1 loaf/12 slices',
        rating: '4.7/5',
      },
    ],
    id: 2,
  },
  'bnut-squash': {
    name: 'Butternut Squash',
    choices: [
      {
        source: 'https://www.allrecipes.com/recipe/234276/autumn-spiced-butternut-squash-bread/',
        title: 'Butternut Squash Bread from All Recipes',
        desc: 'This butternut squash bread is a great bread for Thanksgiving and a delicious way to use butternut squash!',
        ingredients: [
          '2 ⅔ cups white sugar',
          '⅔ cup butter',
          '2 cups pureed cooked butternut squash (1 large squash)',
          '4 eggs',
          '⅔ cup water',
          '3 ⅓ cups all-purpose flour',
          '2 teaspoons baking soda',
          '2 teaspoons baking powder',
          '1 ½ teaspoons salt',
          '1 teaspoon ground cinnamon',
          '1 teaspoon ground cloves or to taste',
          '⅔ cup chopped walnuts (Optional)',
          '⅔ cup raisins (Optional)',
        ],
        directions: [
          'Preheat the oven to 350 degrees F (175 degrees C). Grease two 9x5-inch loaf pans.',
          'Beat sugar and butter together in a bowl until fluffy. Stir butternut squash, eggs, and water into sugar mixture.',
          'Mix flour, baking soda, baking powder, salt, cinnamon, and ground cloves in another bowl; stir into sugar mixture. Add walnuts and raisins; stir until batter is just blended. Pour batter into prepared loaf pans.',
          'Bake in the preheated oven until a toothpick inserted into the center comes out clean, about 1 hour. Cool in the pans briefly before removing to cool completely on a wire rack.',
        ],
        nutrition: {
          calories: '254',
          fat: '8g',
          protien: '3g',
          carbs: '45g',
          sugar: '27g',
          fiber: '1g',
        },
        yeild: '2 loaves/20 slices',
        rating: '4.8/5',
      },
      {
        source: 'https://www.mybakingaddiction.com/butternut-squash-bread/',
        title: 'Butternut Squash Bread from My Baking Addiction',
        desc: 'Butternut Squash Bread is full of autumnal flavors that only get more complex with time. This moist and delicious quick bread may just become your new favorite fall treat.',
        ingredients: [
          '1 cup butternut squash puree (1 small squash)',
          '2 eggs',
          '½ cup vegetable oil',
          '¼ cup water',
          '1 cup white sugar',
          '½ cup brown sugar',
          '1 ¾ cups all-purpose flour',
          '1 teaspoons baking soda',
          '½ teaspoon kosher salt',
          '2 teaspoons ground cinnamon',
          '½ teaspoon ground nutmeg',
          '½ teaspoon ground cardamom',
        ],
        directions: [
          'Preheat oven to 350°F (175°C). Grease and flour one 8.5 x 4.5 x 2.5 inch loaf pan.',
          'In a large bowl, combine butternut squash puree, eggs, vegetable oil, water, white sugar, and brown sugar. Mix until well combined.',
          'In another bowl, whisk together flour, baking soda, salt, cinnamon, nutmeg, and cardamom.',
          'Gradually add dry ingredients to wet ingredients; mix until just combined.',
          'Pour batter into prepared loaf pan. Bake for 55-65 minutes or until a toothpick inserted into the center comes out clean. Cool in the pan for 10 minutes before transferring to a wire rack to cool completely.',
        ],
        nutrition: {
          calories: '315',
          fat: '12g',
          protien: '4g',
          carbs: '50g',
          sugar: '31g',
          fiber: '1g',
        },
        yeild: '1 loaf/10 slices',
        rating: '4.4/5',
      },
    ],
    id: 3,
  },
};

const onChangeProduce = (event) => {
  const selectedKey = event.target.value;
  console.log(selectedKey);
  selectedProduce = selectedKey;
  const selectedRecipe = recipies[selectedKey];
  console.log(selectedProduce);
  if (selectedProduce.length > 0) {
    console.log(`Selected produce: ${selectedProduce}`);
  }
};
</script>

<template>
  <h3>Don Donald's Bread Maker</h3>
  <label for="produce-select">Select your produce:</label>
  <select name="produce-select" @change="onChangeProduce($event)">
    <option value="" disabled selected hidden>Select your option</option>
    <option value="s-pot">Sweet Potato</option>
    <option value="bnut-squash">Butternut Squash</option>
    <option value="banana">Banana</option>
  </select>

  <div v-if="selectedProduce" :key="recipies[selectedProduce].id">
    {{ recipies[selectedProduce]?.name }}
    <!-- <p>Produce has been selected</p> -->
  </div>
</template>
