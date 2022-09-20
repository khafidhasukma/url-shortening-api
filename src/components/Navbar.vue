<template>
  <nav class="navbar navbar-expand-lg bg-white sticky-top pt-4 pb-3">
    <div class="container">
      <a class="navbar-brand" href="#">
        <img src="/assets/img/logo.svg" width="130" alt="" />
      </a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item px-2">
            <a class="nav-link active" aria-current="page" href="#">Features</a>
          </li>
          <li class="nav-item px-2">
            <a class="nav-link" href="#pricing" aria-current="page">Pricing</a>
          </li>
          <li class="nav-item px-2">
            <a class="nav-link" href="#resources" aria-current="page">Resources</a>
          </li>
        </ul>
      </div>
      <div class="d-flex gap-2">
        <button class="border-0 btn-login">Login</button>
        <button class="border-0 btn-signup rounded-pill">Sign Up</button>
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
</style>

<script>
export default {
  name: "Navbar",
};
</script>
