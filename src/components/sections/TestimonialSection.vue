<template>
    <section class="testimonial">
        <div class="container">
            <div class="testimonial__box">
                <img class="testimonial__img" src="../../assets/img/man_testimonial.png" alt="testimonial">
                <p class="testimonial__text">Curabitur non tristique tortor. Vestibulum aliquet suscipit ipsum in volutpat. Donec vel lacinia sem, vitae semper nulla. In hac habitasse platea dictumst. Mauris consectetur est et nibh sadip hendrerit bibendum.</p>
                <span class="testimonial__name"><strong>Darío Pineda</strong>, Theme Fusion</span>
                <div class="testimonial__icons">
                    <span class="testimonial__icon"><i class="fa-solid fa-circle"></i></span>
                    <span class="testimonial__icon"><i class="fa-regular fa-circle"></i></span>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'TestimonialSection',
    }
</script>

<style lang="scss" scoped>
    .testimonial {
        background-image: url('../../assets/img/testimonials_home_1_bg.jpg');
        background-position: center;
        background-size: cover;
        margin: 5rem 0;
        font-size: .875rem;

        &__box {
            text-align: center;
            padding: 6.25rem;
            color: var(--primary-color-text);
        }

        &__text {
            margin: 1.875rem;
        }

        &__name {
            display: inline-block;
            margin-bottom: 1.875rem;
        }

        &__icon {
            margin-right: .625rem;
        }
    }
</style>