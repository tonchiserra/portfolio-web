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
                <a :href="project.repo" :class="!!project.repo ? '' : 'disabled'">View code</a>
            </div>
        </div>
    </SplideSlide>
</template>

<style scoped lang="scss">
.project-card {
    display: grid;
    grid-template-columns: 50% 50%;
    border-radius: 10px;
    border: 1px solid $gray-color-100;
    transition: all 300ms ease;

    @include mobile-only{
        grid-template-columns: 100%;
    }

    &.is-active {
        transform: translateY(-100px);

        @include mobile-only {
            transform: unset;
        }
    }

    .image-container {
        background-color: $second-color;

        @include mobile-only {
            height: 250px;
        }

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

        @include mobile-only {
            padding: 20px 20px 30px;
        }

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
                color: $second-text-color;
            }
        }

        .buttons {
            display: flex;
            flex-direction: row;
            align-items: center;
            justify-content: flex-start;
            gap: 20px;

            .button {
                color: $main-color;

                &:hover {
                    color: $text-color;
                }
            }
        }
    }
}
</style>