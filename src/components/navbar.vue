<template>
  <nav class="navbar navbar-expand-lg navbar-light our-nav row col-12">
    <a class="navbar-brand app-logo" href="#">
      <router-link to="/">
        <img src="../../public/logo.svg" />
      </router-link>
    </a>
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarSupportedContent"
      aria-controls="navbarSupportedContent"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>

    <div class="collapse navbar-collapse nav-utilitiess nav-utilities" id="navbarSupportedContent">
      <ul class="navbar-nav col-12">
        <li class="nav-item mx-1">
          <a class="nav-link features" href="#">Features</a>
        </li>

        <li class="nav-item mx-1">
          <a class="nav-link p" href="#">Pricing</a>
        </li>
        <li class="nav-item mx-1">
          <a class="nav-link" href="#">Resources</a>
        </li>
      </ul>

      <div class="col-12 test">
        <button class="btn btn-light signup-btn mx-2">Login</button>
        <button class="btn btn-s login-btn mx-2">Sign Up</button>
      </div>
    </div>
  </nav>
</template>

<style scoped>
/* Navbar CSS */
.test {
  margin-left: 15px;
}

nav {
  margin-bottom: 20px;
}
.btn-s {
  background: hsl(180, 66%, 49%);
  color: white;
}
.short {
  text-decoration: none;
  color: black;
  font-weight: bolder;
}
.app-logo {
  margin-left: 7vw;
}
.btn {
  margin-right: 7vw;
}
.nav-link {
  text-decoration: none;
}
.nav-utilities {
  margin-right: 40vw;
}

.nav-item .nav-link {
  font-size: 16px;
  font-weight: bold;
  color: Gray hsl(0, 0%, 75%) !important;
}

.login-btn {
  font-size: 16px;
  width: 6vw;
  border-radius: 20px;
}
.signup-btn {
  font-size: 16px;
  width: 6vw;
  border-style: none;
  background: white !important;
}

@media screen and (max-width: 700px) {
  .login-btn,
  .signup-btn {
    width: 20vw;
  }
  .features {
    position: relative;
    right: 5px;
  }
  .p {
    margin-right: 17px;
  }
  .nav-utilitiess {
    margin-right: 400px !important;
    position: relative;
    right: 55px;
  }
  .test {
    display: flex;
    flex-direction: row;
    position: relative;
    left: 15px;
  }
  .app-logo img {
    width: 20vw;
  }
  .app-logo {
    margin-left: 6vw;
  }
}
</style>