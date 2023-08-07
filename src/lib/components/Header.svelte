<script>
    import NavBar from "./NavBar.svelte";
    import logo from "../images/logo-main.png";
    import img1 from "../images/headerr-1.jpg";

    const NavList = [
        {name: "Page" , link: "/page"},
        {name: "Portfolio" , link: "/Portfolio"},
        {name: "Blog" , link: "/Blog"},
        {name: "Shop" , link: "/Shop"}
    ];
</script>

<header class="bg-gray-900 mt-4 mr-4 max-w-lg">

        <div class="items-center w-4 h-4">
            <img src={logo} class="w-4 h-4" alt="leroux">

            <div class="items-center">
                <NavBar name="Home" link="/" />

                {#each NavList as item}
                    <NavBar name={item.name} link={item.link} />
                {/each}
            </div>
        </div>
    

</header>
<div class="max-w-lg">
    <img src={img1} alt="image1">
</div>

<style>
    header{
        background-color: darkslategrey;
    }
    img{
        height: 5%;
        width: 5%;
    }
    div{
        width: 50%;
    }
</style>

