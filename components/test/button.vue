<template>
    <div class="test-button">
        <button :class="classes">
            <p class="test-button__text">
                <slot />
            </p>
        </button>
    </div>
</template>
<script>
	export default {
		name: 'TestButton',
        props: {
			view: {
				type: String,
				default: 'light',
				validator: (value) => ['light', 'dark'].includes(value),
			}
		},
		setup(props) {
			const classes = computed(() => ({
				'test-button__button': true,
				[`test-button__button_${props.view}`]: true
			}));

			return { classes };
		},
	};
</script>
<style lang="less" scoped>
    .test-button {
        &__button {
            padding: 6px 12px;
            &_dark {
                background-color: #000;
                .test-button__text {
                    color: white;
                }
            }
        }
        &__text {
            font-size: 14px;
            color: black;
        }
    }
</style>