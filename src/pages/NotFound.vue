<script setup>
import { useRouter } from "vue-router";
const router = useRouter();
</script>

<template>
    <div class="error_container">
        <div class="error">
            <div class="four-number">4</div>
            <img class="pokeball" src="../assets/images/pokeball.png" alt="pokeball" />
            <div class="four-number">4</div>
        </div>
        <div class="error-text">
            <h4 class="error-primary">Uh-oh!</h4>
            <p class="error-semi">You look lost on your journey!</p>
            <button class="go-home-btn" @click="() => router.push({ name: 'home' })">Go back to Home</button>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@import "../assets/scss";
.error_container {
    margin-top: 120px;
    @include flex(center, center);
    flex-direction: column;
}

.error {
    @include flex(center, center);
}
.four-number {
    font-size: 18rem;
    font-weight: 700;
    color: $text-color;
    line-height: 22rem;

    @include tablet {
        font-size: 10rem;
        line-height: 14rem;
    }

    @include mobile {
        font-size: 6rem;
        line-height: 8rem;
    }
}

.pokeball {
    width: 300px;

    @include tablet {
        width: 200px;
    }

    @include mobile {
        width: 100px;
    }
}

.error-text {
    @include flex(center, center);
    flex-direction: column;
    margin-top: 20px;
}

.error-primary {
    margin-top: 26px;
    font-size: 3rem;
    font-weight: 700;
    line-height: 1.6;
    color: $black;

    @include tablet {
        font-size: 2rem;
    }

    @include mobile {
        font-size: 1.8rem;
    }
}

.error-semi {
    margin-top: 26px;
    font-size: 2rem;
    font-weight: 400;
    line-height: 1.6;
    color: $text-color;

    @include tablet {
        font-size: 1.6rem;
    }

    @include mobile {
        font-size: 1.2rem;
    }
}

.go-home-btn {
    margin-top: 30px;
    display: inline-block;
    padding: 12px 20px;
    font-size: 1.2rem;
    font-weight: 500;
    line-height: 1.4;
    border-radius: 12px;
    color: $white;
    cursor: pointer;
    transition: all 0.3s ease;
    background-color: $red;
    &:hover {
        background-color: rgba($color: $red, $alpha: 0.8);
    }
}
</style>

<style lang="scss">
body {
    background-image: unset;
    background-color: #fff;
}
</style>