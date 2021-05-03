<template>
  <li class="member-card">
    <img
      src="https://raw.githubusercontent.com/Real-Dev-Squad/website-static/main/members/adnan/img.png"
      width="180"
      height="180"
      alt="Adnan Raghib"
    />
    <h2 class="member-name">{{props.member.name}}</h2>
    <ul class="member-links">
      <li>
        <a class="icon" href="//twitter.com//raghib_adnan"
          ><img width="32" height="32" src="../static/twitter.png" alt=""
        /></a>
      </li>
      <li>
        <a class="icon" href="//twitter.com//raghib_adnan"
          ><img width="32" height="32" src="../static/github.png" alt=""
        /></a>
      </li>
      <li>
        <a class="icon" href="//twitter.com//raghib_adnan"
          ><img width="32" height="32" src="../static/linkedin.png" alt=""
        /></a>
      </li>
    </ul>
  </li>
</template>

<script>
export default {
  name: 'MemberCard',
  props: {
    member: {
      name: String
    }
  }
}
</script>

<style scoped>
ul.member-links {
  list-style: none;
  display: flex;
  justify-content: center;
  align-content: center;
  margin: 0;
  padding: 0;
  width: 100%;
}
ul li.member-card {
  display: flex;
  flex-direction: column;
  border: 1px solid #f4f4f4;
  background: #fff;
  cursor: pointer;
  border-radius: 5%;
  box-shadow: 0 0 15px -7px rgb(0 0 0 / 65%);
  margin: 20px;
  padding: 20px 10px;
  width: 250px;
}
ul li img {
  border-radius: 50%;
  margin: 0 auto;
}
.member-name {
  padding: 10px;
  margin: 16px 0;
}
.icon {
  border-radius: 50%;
  margin: 4px;
  display: inline-block;
}
</style>