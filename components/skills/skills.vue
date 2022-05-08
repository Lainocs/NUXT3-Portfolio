<template>
    <div class="content">
        <h2 id="skill-preview" data-aos="fade-left">Skills</h2>
        <div>
            <div data-aos="fade-down" data-aos-duration="1000" class="card">
                <div v-for="skill in skills" :key="skill" class="tab" :class="skill.skillName">
                    <img :src="skill.skillPicture" alt="skill-logo">
                    <div class="skill">
                        <!-- <h3 class="skill-title">{{skill.skillName}}</h3> -->
                        <div class="container-skills">
                            <div class="skill-content">
                                <div class="left">
                                    <div class="typewriter">
                                        <h3>{{skill.skillCode}}</h3>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div data-aos="zoom-in" data-aos-duration="1000" class="card">
                <div v-if="otherSkills[0]" class="otherSkills">
                    <div class="otherSkills-content">
                        <div v-for="otherSkill in otherSkills" :key="otherSkill" class="left others" @click="addToSkills(otherSkill)">
                            <a href="#skill-preview"><img :src="otherSkill.skillPicture"></a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import AOS from '@/mixins/aos';
    export default {
    name: "Skills",
    mixins: [
        AOS
    ],
    data() {
        return {
            skills: [
                {
                    skillName: 'Javascript',
                    skillPicture: '_nuxt/assets/images/skills/javascript.webp',
                    skillCode: 'document.getElementById("skills")',
                },
            ],
            otherSkills: [
                {
                    skillName: 'Python',
                    skillPicture: '_nuxt/assets/images/skills/python.webp',
                    skillCode: 'import numpy as np',
                },
                {
                    skillName: 'Django',
                    skillPicture: '_nuxt/assets/images/skills/django.webp',
                    skillCode: 'from django.shortcuts import render',
                },
                {
                    skillName: 'React',
                    skillPicture: '_nuxt/assets/images/skills/react.webp',
                    skillCode: 'import React from "react";',
                },
                {
                    skillName: 'NodeJS',
                    skillPicture: '_nuxt/assets/images/skills/node-js.webp',
                    skillCode: 'import express from "express";',
                },
                {
                    skillName: 'Swift',
                    skillPicture: '_nuxt/assets/images/skills/swift.webp',
                    skillCode: 'import Foundation',
                },
                {
                    skillName: 'PHP',
                    skillPicture: '_nuxt/assets/images/skills/php.webp',
                    skillCode: "foreach($skills as $skill) { $skill->name };",
                },
                {
                    skillName: 'Laravel',
                    skillPicture: '_nuxt/assets/images/skills/laravel.webp',
                    skillCode: 'php artisan db:seed SkillSeeder',
                },
                {
                    skillName: 'Symfony',
                    skillPicture: '_nuxt/assets/images/skills/symfony.webp',
                    skillCode: 'php bin/console doctrine:fixtures:load',
                },
                {
                    skillName: 'VueJS',
                    skillPicture: '_nuxt/assets/images/skills/vue-js.webp',
                    skillCode: "{{ data() { return { skillCode: this.skills.code }} }}",
                },
                {
                    skillName: 'Wordpress',
                    skillPicture: '_nuxt/assets/images/skills/wordpress.webp',
                    skillCode: "while ( have_posts() ) { the_post(); }",
                }
            ]
        }
    },
    methods: {
        addToSkills(skill) {
            // if skill isn't already in skills, add it
            if (!this.skills.includes(skill)) {

                this.skills.push(skill);

                // remove skill from otherSkills
                this.otherSkills = this.otherSkills.filter(otherSkill => otherSkill.skillName !== skill.skillName);

                // get the last skill in skills
                const lastSkill = this.skills[this.skills.length - 2];

                if(!this.otherSkills.includes(lastSkill)) {
                    this.otherSkills.push(lastSkill);
                }

                //remove otherSkill from skills
                this.skills = this.skills.filter(skill => skill.skillName !== lastSkill.skillName);
            }
        }
    },
}
</script>

<style>
    .typewriter h3 {
            font-size: 1.2em;
            overflow: hidden; /* Ensures the content is not revealed until the animation */
            border-right: .15em solid #6d6d6d; /* The typwriter cursor */
            white-space: nowrap; /* Keeps the content on a single line */
            margin: 0 auto; /* Gives that scrolling effect as the typing happens */
            letter-spacing: .15em; /* Adjust as needed */
            animation: 
                typing 3.5s steps(40, end),
                blink-caret .75s step-end infinite;
    }

    /* The typing effect */
    @keyframes typing {
    from { width: 0 }
    to { width: 100% }
    }

    /* The typewriter cursor effect */
    @keyframes blink-caret {
    from, to { border-color: transparent }
    50% { border-color: #6d6d6d; }
    }

    .splide {
        max-width: 100%;
    }

    .splide__pagination {
        bottom: 5em;
    }

    .skill {
        padding: 50px 0;
        color: #ffffff;
        
    }

    .content {
        width: 80vw;
        margin: 0 auto;
    }

    .content h2:first-child {
        font-size: 3em;
    }

    .container-skills {
        max-width: 90vw;
        margin: 0 auto;
        background-color:  rgba(94, 94, 94, 0.1);
        border-radius: 10px;
    }

    .skill-title {
        font-size: 1.3em;
        text-align: center;
    }

    .skill-content {
        border-radius: 10px;
        padding: 50px;
        margin: 50px 0;
        color: #6d6d6d;
    }

    .skill-content h2 {
        text-decoration: underline;
        text-underline-offset: 20px;
    }

    .tab {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        margin: 30px auto;
    }

    .tab img {
        height: 150px;
    }

    .card {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        border-radius: 20px;
    }

    .card .nav-tabs {
        list-style: none;
        display: flex;
    }

    .card .nav-tabs:last-child {
        color: #fff;
        padding: 0;
        margin: 20px 0 100px 0;
    }

    .card .nav-tabs:last-child h3 {
        text-decoration: underline;
        text-underline-offset: 20px;
    }

    .otherSkills {
        font-size: 1.4em;
    }

    .otherSkills-content {
        padding-top: 50px;
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        align-items: center;
        gap: 50px;
    }

    .otherSkills-content img {
        height: 80px;
        cursor: pointer;
    }

    @media screen and (max-width: 1000px) {
        .splide {
            max-width: fit-content !important;
        }
        .splide__arrows {
            display: none;
        }

        .skill-content {
            max-width: 80vw;
        }
    }
</style>