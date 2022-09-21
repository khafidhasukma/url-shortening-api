<template>
  <nav class="navbar navbar-expand-lg bg-white sticky-top pt-4 pb-3 text-center text-md-start">
    <div class="container">
      <a class="navbar-brand" href="#">
        <img src="/assets/img/logo.svg" class="logo-img" width="130" alt="" />
      </a>
      <button class="navbar-toggler p-1" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav me-auto">
          <li class="nav-item px-2 mb-2 mb-md-0">
            <a class="nav-link active" aria-current="page" href="#">Features</a>
          </li>
          <li class="nav-item px-2 mb-2 mb-md-0">
            <a class="nav-link" href="#pricing" aria-current="page">Pricing</a>
          </li>
          <li class="nav-item px-2 mb-2 mb-md-0">
            <a class="nav-link" href="#resources" aria-current="page">Resources</a>
          </li>
        </ul>
        <hr />
        <div class="d-flex flex-column flex-md-row justify-content-center align-items-center gap-2">
          <button class="border-0 btn-login">Login</button>
          <button class="border-0 btn-signup rounded-pill">Sign Up</button>
        </div>
      </div>
    </div>
  </nav>
</template>

<style scoped>
.nav-link,
.btn-login {
  font-weight: 700 !important;
  color: var(--gray) !important;
}
.nav-link,
.btn-login,
.btn-signup {
  font-size: 1rem !important;
}
.btn-signup {
  background: var(--cyan) !important;
  color: white;
}
button {
  padding: 0.75rem 1.75rem;
  font-weight: 700 !important;
}
.btn-login {
  background: none;
}
.btn-signup:hover {
  background: var(--cyan2) !important;
}
.nav-link:focus,
.nav-link:active,
.btn-login:focus,
.nav-link:hover,
.nav-link:hover,
.btn-login:hover {
  color: black !important;
}
.navbar-toggler {
  border: none !important;
}
.navbar-toggler:focus {
  box-shadow: none !important;
}

@media only screen and (max-width: 991.98px) {
  .nav-link,
  .btn-login {
    color: white !important;
  }
  .navbar-collapse {
    background: var(--very-dark-violet);
    padding: 2rem 1rem;
    border-radius: 12px;
    margin-top: 1rem;
  }

  hr {
    border-top: 1px solid white !important;
  }
  .navbar > .container,
  .navbar > .container-fluid,
  .navbar > .container-lg,
  .navbar > .container-md,
  .navbar > .container-sm,
  .navbar > .container-xl,
  .navbar > .container-xxl {
    align-items: flex-start !important;
  }
  .logo-img {
    width: 100px;
  }
  .nav-link:focus,
  .nav-link:active,
  .btn-login:focus,
  .nav-link:hover,
  .nav-link:hover,
  .btn-login:hover {
    color: var(--cyan) !important;
  }
}
@media only screen and (max-width: 767.98px) {
  .btn-signup {
    width: 100%;
  }
}
</style>

<script>
export default {
  name: "Navbar",
};
</script>
