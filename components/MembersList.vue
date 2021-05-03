<template>
  <ul>
    <li class="member-card" v-for="member of this.members" :key="member.name">
      <img
        :src="`https://raw.githubusercontent.com/Real-Dev-Squad/website-static/main/members/${member.username}/img.png`"
        width="180"
        height="180"
        :alt="member.first_name + ' ' + member.last_name"
      />
      <h2 class="member-name">{{ member.first_name + ' ' + member.last_name }}</h2>
      <ul class="member-links">
        <li>
          <a class="icon" :href="`//twitter.com/${member.twitter_id}`"
            ><img width="32" height="32" src="../static/twitter.png" :alt="`${member.username} twitter link`"
          /></a>
        </li>
        <li>
          <a class="icon" :href="`//github.com/${member.github_id}`"
            ><img width="32" height="32" src="../static/github.png" :alt="`${member.username} github link`"
          /></a>
        </li>
        <li>
          <a class="icon" :href="`//linkedin.com/in/linkedin_id`"
            ><img width="32" height="32" src="../static/linkedin.png" :alt="`${member.username} linkedin link`"
          /></a>
        </li>
      </ul>
    </li>
  </ul>
</template>

<script>
import MemberCard from "./MemberCard";
import $axios from "axios";
export default {
  name: "MembersList",
  data() {
    return {
      members: [],
      myName: 'raja',
    };
  },
  components: {
    // MemberCard,
  },
  methods: {
    async getMembers() {
      const response = await $axios.get(`//localhost:3004/members`);
      return {
        members: response.data
      };
    },
  },
  created() {
    const response = this.getMembers().then(response=>{
      this.members = response.members;
    });
  },
};
</script>

<style>
ul {
  list-style: none;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-content: center;
  margin: 0;
  padding: 0;
  width: 100%;
}
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