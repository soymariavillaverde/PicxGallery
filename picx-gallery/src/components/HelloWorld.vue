<template>
  <div class="hello">
    <section class="text-center text-lg-start">
    <!-- Jumbotron -->
      <div class="container py-4">
        <div class="row g-0 align-items-center">
          <div class="col-lg-6 mb-5 mb-lg-0">
            <div class="card cascading-right" style="
                background: hsla(0, 0%, 100%, 0.55);
                backdrop-filter: blur(30px);
                ">
              <div class="card-body p-5 shadow-5 text-center">
                <h2 class="fw-bold mb-5">My image gallery</h2>
                <form v-on:submit.prevent="login">
                  <!-- Email input -->
                  <div class="form-outline mb-4">
                    <input type="email" id="userEmail" class="form-control" placeholder="Email adress" v-model="userEmail"/>
                    <!-- <label class="form-label" for="userEmail">Email address</label> -->
                  </div>

                  <!-- Password input -->
                  <div class="form-outline mb-4">
                    <input type="password" id="userPassword" class="form-control" placeholder="Password" v-model="userPassword"/>
                    <!-- <label class="form-label" for="form3Example4">Password</label> -->
                  </div>

                  <!-- Submit button -->
                  <button type="submit" class="btn btn-primary btn-block mb-4">
                    Sign up
                  </button>
                </form>
              </div>
            </div>
          </div>

          <div class="col-lg-6 mb-5 mb-lg-0">
            <img src="@/assets/background-app.jpeg" class="w-100 rounded-4 shadow-4"
              alt="" />
          </div>
        </div>
      </div>
    <!-- Jumbotron -->
  </section>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data: function() {
    return {
      userEmail: "",
      userPassword: "",
      loginError: false,
      errorMsg: "",
    }
  },
  methods: {
    login() {
      console.log(this.userPassword);
    }
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

  <style>
    .cascading-right {
      margin-right: -50px;
    }

    @media (max-width: 991.98px) {
      .cascading-right {
        margin-right: 0;
      }
    }

    .hello{
      background-color: rgba(245, 167, 179, 0.3);
    }
  </style>
