<template>
    <section class="section">
        <div class="container">
            <div class="about">
                <ul class="about-wrapper">
                    <li class="about-wrapper__item">
                        <div class="about-wrapper__ico">
                            <img src="@/assets/icons/heroicons_sm-user.svg" alt="">
                        </div>
                        <div class="about-wrapper__info">
                            <span>90+</span>
                            <p>Users</p>
                        </div>
                    </li>
                    <li class="about-wrapper__item">
                        <div class="about-wrapper__ico">
                            <img src="@/assets/icons/gridicons_location.svg" alt="">
                        </div>
                        <div class="about-wrapper__info">
                            <span>30+</span>
                            <p>Locations</p>
                        </div>
                    </li>
                    <li class="about-wrapper__item">
                        <div class="about-wrapper__ico">
                            <img src="@/assets/icons/bx_bxs-server.svg" alt="">
                        </div>
                        <div class="about-wrapper__info">
                            <span>50+</span>
                            <p>Servers</p>
                        </div>
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
.about {
    &-wrapper {
        position: relative;

        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;

        gap: 40px;
        
        padding: 35px 50px;
        border-radius: var(--br--10);
        background-color: var(--white);  
        
        &::after {
            position: absolute; 

            content: '';

            width: 90%;
            height: 90%;

            bottom: -55px;
            left: 50%;

            opacity: 0.06;
        
            background-color: var(--gray-40);
            filter: blur(57px);
            border-radius: var(--br--10);
            
            transform: translateX(-50%);
            z-index: -1;
        }
    }

    &-wrapper__item,
    &-wrapper__info,
    &-wrapper__ico {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    &-wrapper__item {
        position: relative;

        &:last-child {
            position: static;

            &::after {
                content: none;
            }
        }

        &::after {
            position: absolute;

            content: '';

            left: 50%;
            bottom: -20px;

            transform: translateX(-50%);
            width: 120px;
            height: 2px;

            background-color: var(--gray-100);
            border-radius: var(--br--3);
        }
    }

    &-wrapper__ico {
        flex-shrink: 0;

        width: 55px;
        height: 55px;

        border-radius: 70px;
        background: var(--gray-200);

        img {
            width: 24px;
            height: 24px;
        }
    }

    &-wrapper__info {
    }
}
</style>