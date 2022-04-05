<script>
    import {Link} from 'svelte-navigator'

    let sandwich = true

    const toggleSandwich = () => {
        sandwich = !sandwich
    }
</script>

<style>
    nav{
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;

        width: 100vw; 
    }

    .logo{
        padding-left: 2em;
    }

    .categories{
        display: flex;
        align-items: center;
        justify-content: space-around;

        padding-right: 4em;
        width: 70vw;
    }



    @media only screen and (min-width: 600px){
        .container{
            display: none;
        }
    }

    @media only screen and (max-width: 600px){
    .categories{
        display: none;
    }

        /* Sandwich Menu Styling, copied from W3 Schools */
        .container {
        display: inline-block;
        cursor: pointer;
        margin-right: 0;
        width: 100px;
        }

        .bar1, .bar2, .bar3 {
        width: 35px;
        height: 5px;
        background-color: #333;
        margin: 6px 0;
        transition: 0.4s;
        }
    /* Rotate first bar */
        .change .bar1 {
        -webkit-transform: rotate(-45deg) translate(-9px, 6px) ;
        transform: rotate(-45deg) translate(-9px, 6px) ;
        }
    /* Fade out the second bar */
        .change .bar2 {
        opacity: 0;
        }
    /* Rotate last bar */
        .change .bar3 {
        -webkit-transform: rotate(45deg) translate(-8px, -8px) ;
        transform: rotate(45deg) translate(-8px, -8px) ;
        }
    }
    
</style>

<nav>
    <h1 class='logo'>Logo</h1>
    <div class="categories">
        <Link to='/'><h5>Home</h5></Link>
        <Link to='about'><h5>About Us</h5></Link>
        <Link to='menu'><h5>Menu</h5></Link>
        <Link to='contact'><h5>Contact Us</h5></Link>
    </div>
    <div class="container {sandwich ? '' : 'change'}" on:click={toggleSandwich}>
      <div class="bar1"></div>
      <div class="bar2"></div>
      <div class="bar3"></div>
    </div>
</nav>
