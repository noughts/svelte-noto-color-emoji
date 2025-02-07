<script lang="ts">
    export let emoji: string;
    export let size: string;
    $: codePoint = emoji.codePointAt(0);
    $: unicode = codePoint?.toString(16);
    $: src = `https://raw.githubusercontent.com/googlefonts/noto-emoji/refs/heads/main/svg/emoji_u${unicode}.svg`;
</script>

<img {src} alt={emoji} style:width={size} style:height={size} />
