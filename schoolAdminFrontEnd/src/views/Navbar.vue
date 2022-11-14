<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <a class="navbar-brand" href="#">School Admin Website</a>
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarNavDropdown"
      aria-controls="navbarNavDropdown"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavDropdown">
      <ul class="navbar-nav">
        <li class="nav-item active">
          <a class="nav-link" href="#"><RouterLink to="/">Home</RouterLink></a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#"
            ><RouterLink to="/about">About</RouterLink></a
          >
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#"
            ><RouterLink to="/students">Students</RouterLink></a
          >
        </li>
      </ul>
    </div>
  </nav>
</template>

<script></script>
