<template>
  <form>
    <label>Email:</label>
    <input type="email" v-model="email" required />

    <label>Password:</label>
    <input type="password" v-model="password" required />

    <label>Role:</label>
    <select v-model="role">
      <option value="developer">Web Developer</option>
      <option value="designer">Web Designer</option>
      <option value="tester">Web Tester</option>
    </select>

    <div class="terms">
      <label>Accept terms and conditions</label>
      <input type="checkbox" v-model="terms" required />
    </div>

    <label>Counties to Relocate </label>
    <div>
      <label>Kisumu</label>
      <input type="checkbox" value="kisumu" v-model="counties" />
    </div>
    <div>
      <label>Nairobi</label>
      <input type="checkbox" value="nairobi" v-model="counties" />
    </div>
    <div>
      <label>Mombasa</label>
      <input type="checkbox" value="mombasa" v-model="counties" />
    </div>
  </form>

  <p>Email: {{ email }}</p>
  <p>Password: {{ password }}</p>
  <p>Your role: {{ role }}</p>
  <p>Terms accepted: {{ terms }}</p>
  <p>Counties: {{ counties }}</p>
</template>

<script>
export default {
  name: "SignupForm",
  data() {
    return {
      email: "",
      password: "",
      role: "developer",
      terms: false,
      counties: [],
    };
  },
};
</script>

<style>
form {
  max-width: 420px;
  margin: 30px auto;
  background: white;
  text-align: left;
  padding: 40px;
  border-radius: 10px;
}
label {
  color: #aaa;
  display: inline-block;
  margin: 25px 0 15px;
  font-size: 0.6em;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: bold;
}
input,
select {
  display: block;
  padding: 10px 6px;
  width: 100%;
  box-sizing: border-box;
  border: none;
  border-bottom: 1px solid #ddd;
  color: #555;
}
</style>