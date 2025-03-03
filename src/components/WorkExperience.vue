<script setup>
const workHistory = [
    {
        title: "Chorus Teacher",
        organization: "Wesleyan School",
        duration: "2017-Present",
        responsibilities: [
            "Led cross-functional collaboration across school divisions for large-scale events.",
            "Directed musical theater productions, overseeing music, orchestration, and live performances.",
            "Managed team meetings, scheduling, and performance logistics for major annual events.",
        ],
        subResponsibilities: [
            "2022 - Nominated for Shuler Hensley Award for Best Music Direction.",
        ],
    },
    {
        title: "Chorus Teacher",
        organization: "McEachern High",
        duration: "2010-2017",
        responsibilities: [
            "Developed and coached 150+ students annually, fostering a collaborative learning environment.",
            "Consistently improved ensemble performance scores through structured skill development & coaching.",
            "Served as Fine Arts Chair, coordinating efforts between multiple artistic departments.",
        ],
    },
];
</script>

<template>
    <div class="container">
        <section class="work">
            <h1 class="title">Work History</h1>
            <article v-for="(job, index) in workHistory" :key="index" class="job">
                <h2 class="job-title">{{ job.title }} | {{ job.organization }}</h2>
                <h3 class="job-duration">{{ job.duration }}</h3>
                <ul>
                    <li v-for="(responsibility, i) in job.responsibilities" :key="i">
                        {{ responsibility }}
                        <!-- Render sub-responsibilities if they exist -->
                        <ul v-if="i === job.responsibilities.length - 1 && job.subResponsibilities">
                            <li v-for="(sub, j) in job.subResponsibilities" :key="j">{{ sub }}</li>
                        </ul>
                    </li>
                </ul>
            </article>
        </section>
    </div>
</template>

<style scoped>
    .container {
        /* padding: 120px 0 0; */
        display: flex;
        justify-content: center;
        padding: 100px 0 0;
        max-width: 90%;
        margin: 0 auto;
    }

    .work {
        margin: 0px 0px 40px;
        /* text-align: left; */
        color: white;
        padding: 20px;
        max-width: 850px;
    }

    .title {
        text-align: center;
        font-size: 28pt;
        margin-bottom: 20px;
    }

    .job {
        margin-bottom: 30px;
    }

    .job-title {
        font-size: 22pt;
        margin: 0 0 10px;
    }

    .job-duration {
        font-size: 18pt;
        margin: 0 0 15px;
    }

    ul {
        padding-left: 20px;
        margin: 0;
    }

    h2 {
        font-size: 20pt;
    }

    li {
        font-size: 16pt;
        line-height: 1.6;
        text-align: left;
    }

    @media screen and (max-width: 480px) {
        .work {
            margin: 0px 20px 40px;
            padding: 30px;
        }
        .title {
            font-size: 24pt;
        }

        .job-title {
            font-size: 20pt;
        }

        .job-duration {
            font-size: 18pt;
        }

        li {
            font-size: 14pt;
        }
    }
</style>