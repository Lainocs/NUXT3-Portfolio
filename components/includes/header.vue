<template>
    <div class="header">
        <div class="header-title">
            <h2>Nicolas de Garrigues</h2>
        </div>
        <nav class="header-nav">
            <ul>
                <li><a href="#">About</a></li>
                <li><a href="#">Projects</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    </div>
</template>
<script>
    export default {
        name: 'includes-header'
    }
</script>

<style>
    .header {
        padding: 50px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        text-transform: uppercase;
    }

    .header-title {
        font-size: 1.5em;
        font-weight: bold;
    }

    .header-nav ul {
        list-style: none;
        gap: 100px;
        display: flex;
        justify-content: space-around;
    }
    a {
        color: #fff;
        text-transform: uppercase;
        text-decoration: none;
        letter-spacing: 0.15em;
        
        display: inline-block;
        padding: 15px 20px;
        position: relative;
    }
    a:after {    
        background: none repeat scroll 0 0 transparent;
        bottom: 0;
        content: "";
        display: block;
        height: 2px;
        left: 50%;
        position: absolute;
        background: #fff;
        transition: width 0.3s ease 0s, left 0.3s ease 0s;
        width: 0;
    }
    a:hover:after { 
        width: 100%; 
        left: 0; 
    }
</style>