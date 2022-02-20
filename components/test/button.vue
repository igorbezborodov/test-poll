<template>
    <div>
        <button style="width: 100px; height 20px; background-color: grey">
            <slot />
        </button>
    </div>
</template>
<script>
	export default {
		name: 'TestButton',
	};
</script>