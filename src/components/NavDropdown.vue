<template>
  <div class="menu_dropdown">
    <div class="container">
      <ul>
        <router-link to="/" @click='categories= !categories'>Visage</router-link>
        <router-link to="/">Corps</router-link>
        <router-link to="/">Capillaire</router-link>
        <router-link to="/">Douche</router-link>
        <router-link to="/">Savon</router-link>
        <router-link to="/">Nouveautés</router-link>
        <router-link to="/">Rituels de soin</router-link>
      </ul>
        <ProductDropdown title="visages" :items="visages" v-show="categories"></ProductDropdown>
      <div class="product_gallery" v-if="!categories">
        <img
          src="../assets/navigation/produit1.jpg"
          alt=""
          class="product_image"
        />
        <img
          src="../assets/navigation/produit2.svg"
          alt=""
          class="product_image"
        />
        <img
          src="../assets/navigation/produit3.jpg"
          alt=""
          class="product_image"
        />
      </div>
    </div>
  </div>
</template>

<script>
import ProductDropdown from './ProductMenuDropdown.vue'
export default {
  name: "Dropdown",
  components: {
    ProductDropdown
  },
  data() {
    return {
      categories:false,
      visages: [
        {
          category: "Par type de produit",
          cat: [
            {
              title: "Démaquillant & nettoyant",
              link: "#",
            },
            {
              title: "Sérum",
              link: "#",
            },
            {
              title: "Crème de jour",
              link: "#",
            },
            {
              title: "Soin de nuit",
              link: "#",
            },
            {
              title: "Soin yeux & lèvres",
              link: "#",
            },
            {
              title: "Masque & gommage visage",
              link: "#",
            },
          ],
        },
        {
          category: "Par besoin",
          cat: [
            {
              title: "Hydratant",
              link: "#",
            },
            {
              title: "Nourrissant",
              link: "#",
            },
            {
              title: "Anti-âge",
              link: "#",
            },
            {
              title: "Purifiant",
              link: "#",
            },
            {
              title: "Nettoyant & exfoliant",
              link: "#",
            },
          ],
        },
        {
          category: "Par type de peau",
          cat: [
            {
              title: "Peau sensible",
              link: "#",
            },
            {
              title: "Peau mature",
              link: "#",
            },
            {
              title: "Peau très sèche",
              link: "#",
            },
            {
              title: "Peau mixte à grasse",
              link: "#",
            },
            {
              title: "Tous types de peaux",
              link: "#",
            },
          ],
        },
        {
          category: "Par gamme",
          cat: [
            {
              title: "Olive",
              link: "#",
            },
            {
              title: "Argan",
              link: "#",
            },
            {
              title: "Karité",
              link: "#",
            },
            {
              title: "Argile",
              link: "#",
            },
            {
              title: "Antipollution",
              link: "#",
            },
          ],
        },
      ],
    };
  },
  methods:{

  }
};
</script>

<style>
.menu_dropdown {
  height: 440px;
  width: 100%;
  border-top: 1px solid var(--cloudy-green);
  /* transform: translateY(-440px); */
  position: relative;
  transition: transform 0.4s ease;
}
ul {
  display: flex;
  align-items: flex-start;
  flex-direction: column;
  padding: 27px 0 157px 0;
  height: 70%;
  justify-content: space-around;
}
ul a {
  list-style: none;
  margin: 0;
  padding-right: 209px;
  position: relative;
  width: 100%;
}
.menu_dropdown a:nth-child(-n + 5)::before {
  content: "";
  position: absolute;
  height: 1px;
  left: 100px;
  background: var(--warm-grey);
  width: 8px;
  transform: rotate(45deg);
  top: 5px;
  opacity: 0;
  transition: all 0.4s ease;
}
.menu_dropdown a:nth-child(-n + 5)::after {
  content: "";
  position: absolute;
  height: 1px;
  left: 100px;
  background: var(--warm-grey);
  width: 8px;
  transform: rotate(145deg);
  top: 10px;
  opacity: 0;
  transition: all 0.4s ease;
}
.menu_dropdown a:hover:before {
  opacity: 1;
  left: 110px;
}
.menu_dropdown a:hover:after {
  opacity: 1;
  left: 110px;
}
.product_gallery {
  display: flex;
  width: 100%;
  align-items: center;
  justify-content: center;
  gap: 60px;
}
.product_image {
  object-fit: contain;
  height: 100%;
  max-height: 300px;
  max-width: 33%;
}
</style>
