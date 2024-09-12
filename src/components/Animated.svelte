<script lang="ts">
    import { fade } from 'svelte/transition';
    import GoogleTranslate from './GoogleTranslate.svelte'
    export let update: any;

    // function fixPosition(node, { delay = 0, duration = 400, width = 300 }) {
    //     return {
    //         delay,
    //         duration,
    //         css: function (t) {
    //             return `height: 0px; overflow:hidden;`;
    //         },
    //     };
    // }
</script>

{#key update}
<GoogleTranslate
elementId={'google-translate-element'}
options={{ pageLanguage: 'kr', includedLanguages: 'pt,en' }}>
</GoogleTranslate>
    <div class="animated" in:fade="{{ duration: 400 }}" id="google-translate-element">
        <slot />
    </div>
{/key}

<style>
</style>
