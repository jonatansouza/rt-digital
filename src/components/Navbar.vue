<template lang="html">
<div id="navbar">
<nav id="sidebar-wrapper" v-bind:class="{active : menuActive}">
    <ul class="sidebar-nav">
        <a id="menu-close" href="#" @click="toggleClass()" class="btn btn-light btn-lg pull-right toggle"><i class="fa fa-times"></i></a>
        <li class="sidebar-brand">
            <a href="#">Start Bootstrap</a>
        </li>
        <li>
            <a href="#">Home</a>
        </li>
        <li>
            <a href="#">About</a>
        </li>
        <li>
            <a href="#">Services</a>
        </li>
        <li>
            <a href="#">Portfolio</a>
        </li>
        <li>
            <a href="#">Contact</a>
        </li>
    </ul>
</nav>
<a id="menu-toggle"  @click="toggleClass()" href="#" class="btn btn-dark btn-lg toggle"><i class="fa fa-bars"></i></a>
</div>
</template>

<script>
export default {
  data () {
    return {
      menuActive: false
    }
  },
  methods: {
    toggleClass: function () {
      this.menuActive = !this.menuActive
    }
  }
}
</script>

<style scoped>

/* Side Menu */
#sidebar-wrapper {
  z-index: 1000;
  position: fixed;
  top: 0;
  right: 0;
  width: 250px;
  height: 100%;
  transform: translateX(250px);
  overflow-y: auto;
  background: #222;
  -webkit-transition: all 0.4s ease 0s;
  -moz-transition: all 0.4s ease 0s;
  -ms-transition: all 0.4s ease 0s;
  -o-transition: all 0.4s ease 0s;
  transition: all 0.4s ease 0s;
}
.sidebar-nav {
  position: absolute;
  top: 0;
  width: 250px;
  margin: 0;
  padding: 0;
  list-style: none;
}
.sidebar-nav li {
  text-indent: 20px;
  line-height: 40px;
}
.sidebar-nav li a {
  display: block;
  text-decoration: none;
  color: #999;
}
.sidebar-nav li a:hover {
  text-decoration: none;
  color: #fff;
  background: rgba(255, 255, 255, 0.2);
}
.sidebar-nav li a:active,
.sidebar-nav li a:focus {
  text-decoration: none;
}
.sidebar-nav > .sidebar-brand {
  height: 55px;
  font-size: 18px;
  line-height: 55px;
}
.sidebar-nav > .sidebar-brand a {
  color: #999;
}
.sidebar-nav > .sidebar-brand a:hover {
  color: #fff;
  background: none;
}
#menu-toggle {
  z-index: 1;
  position: fixed;
  top: 0;
  right: 0;
}
#sidebar-wrapper.active {
  right: 250px;
  width: 250px;
  -webkit-transition: all 0.4s ease 0s;
  -moz-transition: all 0.4s ease 0s;
  -ms-transition: all 0.4s ease 0s;
  -o-transition: all 0.4s ease 0s;
  transition: all 0.4s ease 0s;
}
.toggle {
  margin: 5px 5px 0 0;
}


</style>
