<template>
  <div class="container">
    <Header />
    <MembersList />
    <Footer />
  </div>
</template>

<script>
import Header from '../components/Header'
import MembersList from '../components/MembersList'
import Footer from '../components/Footer'
export default {
  components: {
    Header,
    MembersList,
    Footer,
  }
}
</script>

<style scope>
.container {
  text-align: center;
}
</style>
