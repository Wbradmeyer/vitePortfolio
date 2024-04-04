<script setup></script>

<template>
    <div class="container">
        <div class="work">
            <h1 style="text-align: center;">Work History</h1>
            <h2 style="margin-bottom: 10px;">Chorus Teacher | Wesleyan School</h2>
            <h2 style="margin-top: 0px;">2017-Present</h2>
            <ul>
                <li>Collaborated with essential stakeholders across lower, middle, and high school 
                    divisions to present performances</li>
                <li>Planned and organized daily rehearsals as well as major annual events</li>
                <li>Directed annual musical theater productions</li>
                    <ul>
                        <li>Taught/rehearsed all music, contracted and directed a professional orchestra</li>
                        <li>2022 - Nominated for Shuler Hensley Award for Best Music Direction</li>
                    </ul>
            </ul>
            <h2 style="margin-bottom: 10px;">Chorus Teacher | McEachern High</h2>
            <h2 style="margin-top: 0px;">2010-2017</h2>
            <ul>
                <li>Developed and directed around 150 young singers annually fostering a supportive atmosphere</li>
                <li>Competed in a thriving county among the top-rated programs in the state</li>
                <li>Led as Fine Arts Chair promoting collaboration and organization between the band, chorus, 
                    orchestra, and visual art instructors</li>
            </ul>
        </div>
    </div>
</template>

<style scoped>
    .container {
        padding: 120px 0px 0px;
    }

    .work {
        margin: 0px 0px 40px;
        text-align: left;
        color: white;
        padding: 20px;
        max-width: 850px;
    }

    h2 {
        font-size: 20pt;
    }

    li {
        font-size: 18pt;
    }

    @media screen and (max-width: 480px) {
        h2 {
            font-size: 28pt;
        }
        
        li {
            font-size: 26pt;
        }
        .work {
            margin: 0px 20px 40px;
            padding: 30px;
        }
    }
</style>