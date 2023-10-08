<template>
    <section class="section">
        <header class="header container">
            <div class="header-logo">
                <img src="@/assets/icons/logo.svg" alt="">
                <p>Lasles<span>VPN</span></p>
            </div>
            <nav class="header-nav">
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
            </nav>
            <div class="header-actions">
                <a href="#">Sign In</a>
                <a href="#">Sign Up</a>
            </div>
            <div class="header-burger hamburger--squeeze" type="button">
                <span class="hamburger-inner"></span>
            </div>
        </header>
    </section>
</template>

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
    }

    &-nav,
    &-actions {
        display: none;
    }

    &-burger {
        position: relative;
        width: 25px;
        height: 21px;

        &::after,
        &::before {
            position: absolute;

            content: '';

            width: 100%;
            height: 3px;

            background-color: var(--gray-50);
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
        transition: .3s;
    }
}
</style>