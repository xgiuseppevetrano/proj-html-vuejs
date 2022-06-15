<template>
    <div class="buttons">
        <button class="button" :class="{active : button.isActive}" v-for="(button, index) in buttons" :key="index">{{button.text}}</button>
    </div>
</template>

<script>
    export default {
        name: 'RectangularButton',
        data () {
            return {
                buttons: [
                    {
                        text: 'Men',
                        isActive: true
                    },
                    {
                        text: 'Woman',
                        isActive: false
                    },
                    {
                        text: 'Accessories',
                        isActive: false
                    }
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    .buttons {
        text-align: center;
        padding: 3.125rem 0;

        .button {
            padding: .9375rem 3.125rem;
            border: 1px solid var(--quinary-color-text);
            background-color: var(--bg-color-rectangular-button);
            color: var(--quaternary-bg-color);
            font-weight: 600;

            &.active {
                background-color: transparent;
            }
        }
    }
</style>