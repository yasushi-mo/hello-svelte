<script lang="ts">
  const title = $state('Svelte 入門')
  let name = $state('')
  let greeting = $state('')

  function greet() {
    greeting = `こんにちは、${name}さん`
  }
</script>

<h1>{title}</h1>

<label>
  名前
  <input bind:value={name} />
</label>
<p>入力中の値：{name}</p>

<button onclick={greet}>挨拶する</button>
<p>{greeting}</p>