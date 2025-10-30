<template>
  <section class="login-page">
    <div class="login-card">
      <h2 class="title"></h2>

      <form @submit.prevent="onSubmit" class="login-form" novalidate>
        <label for="email">Email</label>
        <input id="email" v-model="email" type="email" placeholder="you@example.com" required />

        <label for="password">Password</label>
        <input id="password" v-model="password" type="password" placeholder="••••••••" required />

        <div class="actions">
          <button type="submit" class="btn btn-login">Login</button>
          <router-link to="/signup" class="btn btn-signup">Sign Up</router-link>
        </div>

        <p class="note" v-if="error">{{ error }}</p>
      </form>
    </div>
  </section>

</template>

<script>
export default {
  name: "LoginView",
  data() {
    return {
      email: "",
      password: "",
      error: ""
    };
  },
  methods: {
    onSubmit() {
      this.error = "";
      if (!this.email || !this.password) {
        this.error = "Please enter email and password.";
        return;
      }
      console.log("Login attempt:", { email: this.email });
      this.error = "This is a demo form — hook up your auth logic.";
    }
  }
};
</script>

<style scoped>

.login-page {
  min-height: calc(100vh - 100px);
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 40px 16px;
  background-color: #e9ffff;
}

.login-card {
  width: 100%;
  max-width: 420px;
  background: #fff;
  border-radius: 12px;
  padding: 28px;
  box-shadow: 0 8px 28px rgba(49, 77, 13, 0.08);
  border: 1px solid rgba(49, 77, 13, 0.06);
}

.title {
  margin: 0 0 18px;
  font-family: Berlin Sans FB, Helvetica, Arial, sans-serif;
  color: #314D0D;
  text-align: center;
  font-size: 1.4rem;
}

.login-form {
  display: grid;
  gap: 12px;
}

.login-form label {
  font-size: 0.85rem;
  color: #2c3e50;
  text-align: left;
}

.login-form input {
  width: 100%;
  padding: 10px 12px;
  border: 1.5px solid #dbe7cf;
  border-radius: 8px;
  font-size: 0.95rem;
  outline: none;
  transition: border-color .12s ease, box-shadow .12s ease;
}

.login-form input:focus {
  border-color: #314D0D;
  box-shadow: 0 4px 12px rgba(49,77,13,0.06);
}


.actions {
  display: flex;
  gap: 12px;
  margin-top: 6px;
  justify-content: center;
  align-items: center;
}

.btn-login {
  background-color: #314D0D;
  color: #fff;
  border: 2px solid #1a3a0d;
  padding: 12px 26px;
  font-weight: 700;
  font-size: 1.05rem;
  border-radius: 8px;
  cursor: pointer;
  transition: transform .15s ease, background-color .12s ease, border-color .12s ease;
}

.btn-login:hover {
  transform: translateY(-2px);
  background-color: #27400a;
  border-color: #122707;
}

.btn-signup {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  min-width: 120px;
  padding: 10px 18px;
  color: #314D0D;
  background: transparent;
  border: 2px solid #314D0D;
  border-radius: 8px;
  font-weight: 700;
  text-decoration: none;
  font-size: 1rem;
  transition: transform .15s ease, background-color .12s ease, color .12s ease;
}

.btn-signup:hover {
  transform: translateY(-2px);
  background: rgba(49,77,13,0.06);
}

.note {
  margin-top: 10px;
  color: #b33131;
  font-size: 0.9rem;
  text-align: center;
}
</style>