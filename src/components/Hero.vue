<template>
    <section class="section">
        <div class="container">
            <div class="hero">
                <div class="hero-info">
                    <h1>Want anything to be easy with <span>LaslesVPN.</span></h1>
                    <p>Provide a network for all your needs with ease and fun using LaslesVPN discover interesting features from us.</p>
                    <a href="#" class="btn btn--filled btn--filled-br">Get Started</a>
                </div>
                <div class="hero-img">
                    <img src="@/assets/img/illustration-hero.svg" alt="">
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
.hero {
    display: flex;
    flex-direction: column;

    align-items: center;

    padding: 120px 0 70px;

    gap: 25px;

    &-info {
        h1 {
            font-size: 35px;
            font-weight: 500;
        }

        h1 span {
            font-size: 35px;
            font-weight: 700;
        }

        p {
            margin: 15px 0 35px;
            line-height: 25px;
            
            color: var(--gray-50);
        }
    }

    &-img {
        width: 100%;

        img {
            width: 100%;
        }
    }
}
</style>