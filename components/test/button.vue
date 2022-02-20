<template>
    <div class="test-button">
        <button class="test-button__button">
            <p class="test-button__text">
                <slot />
            </p>
        </button>
    </div>
</template>
<script>
	export default {
		name: 'TestButton',
	};
</script>
<style lang="less" scoped>
    .test-button {
        &__button {
            padding: 6px 12px;
        }
        &__text {
            font-size: 14px;
            color: black;
        }
    }
</style>