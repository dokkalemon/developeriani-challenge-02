<template>
    <section class="card-container">
        <div class="card">
            <div class="card-image">
                <img :src="require(`../assets/${thumb}`)" alt="">
                <div class="card-image-philter">
                    <img src="../assets/icon-view.svg" alt="">
                </div>
            </div>
            <div class="card-info">
                <div class="card-title">
                    <h2>{{ title }}</h2>
                </div>
                <div class="card-text">
                    <p>{{ text }}</p>
                </div>
                <div class="card-value">
                    <div class="card-item">
                        <img :src="require(`../assets/${logoValue}`)" alt="">
                        <span>{{ value }} {{ typeValue }}</span>
                    </div>
                    <div class="card-item">
                        <img src="../assets/icon-clock.svg" alt="">
                        <span>{{ time }}</span>
                    </div>
                </div>
                <div class="card-line"></div>

                <div class="card-user">
                    <img :src="require(`../assets/${avatar}`)" alt="">
                    <span>Creation of <a :href="`${url}`">{{ name }}</a></span>
                </div>

            </div>

        </div>
    </section>
          
</template>

<script>

export default {
    name: 'Card',

    props: {
        thumb: String,
        title: String,
        text: String,
        logoValue: String,
        value: String,
        typeValue: String,
        time: String,
        avatar: String,
        name: String,
        utl: String

    }
}
</script>

<style scoped lang="scss">
@import '@/styles/vars.scss';

.card-container {
    height: 606px;
    width: 360px;
    padding: 10px;
    transition: all .4s cubic-bezier(.17,.67,.34,1.8);
    .card {
        height: 100%;
        width: 100%;
        background-color: $card-back;
        border-radius: 15px;
        padding: 24px;
        cursor: pointer;
    }
    .card-image {
        height: 302px;
        width: 100%px;
        margin: 0 auto;
        position: relative;
        border-radius: 8px;
        overflow: hidden;
        cursor: pointer;
        img {
            height: 100%;
            width: 100%;
            object-fit: cover;
        }
        .card-image-philter {
            height: 100%;
            width: 100%;
            background-color: hsla(178, 100%, 50%, 0.502);
            position: absolute;
            top: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            opacity: 0;
            transition: all 0.4s ease;
            img {
                height: 48px;
                width: 48px;
            }
        }
    }
    .card-info {
        height: 100%;
        width: 100%;
        .card-title {
            padding: 30px 0px 20px 0;
            font-weight: 300;
            h2 {
                font-size: 22px;
                transition: all .4s ease
            }
        }
        .card-text {
            p {
                font-size: 16px;
                font-weight: 300;
                color: $soft-blue;
                padding: 0 0 30px 0
            }
        }
        .card-value {
            height: 30px;
            width: 100%;
            display: flex;
            padding-bottom: 30px;

            .card-item {

                height: 100%;
                width:100%;
                display: flex;
                align-items: center;
                img {
                    margin-right: 5px;
                }
                &:first-child {
                    justify-content: flex-start;
                    span {
                        color: $cyan;
                    }
                }
                &:last-child {
                    justify-content: flex-end;
                    span {
                        color: $soft-blue;
                        font-weight: 300;
                    }
                }
            }
            
        }

        .card-line {
            height: 1px;
            width: 100%;
            background-color: $card-line;
            margin-bottom: 16px;
        }

        .card-user {
            height: 33px;
            display: flex;
            justify-content: flex-start;
            align-items: center;
            img {
                height: 100%;
                border: 1px solid $white;
                border-radius: 100%;
                margin-right: 20px;
            }
            span {
                color: $soft-blue;
                font-weight: 300;
                a {
                    color: white;
                    text-decoration: none;
                    transition: all .4s ease
                }
            }
        }

    }
    &:hover {
        .card-user {
            span {
                a {
                    color: $cyan;
                }
            }
        }
        transform: scale(1.05);
        .card-image-philter {
            opacity: 1;
        }
        .card-title {
        h2 {
            color: $cyan
        }
    }
}
}

@media screen and (max-width: 375px) {
    .card-container {
        height: 553px;
        width: 237;
        .card {
            .card-image {
                height: 278px
            }
            .card-value {
                .card-item {
                    span {
                        font-size: 15px;
                    }
                }
            }
            .card-user {
                height: 25px;
                padding-bottom: 5px;
                span {
                    font-size: 15px;
                }
            }
        }
    }
}

</style>




