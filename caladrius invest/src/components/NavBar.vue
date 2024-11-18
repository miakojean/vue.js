<template>

    <nav>
        <div class="nav__logo"><a href="#">CALIUS</a></div>
            <div class="nav__menu__btn" id="menu-btn">
            <button class="nav__btn" type="button">Commencer</button>
        </div>
    </nav>

</template>

<script>

</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

:root{
    --primary-color: #18534F;
    --secondary-color: #2a9d8f;
    --textcolor: #272323;

    /*About font size*/
    --header-h1-size: 2.5rem;
    --header-h2-size: 2rem;
    --header-h3-size: 1.5rem;
    --header-p-size: 1rem

    /*spa*/
}

.nav__btn{
    padding: 0.5rem;
    font-size: 0.8rem;
    font-family: 'poppins', sans-serif;
    border-radius: 0.5rem;
    background: var(--secondary-color);
    color: aliceblue;
    border: none;
}

.btn{
    padding: 0.5rem;
    background: var(--secondary-color);
    color: white;
    font-family: 'poppins', sans-serif;
    font-weight: 300;
    font-size: 1rem;
    border: none;
    border-radius: 0.5rem;
    cursor: pointer;
}


/*============================================================*/

*{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}


/*nav*/

nav {
    position: fixed;
    width: 100%;
    max-width: var(--max-width);
    margin: auto;
    padding: 1rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 2rem;
    background-color: white;
    z-index: 99;
    box-shadow: 0px 2px 10px rgba(0, 0, 0, 0.2);
}
    
.nav__logo a {
    text-decoration: none;
    font-size: 1.2rem;
    font-weight: 700;
    color: var(--royal-blue-traditional);
}
    
.nav__links {
position: absolute;
left: 0;
top: 68px;
padding: 2rem;
width: 100%;
list-style: none;
display: flex;
align-items: center;
flex-direction: column;
gap: 2rem;
transform: scaleY(0);
transform-origin: top;
transition: 0.5s;
background-color: rgba(255, 255, 255, 0.9);
}

.nav__log{
display: none;
}

.nav__links.open {
transform: scaleY(1);
}

.link a {
font-weight: 400;
color: var(--text-light);
transition: 0.3s;
}

.link a:hover {
color: var(--text-dark);
}

.nav__links .link a {
color: var(--text-dark);
opacity: 0;
}

.nav__links.open .link a {
opacity: 1;
}

.link__log{
background: var(--bice-blue);
color: var(--white);
padding: 10px;
border-radius: 5px;
}

.link__log a{
text-align: center;
text-decoration: none;
color: var(--white);
}

.nav__menu__btn {
font-size: 1.5rem;
color: var(--text-dark);
cursor: pointer;
}

</style>