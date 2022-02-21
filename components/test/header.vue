<template>
    <div class="header">
        <test-button>
            Войти
        </test-button>
        <test-button view="dark">
            Зарегистрироваться
        </test-button>
    </div>
</template>
<script>
	export default {
		name: 'TestHeader',
	};
</script>
<style lang="less" scoped>
    .header {
        display: flex;
        gap: 24px;
        justify-content: flex-end;
        align-items: center;
        padding: 10px 20px;
    }
</style>