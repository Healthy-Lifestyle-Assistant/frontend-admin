<template>
    <nav class="navbar fixed-top navbar-expand-lg bg-light mb-5" data-bs-theme="light">

        <div class="container-fluid">
            <!-- Logo -->
            <router-link to="/" class="navbar-brand me-5">
                <img src="" alt="" class="d-inline-block align-text-top logo-custom-size">
                Healthy Lifestyle - Admin
            </router-link>

            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
                aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>

            <!-- Menu -->
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">

                    <!-- Users -->
                    <li class="nav-item me-3">
                        <router-link to="/" :class="{ 'nav-link': true, 'active': false }">Users</router-link>
                    </li>

                    <!-- Workouts -->
                    <li class="nav-item me-3">
                        <router-link to="/" :class="{ 'nav-link': true, 'active': false }">Workouts</router-link>
                    </li>

                    <!-- Exercises -->
                    <li class="nav-item me-3">
                        <router-link to="/" :class="{ 'nav-link': true, 'active': false }">Exercises</router-link>
                    </li>

                    <!-- Media -->
                    <li class="nav-item me-3">
                        <router-link to="/" :class="{ 'nav-link': true, 'active': false }">Media</router-link>
                    </li>

                    <!-- Body Parts -->
                    <li class="nav-item me-3">
                        <router-link to="/" :class="{ 'nav-link': true, 'active': false }">Body Parts</router-link>
                    </li>

                </ul>

                <!-- Login -->
                <div v-if="isLogged" class="d-flex align-items-center">
                    <!-- <div class="me-2">isLogged: {{ isLogged }}</div>
                    <div class="me-2">curUrl: {{ getCurrentUrl }}</div>
                    <div class="me-2">prevUrl: {{ getPreviousUrl }}</div> -->

                    <router-link to="/" class="btn btn-outline-secondary me-2" role="button">Settings</router-link>
                    <router-link to="/" class="btn btn-outline-secondary me-2" role="button">Logout</router-link>
                </div>

                <div v-else class="d-flex align-items-center">
                    <!-- <div class="me-2">isLogged: {{ isLogged }} </div>
                    <div class="me-2">curUrl: {{ getCurrentUrl }}</div>
                    <div class="me-2">prevUrl: {{ getPreviousUrl }}</div> -->

                    <router-link to="/" class="btn btn-outline-secondary me-2" role="button">Login</router-link>
                </div>

            </div>

        </div>
    </nav>
</template>

<script>
export default {
    name: "NavbarComponent"
}
</script>
