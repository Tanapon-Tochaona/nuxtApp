<template>
    <div>
                <nav class="navbar navbar-expand-lg bg-body-tertiary">
        <div class="container-fluid">
            <a class="navbar-brand" href="#">Navbar</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="/">Home</a>
                </li>
                <li class="nav-item">
                <a class="nav-link" href="/about">about us</a>
                </li>
                <li class="nav-item">
                <a class="nav-link" href="/limitmessage">Limit Message</a>
                </li>
                <li class="nav-item">
                <a class="nav-link" href="/previewImage">Preview Image</a>
                </li>
            </ul>
            <form class="d-flex" role="search">
                <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
                <button class="btn btn-outline-success" type="submit">Search</button>
            </form>
            </div>
        </div>
        </nav>
        <footer class="bg-dark  text-white " style="text-align: center;">
            <div class="container w-100" >
            <h5 style="width: 100%;"> copyright © 2023 Tanapon</h5>
            </div>
        </footer>
    </div>
    <slot />
</template>
<script>

</script>

<style>
a {
  text-decoration: none;
  color: white;
}


footer {
  position: fixed;
  bottom: 0;
  width: 100%;
}

</style>