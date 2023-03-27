<template>
  <div class="parent-element">
    <div class="footer-container">
      <div
        class="container-lg"
        style="display: flex; justify-content: space-evenly; margin-top: 30px;"
      >
        <div class="col-md-3">
          <img
            src="../assets/repair-solutions-logo.png"
            style="width: 70%;"
            alt="Repair Solutions logo"
          />
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Alias sequi
            aliquid sint optio perspiciatis! Cumque eos repellat praesentium
            magnam in?
          </p>
        </div>
        <div class="col-md-3">
          <h2>Contact us</h2>
          <ul class="list-one">
            <li><span>+45-71723434</span></li>
            <li><span>info@repairsolutions.dk</span></li>
            <li>
              <i class="sp-map-marker"></i>
              <span>777/ab Rampura Bonosri</span>
              <span>North DC-3050 USA.</span>
            </li>
          </ul>
        </div>
        <div class="col-md-3">
          <h2>Menu</h2>
          <ul>
            <li style="text-decoration:none">
              <router-link to="/sign-in">Account</router-link>
            </li>
            <li><router-link to="/sign-in">Log in</router-link></li>
            <li><router-link to="/sign-in">Register</router-link></li>
            <li><router-link to="/shop">Shop</router-link></li>
            <li><router-link to="/checkout">Checkout</router-link></li>
          </ul>
        </div>
        <div class="col-md-3">
          <h2>Subscribe to news</h2>
          <form class="f-subscribe-form">
            <span>
              <input
                placeholder="Your e-mail"
                type="text"
                style="
              margin-right: 5px;
              box-sizing: border-box;
              height: 35px;
              width: 79%;
            "
              />
            </span>
            <button style="background-color: #333333;">
              <font-awesome-icon icon="fas fa-arrow-right" color="white" />
            </button>
          </form>
          <p>
            Enter your email address if you want to receive our newsletter.
            Subscribe now!
          </p>
        </div>
      </div>
    </div>

    <div class="container-fluid bg-dark text-light copyright">
      <div class="container-lg pt-3">
        <div class="row">
          <div class="col-lg-6">
            <p>
              Copyright &copy;
              <router-link to="/" class="text-light">
                Repair Solutions
              </router-link>
              All rights reserved
            </p>
          </div>
          <div class="col-lg-6">
            <span>
              <a href="#" class="text-light mx-2">
                <font-awesome-icon icon="fa-brands fa-facebook-f" />
              </a>
              <a href="#" class="text-light mx-2">
                <font-awesome-icon icon="fa-brands fa-twitter" />
              </a>
              <a href="#" class="text-light mx-2">
                <font-awesome-icon icon="fa-brands fa-linkedin-in" />
              </a>
              <a href="#" class="text-light mx-2">
                <font-awesome-icon icon="fa-brands fa-instagram" />
              </a>
            </span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "footerComponent"
};
</script>

<style scoped>
.footer-container {
  margin-top: 80px;
  height: 300px;
  background-color: aliceblue;
  height: fit-content;
  margin-bottom: -600px;
  display: flex;
  justify-content: space-evenly;
  text-align: center;
}

.copyright {
  background-color: #333333;
  color: white;
  padding-bottom: 2px;
  text-align: center;
  margin-top: 600px;
}

.copyright a:hover {
  background-color: #4e4a4a;
  color: white;
}

.copyright .site-name {
  color: white;
  text-decoration: underline;
}

h2 {
  margin-top: 0;
}

ul {
  padding: 5px 0 15px 8px;
}

ul.list-one {
  padding-right: 20px;
}

ul li {
  list-style: none;
  padding-bottom: 4px;
}

ul li a {
  font-weight: 600;
  color: #333333;
}

ul li a:hover {
  color: rgb(94, 94, 94);
}

.footer-menu {
  display: block;
}

@media (max-width: 1200px) and (min-width: 900px) {
  .footer-menu {
    display: none;
  }
}
</style>
