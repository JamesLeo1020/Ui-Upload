<template>
<div class="side-bar">
    <div class="area"></div><nav class="main-menu">
        <ul>
            <li>
                <a href="#">
                    <i class="uil uil-estate"></i>                        
                    <span class="nav-text">
                    <NuxtLink to="/home">Home</NuxtLink>
                    </span>
                </a>
                
            </li>
            <li>
                <a href="#">
                    <i class="uil uil-file-alt"></i>                       
                    <span class="nav-text">
                    <NuxtLink to="/Draft">Draft</NuxtLink>
                    </span>
                </a>
                
            </li>
            <li>
                <a href="#">
                    <i class="uil uil-book-medical"></i>                        
                    <span class="nav-text">
                    <NuxtLink to="/CreatePost">Create Post</NuxtLink>
                    </span>
                </a>
                
            </li>
            <li>
                <a href="#">
                    <i class="uil uil-setting"></i>                        
                    <span class="nav-text">
                    <NuxtLink to="/Setting">Setting</NuxtLink>
                    </span>
                </a>
                
            </li>

        </ul>

        <ul class="logout">
            <li>
                <a href="#">
                    <i class="uil uil-power"></i>                        
                    <span class="nav-text">
                    <NuxtLink to="/home">Log Out</NuxtLink>
                    </span>
                </a>
                
            </li>
        </ul>
    </nav>
</div>
</template>

<script>
export default {

}
</script>

<style>

</style>