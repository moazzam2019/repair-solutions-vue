<template>
  <div class="header-container">
    <!-- Top Header -->
    <div class="top-header">
      <div class="container-lg header-top-main">
        <div class="row grid-container">
          <div class="col-lg-2 col-md-2 header-top-item">
            <a href="tel:+4571723434">
              <div
                class="d-flex align-items-center flex-wrap text-white"
                style="font-size: 14px;"
              >
                <i class="fas fa-phone me-2"></i>
                <span>+45-71723434</span>
              </div>
            </a>
          </div>
          <div class="col-lg-2 col-md-3 header-top-item">
            <a href="mailto:info@repairsolutions.dk">
              <div
                class="d-flex align-items-center flex-wrap text-white"
                style="font-size: 14px;"
              >
                <i class="fas fa-envelope me-2"></i>
                <span>info@repairsolutions.dk</span>
              </div>
            </a>
          </div>
          <div class="col-lg-3 col-md-2 header-top-item text-center">
            <!-- Assuming `currentUser` is a Vue prop -->
            <account-button
              v-if="currentUser"
              :label="currentUser.name"
              :button-one="'Update Data'"
              :link-one="'/update-data'"
              :button-two="'Change Password'"
              :link-two="'/update-password'"
            ></account-button>
          </div>
          <div class="col-lg-2 col-md-2 header-top-item">
            <!-- Assuming `currentUser` and `currentUser.role` are Vue props -->
            <account-button
              v-if="currentUser && currentUser.role === 'admin'"
              label="Admin Panel"
              button-one="Add phone"
              button-two="Update Phone"
              button-three="Delete Phone"
              link-one="/add-product"
              link-two="/shop/update-product"
              link-three="/shop/delete-product"
            ></account-button>
          </div>
          <div class="col-lg-3 col-md-3 header-top-item">
            <div style="margin-top: -8px">
              <input type="text" class="form-control" placeholder="Search..." />
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Bottom Header -->
    <div class="bottom-header">
      <div class="container-lg header-bottom-main">
        <div class="row grid-container">
          <div class="col-lg-2 header-bottom-item">
            <router-link to="/" class="logo-container">
              <img
                src="../assets/repair-solutions-logoo.png"
                alt="Repair Solutions"
                class="logo"
              />
            </router-link>
          </div>
          <div class="col-lg-3 col-md-2 header-bottom-item"></div>
          <div
            class="col-lg-5 col-md-5 header-bottom-item"
            style="margin-top: 12px"
          >
            <router-link to="/shop" style="margin-right: 10px">
              <button class="btn btn-primary">
                SHOP
              </button></router-link
            >
            <router-link to="/contact" style="margin-right: 10px">
              <button class="btn btn-primary">CONTACT</button></router-link
            >
            <router-link to="/sign-in" style="margin-right: 10px">
              <button class="btn btn-primary">SIGN IN</button></router-link
            >
          </div>
          <div class="col-lg-2 col-md-2 header-bottom-item">
            <font-awesome-icon
              :icon="['fas', 'cart-shopping']"
              style="color: white;"
              class="fa-2x pt-3 icon"
            />
            <cart-dropdown v-if="isCartOpen"></cart-dropdown>
          </div>
        </div>
      </div>
    </div></div
></template>

<script>
export default {
  name: "headerComponent"
};
</script>

<style scoped>
.icon:hover {
  cursor: pointer;
}
.header-container {
  background-color: #333333;
  height: 150px;
  margin-bottom: 25px;
}
.grid-container {
  height: 100%;
  width: 100%;
}

.top-header {
  height: 30%;
  border-bottom: 1px solid #666;
}

.header-top-main {
  height: 100%;
  border-right: 1px solid #666;
}

.header-top-item {
  border-left: 1px solid #666;
  padding-top: 10px;
  padding-left: 10px;

  color: white;
}

.bottom-header {
  height: 70%;
  padding-top: 20px;
}

.logo {
  height: 60px;
  padding: auto;
}
</style>
