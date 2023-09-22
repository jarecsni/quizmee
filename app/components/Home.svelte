<page>
    <actionBar title="Quizmee" />
    <gridLayout>
        <label class="info">
            <formattedString>
                <span class="fas" text="&#xf135;" />
                <span text=" {message}" />
            </formattedString>
        </label>
        <button text="About" on:tap="{onAboutButtonTap}" />
    </gridLayout>
</page>

<script lang="ts">
    import { navigate } from 'svelte-native';
    import About from '~/pages/About.svelte';

    let message: string = "Blank Svelte Native App";

    function onAboutButtonTap() {
        navigate({
            page: About,
            props: { }
        })
    }
</script>

<style>
    .info .fas {
        color: #3A53FF;
    }

    .info {
        font-size: 20;
        horizontal-align: center;
        vertical-align: center;
    }
</style>
