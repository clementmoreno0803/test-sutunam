<template>

    <div id="nav">
      <div class="up">
        <div class="container navigation_up">
          <div class="navigation">
            <router-link to="/">Notre histoire</router-link>
            <router-link to="/about">Nos engagements</router-link>
            <router-link to="/about">Notre charte</router-link>
            <!-- <router-link to="/about">Notre actualité</router-link> -->
          </div>
          <div class="service_et_reseaux">
            <img
              src="../assets/navigation/phone.svg"
              alt=""
              class="phone"
            />
            <a href="#">Service client au 04 90 56 91 20</a>
            <a href="#"
              ><img
                src="../assets/navigation/facebook.svg"
                alt="Facebook_icon"
                class="reseaux_sociaux"
            /></a>
            <a href=""
              ><img
                src="../assets/navigation/instagram.svg"
                alt="Instagram_icon"
                class="reseaux_sociaux"
                id="insta"
            /></a>
            <div class="trad">
              <img
                src="../assets/navigation/drapeauFR.svg"
                alt=""
                id="drapeau"
              />
              <h6>Fr</h6>
              <img src="../assets/navigation/arrow.svg" alt="" id="arrow" />
            </div>
          </div>
        </div>
      </div>
      <!-- <img
      src="../assets/navigation/edge_arrow.svg"
      alt=""
      class="left_arrow"
    /> -->
      <!-- <img
      src="../assets/navigation/edge_arrow.svg"
      alt=""
      class="right_arrow"
    /> -->
      <div class="down">
        <div class="nav_down">
          <img
            src="../assets/navigation/menu_icon.svg"
            alt=""
            id="produit"
          />
          <h6>Nos produits</h6>
        </div>
        <div class="nav_down" id="center_left">
          <img src="../assets/navigation/loupe.svg" alt="" id="loupe" />
          <h6>Rechercher...</h6>
        </div>
        <img src="../assets/navigation/logo.svg" alt="" class="main_logo" />
        <div class="nav_down" id="center_right">
          <h6>Me connecter</h6>
          <img src="../assets/navigation/compte.svg" alt="" id="compte" />
        </div>
        <div class="nav_down">
          <h6>Mon panier</h6>
          <img src="../assets/navigation/panier.svg" alt="" id="panier" />
        </div>
      </div>
    </div>
</template>

<script>
export default {
name:'Nav'
}
</script>

<style>

/* ------navigation/UP----- */
.up {
  border-bottom: 1px solid var(--cloudy-green);
}
.navigation_up {
  display: flex;
  align-items: center;
  height: 50px;
  justify-content: space-between;
  position: relative;
}
.navigation a {
  margin-right: 17px;
}
.service_et_reseaux {
  display: flex;
  align-items: center;
  list-style: none;
}
.service_et_reseaux a {
  display: flex;
  align-items: center;
}
.phone {
  width: 8.4px;
  height: 12.4px;
  margin-right: 10px;
}
.reseaux_sociaux {
  width: 16px;
  height: 16px;
  margin: 0 30px 0 31px;
}
#insta {
  margin-left: -10px;
}
#drapeau {
  height: 10px;
  width: 15px;
  margin-right: 5.6px;
}
.trad {
  display: flex;
  align-items: center;
  cursor: pointer;
}
#arrow {
  margin-left: 10.9px;
}
/* ------navigation/MIDDLE----- */
.main_logo {
  position: relative;
  bottom: 18.6px;
  width: 92.4px;
  height: 110px;
  padding: 0 33.8px 11.4px 33.8px;
  background: var(--white);
}
/* .left_arrow {
  position: absolute;
  top: 44px;
  z-index: 99;
  transform: rotate(180deg);
}
.right_arrow {
  position: absolute;
  top: 84px;
} */
/* ---------navigation/DOWN------ */
.down {
  display: flex;
  padding: 0 100px 0 80px;
  justify-content: space-between;
  align-items: center;
  height: 90px;
}
.nav_down {
  display: flex;
  align-items: center;
  padding: 0 29px;
  cursor: pointer;
  position: relative;
}
.nav_down:first-child {
  padding: 0 29px 0 0;
}
.nav_down:last-child {
  padding: 0 0 0 29px;
}
.nav_down::after {
  content: "";
  position: absolute;
  width: 0;
  bottom: -13px;
  left: 50%;
  height: 10px;
  background: var(--cloudy-green);
  transition: width 0.3s ease 0s, left 0.3s ease 0s;
}
.nav_down:hover:after {
  width: 100%;
  left: 0;
}
#center_left {
  margin-right: 180.8px;
}
#center_right {
  margin-left: 168.7px;
}
#produit {
  margin-right: 20px;
}
#loupe {
  margin-right: 19px;
}
#compte {
  margin-left: 19px;
}
#panier {
  margin-left: 19px;
}

</style>
