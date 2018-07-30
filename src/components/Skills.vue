<template>
  <div class="container">
    <div class="holder">
          <input type="text" placeholder="Enter a skill you have.." v-model="skill">
    {{ skill }}
      <ul>
        <li v-for="(data, index) in skills" :key='index'>{{data.skill}}</li>
      </ul>
      <p>These are the skills that you possess.</p>
    </div>
  </div>
</template>

<script src="https://maps.googleapis.com/maps/api/js?v=3.exp&sensor=false&libraries=places"></script>
<script>
export default {
  name: 'Skills',
  data() {
    return {
      name: 'Coursetro',
      

      skill: '',
      skills: [
        {"skill":"Vue.js"},
        {"skill":"Frontend Developer"}
      ],
      showAlert: true,
       btnState: true
    }
         
  },
  methods : {
      addSkill(){
          this.skills.push({skill: this.skill});
          this.skill = '';
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style src="../css/Skills.css" scoped>

</style>
