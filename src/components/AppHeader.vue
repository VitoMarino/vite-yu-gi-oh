<script>
export default {
    data() {
    return {

        }
    }
}
</script>

<template>
    <header>
        <nav>
            <ul>
                <li>
                    <img src="/src/assets/img/yugioh_J7Kcw4J_jpeg_1376x774_crop_q85.webp" alt="yu gi oh">
                </li>
                <li>
                    <p>
                        Yu-Gi-Oh Api
                    </p>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
    @use './style/partials/mixins.scss' as*;
    @use './style/partials/variabili.scss' as*;

    img {
        width: 80px;
    }

    nav ul {
        padding: 1rem;
        display: flex;
        align-items: center;

        p{
            font-size: 3rem;
        }
    }
</style>