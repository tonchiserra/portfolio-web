<script setup lang="ts">
    import { SplideSlide } from '@splidejs/vue-splide';

    defineProps(['project'])
</script>

<template>
    <SplideSlide class="project-card">
        <div class="image-container">
            <img :src="project.image" :alt="project.title" v-if="!!project.image" />
        </div>

        <div class="info-container">
            <div class="project-title">
                <h4>{{ project.title }}</h4>
                <span>{{ project.subtitle }}</span>
            </div>
            <p>{{ project.description }}</p>
            <div class="buttons">
                <a :href="project.demo" class="button" :class="!!project.demo ? '' : 'disabled'">Try it</a>
                <a :href="project.repo" class="underline" :class="!!project.repo ? '' : 'disabled'">View code</a>
            </div>
        </div>
    </SplideSlide>
</template>

<style scoped lang="scss">
.project-card {
    display: grid;
    grid-template-columns: 50% 50%;
    border-radius: 10px;
    border: 1px solid var(--gray-color-100);
    transition: all 300ms ease;

    &.is-active {
        transform: translateY(-100px);
    }

    .image-container {
        background-color: var(--second-color);

        img {
            transition: all 300ms ease;
        }

        &:hover {
            img {
                transform: scale(1.2);
            }
        }
    }

    .info-container {
        display: flex;
        flex-direction: column;
        gap: 20px;
        padding: 40px 20px;

        p {
            font-size: 1.6rem;
            line-height: 2.4rem;
        }

        .project-title {
            display: flex;
            flex-direction: column;
            gap: 5px;

            span {
                font-size: 1.2rem;
                font-weight: 600;
                color: var(--second-text-color);
            }
        }

        .buttons {
            display: flex;
            flex-direction: row;
            align-items: center;
            justify-content: flex-start;
            gap: 20px;

            .button {
                color: var(--main-color);

                &:hover {
                    color: var(--text-color);
                }
            }
        }
    }
}
</style>