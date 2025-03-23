<template>
    <section>
        <article class="presentation">
            <div class="ma-photo">
                <img class="mon-visage" src="@/assets/image/ma-photo.jpg" alt="Photo de presentation">
            </div>
            <div class="espace"></div>
            <p>
                Je m’appelle Iordan Mazette, j'ai 25 ans, et je suis actuellement en formation pour devenir développeur web. Après un parcours varié allant du baccalauréat STMG Mercatique, à la formation militaire, puis l'université de sport (STAPS), j'ai découvert dans l'informatique une passion pour la création et la résolution de problèmes techniques. Ayant déjà expérimenté le développement avec un stage en programmation en <time datetime="2016">2016</time> (de 2 jours), j'aime apprendre, construire des solutions et explorer de nouvelles technologies.
            </p>
            <p>
                Ma curiosité m’a conduit à me former de manière autonome dans de nombreux domaines : jeux vidéo, domotique, électronique et bricolage, autant de passions qui me poussent à évoluer sans cesse. En parallèle, je suis passionné par le sport (football, ski, snowboard, VTT de descente, la course à pieds), la nature, l'automobile et j'aime beacoup voyager, des centres d'intérêt qui me rappellent l'importance de la discipline, de l'effort et de la persévérance, qui sont des valeurs essentielles pour moi.
            </p>
            <p>
                Je suis motivé, curieux, et je m'épanouis dans les projets qui me permettent d’apprendre et d'innover. Mon but est d’apporter une contribution concrète et créative dans le monde du web, en mêlant mes compétences techniques et mes intérêts variés, tout en apprenant de nouvelles choses et en m'amusant.
            </p>
        </article>
    </section>
</template>

<style scoped>
.presentation {
    width: 1000px;
    padding: 125px;
    border: 1px solid #782221;
    background-color: #782221;
    font-size: 25px;
}

p {
    margin: 50px auto;
    text-indent: 7%;
}

* {
    font-family: 'raleway';
}

.mon-visage {
    border: 2px solid white;
    border-radius: 60px 60px 60px 60px;
    box-shadow: 1px 1px 10px 10px black;
    width: 125px;
}

.ma-photo {
    display: flex;
    justify-content: center;
    align-items: center;
}

.espace {
    margin: 100px;
}
</style>