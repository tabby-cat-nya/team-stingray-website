<script setup lang="ts">
import type { ButtonData } from '~/components/MemberCard.vue';


useSeoMeta({
    title: "Team Stingray",
    ogTitle: "Team Stingray",
    description: "Indie group of game devs from Sydney, Australia :3",
    ogDescription: "Indie group of game devs from Sydney, Australia :3.",
});

const tabbyButtons: Ref<ButtonData[]> = ref([
    { link: "https://tabbycat.dev", text: "tabbycat.dev" },
    { link: "https://www.linkedin.com/in/tom--howarth/", text: "Linkedin" },
    { link: "https://bsky.app/profile/tabbycat.dev", text: "Bluesky" },
    { link: "https://tabby-cat-nya.itch.io/", text: "Itch.io" }
]);

const laurenButtons: Ref<ButtonData[]> = ref([
    {link: "https://www.linkedin.com/in/lauren-szmandiuk-00b018257/", text:"Linkedin"},
    {link: "https://gekkosaurus.itch.io/", text:"Itch.io"}
]);

const alexButtons: Ref<ButtonData[]> = ref([
    {link: "https://www.linkedin.com/in/alex-valacos/", text:"Linkedin"},
    {link: "https://pihoqub.itch.io/", text:"Itch.io"}
]);

const xanderButtons: Ref<ButtonData[]> = ref([
    { link: "https://xanderakkari.com/", text: "Portfolio" },
    {link: "https://www.linkedin.com/in/xander-akkari/", text:"Linkedin"},
    {link: "https://cookiespl.itch.io/", text:"Itch.io"}
]);

const ethanButtons: Ref<ButtonData[]> = ref([
    {link: "https://www.linkedin.com/in/ethan-lucas/", text:"Linkedin"},
    {link: "https://ethan-lucas.itch.io/", text:"Itch.io"}
]);
</script>

<template>
    <div>
        <img class="logo" src="/img/verticalWhite.png">

        <hr>

        <h2>Hey there!</h2>
        <p class="temp-space">We're an indie group of game developers from Sydney, Australia!</p>

        <div class="container">
            <BoldButton href="https://twitter.com/TeamStingrayDev" text="Twitter" />
            <BoldButton href="https://discord.gg/3BPYMHqNve" text="Discord Server" />
            <BoldButton href="mailto:devs@teamstingray.dev" text="Email" />
        </div>
        <!-- shortcut link to contact? -->

        <hr>

        <h2>The Team</h2>
        <div class="member-container">
            <MemberCard href="https://www.linkedin.com/in/lauren-szmandiuk-00b018257/" name="Lauren Szmandiuk"
                description="I specialise in creating art and animations! I'm the art director for most of our projects."
                image="/img/lauren.jpg" 
                :buttons="laurenButtons" />
            <MemberCard href="" name="Tom Howarth"
                description="I specialise in game design, managing the process of getting Arcane Raiders to Steam and other neat features like Acheivements and Discord integration"
                image="/img/tabby.jpg"
                :buttons='[
    { link: "https://tomhowarth.vercel.app/", text: "Portfolio" },
    { link: "https://www.linkedin.com/in/tom--howarth/", text: "Linkedin" }
]' />
            <MemberCard href="https://www.linkedin.com/in/ethan-lucas/" name="Ethan Lucas"
                description="Hello! My name is Ethan and I am a full-time Bachelor of Games Development student at the University of Technology Sydney. As a part of this degree, I have created various projects that prove knowledge in the field of game design and software usability. I have a great interest in digital entertainment media and being a part of successful teams."
                image="/img/ethan.jpg"
                :buttons="ethanButtons" />
                
            <MemberCard href="https://www.linkedin.com/in/xander-akkari/" name="Xander Akkari"
                description="I'm a game developer and multimedia specialist! I worked on the game design, programming and multiplayer implementation for Arcane Raiders. I also do video editing and any miscellaneous art that we need!" image="/img/xander.jpg" :buttons="xanderButtons" />
            <MemberCard href="https://www.linkedin.com/in/alex-valacos-326490256/" name="Alex Valacos"
                description="I was one of the main programmers and designers for Arcane Raiders, focussing on enemy logic and balance" image="/img/alex.jpg" :buttons="alexButtons" />
        </div>
        <!-- flexbox of team member cards -->

        <hr>

        <h2>Our Projects</h2>
        <div class="container">
            <ProjectCard src="https://img.itch.zone/aW1nLzE2Mjg0ODg2LnBuZw==/315x250%23c/6FRKz0.png"
                href="https://teamstingray.dev/arcane-raiders" heading="Arcane Raiders"
                description="Fight to the top of the tower with up to 4 players and an arsenal of powerful spells! We'll be showcasing it at SXSW Sydeny and its already avilable to wishlist on Steam!" />

            <ProjectCard src="https://img.itch.zone/aW1nLzE4NTUyMjIyLnBuZw==/315x250%23c/BwM7md.png"
                href="https://clevertop.itch.io/modline-drift" heading="Modline Drift"
                description="Work in progress racing game where you upgrade your car while you race!" />

            <ProjectCard src="https://img.itch.zone/aW1nLzE0NjYyOTAwLnBuZw==/315x250%23c/UaC28P.png"
                href="https://clevertop.itch.io/smoothie-maker-pro" heading="Smoothie Maker Pro"
                description="Make the world's greatest smoothies in this arcade puzzle game!" />

            <ProjectCard src="https://img.itch.zone/aW1nLzE1NDA4ODI2LnBuZw==/315x250%23c/TrI9Z5.png"
                href="https://ethan-lucas.itch.io/super-boxing" heading="Super Boxing"
                description="Prove you're the champion of NEW BOX CITY!" />

            <ProjectCard src="https://img.itch.zone/aW1nLzE0Nzg2Njc0LnBuZw==/315x250%23c/dKTgWr.png"
                href="https://ethan-lucas.itch.io/nothing-shady-at-this-bbq" heading="Nothing Shady at THIS BBQ!"
                description="Absolutely nothing at all!" />

            <ProjectCard src="https://img.itch.zone/aW1nLzEyNjA2MDI1LnBuZw==/315x250%23c/vaNWSF.png"
                href="https://ethan-lucas.itch.io/starship-scramble" heading="Starship Scramble"
                description="Fuel is expensive, Don't run out. - Featured at SXSW Sydney 2023!" />

            <ProjectCard src="https://img.itch.zone/aW1nLzE0MzYzNDI5LnBuZw==/315x250%23c/GU0g%2Bt.png"
                href="https://gekkosaurus.itch.io/tank-blitz" heading="Tank Blitz"
                description="Upgrade your tank as you travel to reach the end of the level" />
        </div>
        <!-- <BoldButton 
        href="/projects"
        text="View All"
    /> -->


        <!-- featured projects - what were currently working on / proud of / recently finished -->
        <!-- link to projects page -->
        <!-- 
    <hr>

    <h2>Contact Us!</h2> -->
        <!-- twitter, discord and email buttons/cards -->


        <!-- <ul><a href="/arcane-raiders">Landing Page for Arcane Raiders</a></ul>
    <ul><a href="/arcane">Short URL to Steam page</a></ul> -->
    </div>
</template>

<style>
.temp-space {
    padding-bottom: 10px;
}

.container {
    display: flex;
    justify-content: center;
    gap: 10px;
    flex-wrap: wrap;
}

.member-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 10px;
    /* align-items: center; */
}

/* @media (max-width: 1000px){
        .container{
            flex-direction: column;
        }
    } */

.logo {
    max-width: 35%;
    align-self: center;

}

body {
    font-family: Arial, Helvetica, sans-serif;
    text-align: center;
    margin-top: 1cm;
}


a {
    font-weight: 800;
}

/* a:link{
        color:cyan
    }

    a:visited{
        color:magenta
    }

    a:active{
        color:violet
    } */
</style>