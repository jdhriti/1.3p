<script setup>
import { RouterLink } from 'vue-router';
</script>

<template>
    <header>
        <nav class="container">
            <div class="brand">
                <img src="https://th.bing.com/th/id/R.57afa497c78638b6f5ec006c8655731a?rik=BkJNag5oufZyBw&riu=http%3a%2f%2f1.bp.blogspot.com%2f_UDtr8B8eYnA%2fS8p8MHKkWBI%2fAAAAAAAAATg%2fx0w3Z-wexNM%2fs1600%2fChess%2bQueen.jpg&ehk=PR0%2b14IASmmB0UeJ7XdrkTvrKgRRWLu1Fgsm7f5kuGY%3d&risl=&pid=ImgRaw&r=0" alt="logo">
                <h1>Queen's Gambit </h1>
            </div>
            <ul class="nav-routes">
                <RouterLink to= "/">Home </RouterLink>
                <RouterLink to= "/about">About</RouterLink>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
header {
    
    font-family: sans-serif;
    background-color: rgb(255, 255, 255);    
    border-color: #0a9343;
    nav {
        display: flex;
        align-items: center;
        padding: 20px 12px;
        .brand {
            display:  flex;
            align-items : center;
            gap: 7px;

            img {
                max-width: 50px;
            }

            h1 {
                font-size: 30px;
                color: #000000;
                text-align: center;
            }
        }

        .nav.routes {
            display: flex;
            flex: 1.5;
            list-style: none;
            gap: 20px; /* Spacing between links */
            margin: 0;
            }

            .nav-routes a {
            text-decoration: none;
            color: #484545; /* Link text color */
            font-weight: bold;
            font-size: 1rem;
            transition: color 0.3s ease; /* Smooth color transition on hover */


                }

            .nav-routes {
                margin-left: auto; /* Pushes navigation to the right */
            }

            .nav-routes a:hover {
                color: #0a9343; /* Change the link color on hover */
            }

            }

    }

</style>