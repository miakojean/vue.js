<template>
    <section>

        <div class="container center-flex">
            <div class="login__form">
                <div class="logo">
                    <H1>CALADRIUS</H1>
                </div>
                <div class="message" style="display: none;">
                <span></span>
                </div>
                <form action="">
                    <div class="input__groupe center-flex">
                        <label for="email">Email</label>
                        <input type="email" name="email" id="" placeholder="Entrer votre email">
                        <span></span>
                    </div>
                    <div class="input__groupe center-flex">
                        <label for="email">Email</label>
                        <input type="password" name="email" id="" placeholder="Entrer votre mot de passe">
                        <span></span>
                    </div>
                    <div class="input__groupe center-flex">
                        <button type="submit">
                            Se connecter
                        </button>
                    </div>
                </form>
            </div>

            <div class="account">

                <p>Mot de passe oublié</p>

            </div>
        </div>

    </section>
</template>

<script>
export default {

}
</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

*{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}

*:root{
    --section_padding: 1rem;

}

h1{
    font-size: 2.5rem;
    font-weight: 800;
}

h2{
    font-size: 2rem;
    font-weight: 600;
}

h3{
    font-size: 1.5rem;
    font-weight: 400;
}

p{
    font-size: var(--p--size);
}

label{
    font-size: var(--h3--size);
    font-weight: 600;
}

input {
    padding: 1rem;
    font-size: var(--p--size);
}

button {
    padding: 0.7rem;
}

body{
    background:#ffffff;
    font-family: 'inter', sans-serif;
}

.center-flex{
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 1rem;
}

section{
    padding: var(--section_padding);
}

.container{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);  
}

</style>