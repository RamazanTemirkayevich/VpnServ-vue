<template>
    <section class="section">
        <header class="header container">
            <div class="header-logo">
                <img src="@/assets/icons/logo.svg" alt="">
                <p>Lasles<span>VPN</span></p>
            </div>
            <nav class="header-nav"
                :class="{
                    'active': isMenuActive
                }"
            >
                <ul class="header-nav__menu">
                    <li class="header-nav__list">
                        <a href="#">About</a>
                    </li>
                    <li class="header-nav__list">
                        <a href="#">Features</a>
                    </li>
                    <li class="header-nav__list">
                        <a href="#">Pricing</a>
                    </li>
                    <li class="header-nav__list">
                        <a href="#">Testimonials</a>
                    </li>
                    <li class="header-nav__list">
                        <a href="#">Help</a>
                    </li>
                </ul>
                <div class="header-nav__actions"
                    :class="{
                        'active': isBtnsActive
                    }"
                >
                    <a href="#">Sign In</a>
                    <a href="#" class="btn btn--stroke">Sign Up</a>
                </div>
            </nav>
            <div class="header-burger" type="button"
                :class="{
                    'active': isBurgerActive
                }"
                @click.prevent="toggle">
                <span></span>
            </div>
        </header>
    </section>
</template>

<script>
export default {
    name: 'burger',
    data: () => ({
        isBurgerActive: false,
        isMenuActive: false,
        isBtnsActive: false
    }),
    methods: {
        toggle () {
            this.isBurgerActive = !this.isBurgerActive
            this.isMenuActive = !this.isMenuActive
            this.isBtnsActive = !this.isBtnsActive
            this.$emit('active')
            this.$emit('active')
        }
    }
}
</script>

<style lang="scss" scoped>
.header {
    display: flex;
    align-items: center;
    justify-content: space-between;

    padding-top: 25px;

    &-logo {
        display: flex;
        align-items: center;
        gap: 10px;

        width: 35px;
        height: 37px;

        z-index: 10;

        p {
            font-size: 20px;
            font-weight: 500;

            color: var(--black);
        }

        p span {
            font-size: 20px;
            font-weight: 700;

            color: var(--black);
        }

        img {
            width: 100%;
            height: 100%;
        }
    }

    &-nav {
        position: fixed;

        display: none;

        padding: 150px 0 30px;

        gap: 50px;

        top: 0;
        left: 0;

        width: 0;
        height: 100%;

        transition: .6s;
        animation: anim 1s ease;
        background-color: var(--white);
        overflow: scroll;

        z-index: 9;

        &.active {
            display: flex;
            align-items: center;
            justify-content: space-between;

            flex-direction: column;

            width: 100%;
        }

        &.active &__menu {
            display: flex;
            flex-direction: column;
            align-items: center;

            gap: 15px;
        }

        &.active &__list a {
            position: relative;

            font-size: 22px;

            color: var(--gray-50);

            &:hover {
                &::after {
                    position: absolute;

                    content: '';

                    bottom: -3px;
                    left: 0;

                    width: 100%;
                    height: 3px;

                    background-color: var(--gray-50);
                    animation: underline 0.3s;
                }
            }
        }
    }

    &-nav__actions {
        display: none;

        a:nth-child(1) {
            font-weight: 700;
        }

        &.active {
            display: flex;
            flex-direction: column;
            align-items: center;

            gap: 15px;
        }
    }

    &-burger {
        position: relative;
        width: 25px;
        height: 21px;

        z-index: 10;

        cursor: pointer;

        &::after,
        &::before {
            position: absolute;

            content: '';

            width: 100%;
            height: 3px;

            background-color: var(--gray-50);
            border-radius: var(--br--5);
            transition: .3s;
        }

        &::before {
            top: 0;
        }

        &::after {
            bottom: 0;
        }

        &.active {
            span {
                scale: 0;
            }

            &::before {
                top: 44%;

                transform: rotate(-135deg);
            }

            &::after {
                top: 44%;

                transform: rotate(135deg);
            }
        }
    }

    &-burger span {
        position: absolute;
        width: 100%;
        height: 3px;

        top: 44%;

        background-color: var(--gray-50);
        border-radius: var(--br--5);
        transition: .3s;
    }
}
</style>