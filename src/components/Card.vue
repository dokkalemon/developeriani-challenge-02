<template>
    <section class="card-container">
        <div class="card">
            <div class="card-image">
                <img src="../assets/image-equilibrium.jpg" alt="">
                <div class="card-image-philter">
                    <img src="../assets/icon-view.svg" alt="">
                </div>
            </div>
            <div class="card-info">
                <div class="card-title">
                    <h1>Equilibrium #3429</h1>
                </div>
                <div class="card-text">
                    <p>Our Equilibrium collection promotes balance and calm</p>
                </div>


            </div>

        </div>
    </section>
          
</template>

<script>

export default {
    name: 'Card'
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
            padding: 30px 0px;
            font-weight: 400;
            h1 {
                font-size: 22px;
            }
            
        }

    }
    &:hover {
        transform: scale(1.05);
        .card-image-philter {
            opacity: 1;
        }
    }
}

</style>