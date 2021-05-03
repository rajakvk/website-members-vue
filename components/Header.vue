<template>
  <div>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">Welcome</a></li>
      <li><a href="#">Events</a></li>
      <li><a href="#" class="active">Members</a></li>
      <li><a href="#">Cypto</a></li>
    </ul>
    <Logo />
    <h1 class="title">
      Real Dev Squad Members
    </h1>
  </div>
</template>

<script>
import Logo from '../components/Logo.vue'
export default {
    name: 'Header',
    components: {
        Logo,
    }
}
</script>
<style scoped>
ul {
  list-style: none;
  display: flex;
  justify-content: left;
  background-color: #1d1283;
  padding: 0;
}
ul li a {
  padding: 14px 16px;
  display: block;
  color: #fff;
  text-decoration: none;
}
ul li a:hover {
  background-color: #fff3;
}
ul li a.active {
  color: #87D870;
}
</style>