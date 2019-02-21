<template>
    <nav class="navbar navbar-default">
        <div class="navbar-header">
            <router-link class="navbar-brand" to="/"> Stock Trader </router-link>
        </div>
        <ul class="nav navbar-nav">
            <router-link tag="li" activeClass="active" exact role="presentation" to="/portfolio"> <a>Portfolio</a> </router-link>
            <router-link tag="li" activeClass="active" exact role="presentation" to="/stocks"> <a>Stocks</a> </router-link>
        </ul>
        <ul class="nav navbar-nav navbar-right">
            <li><a href="#">End Day</a></li>
            <li class="dropdown">
                <a 
                href="#"
                 class="dropdown-toggle" 
                 data-toggle="dropdown" 
                 role="button" 
                 aria-haspopup="true" 
                 aria-expanded="false">Save and Load 
               <span class="caret"></span></a>
                <ul class="dropdown-menu">
                    <li><a href="#">Save</a></li>
                    <li><a href="#">Load</a></li>
                </ul>
            </li>
        </ul>
    </nav>
</template>

<script>
export default {

}
</script>

<style>

</style>
