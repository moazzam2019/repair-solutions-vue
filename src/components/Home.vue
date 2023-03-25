<template>
  <div class="categories-container">
    <router-link
      class="directory-item-container"
      v-for="category in mainCategories"
      :key="category.id"
      :to="category.param"
    >
      <div
        class="background-image"
        :style="'background-image: url(' + category.imageUrl + ')'"
      />
      <div class="directory-item-body">
        <h2>{{ category.title }}</h2>
        <p>Shop Now</p>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      mainCategories: [
        {
          id: 1,
          title: "Apple",
          imageUrl: "https://i.ibb.co/Gk8hgzt/apple.png",
          param: "/apple"
        },
        {
          id: 2,
          title: "Samsung",
          imageUrl: "https://i.ibb.co/p32MGtw/samsung.webp",
          param: "/samsung"
        },
        {
          id: 3,
          title: "OnePlus",
          imageUrl: "https://i.ibb.co/VpSXFgF/oneplus.webp",
          param: "/oneplus"
        },
        {
          id: 4,
          title: "Sony",
          imageUrl: "https://i.ibb.co/RvBdgMc/sony.webp",
          param: "/sony"
        },
        {
          id: 5,
          title: "Huawei",
          imageUrl: "https://i.ibb.co/61x4R9Q/huawei.jpg",
          param: "/huawei"
        },
        {
          id: 6,
          title: "Nokia",
          imageUrl: "https://i.ibb.co/dfPNdJb/nokia.jpg",
          param: "/nokia"
        }
      ]
    };
  },
  mounted() {
    document.title = "Repair Solutions"; // set the page title
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.categories-container {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  animation: slideInFromLeft 1s ease-out 0s 1;
}

@keyframes slideInFromLeft {
  0% {
    transform: translateX(-50%);
  }
  100% {
    transform: translateX(0);
  }
}
.directory-item-container {
  min-width: 47%;
  height: 240px;
  flex: 1 1 auto;
  display: flex;
  align-items: center;
  justify-content: center;
  border: 1px solid black;
  margin: 0 7.5px 15px;
  overflow: hidden;
}

.directory-item-container:hover {
  cursor: pointer;
}

.directory-item-container:hover .background-image {
  transform: scale(1.1);
  transition: transform 3s cubic-bezier(0.25, 0.45, 0.45, 0.95);
}

.directory-item-container:hover .directory-item-body {
  opacity: 1;
  display: flex;
}

.directory-item-container.large {
  height: 380px;
}

.directory-item-container:first-child {
  margin-right: 7.5px;
}

.directory-item-container:last-child {
  margin-left: 7.5px;
}

.directory-item-container .background-image {
  width: 100%;
  height: 100%;
  background-size: cover;
  background-position: center;
}

.directory-item-container .directory-item-body {
  height: 90px;
  padding: 0 25px;
  display: none;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  border: 1px solid black;
  background-color: white;
  opacity: 0.8;
  position: absolute;
}

@media (max-width: 900px) {
  .directory-item-container .directory-item-body {
    display: flex;
  }
}

.directory-item-container .directory-item-body h2 {
  font-weight: bold;
  padding-top: 10px;
  margin: 0 6px 0;
  font-size: 30px;
  color: #4a4a4a;
}

.directory-item-container .directory-item-body h2:hover {
  color: rgb(57, 99, 198);
}

.directory-item-container .directory-item-body p {
  font-weight: lighter;
  font-size: 20px;
}
</style>
