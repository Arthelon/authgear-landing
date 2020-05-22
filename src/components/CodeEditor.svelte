<script>
  export let codeTabs = [];

  let tabIdx = 0;
  $: currTab = codeTabs[tabIdx];

  function handleTabClick(idx) {
    return function() {
      tabIdx = idx;
    };
  }
</script>

<style>
  .editor-wrapper {
    height: 100%;
    width: 100%;
    box-shadow: 0px 2px 14px 0 hsla(0, 0%, 0%, 0.5);
  }

  .editor-area {
    margin: 0;
    padding: 32px 27px;
    width: 100%;
    height: 100%;
    color: #f4c020;
    background-color: #1b1b1b;
  }

  .editor-tabs-wrapper {
    display: flex;
    padding: 20px 25px;
    background-color: #fff;
  }

  .editor-tab {
    font-size: 13px;
    font-weight: 900;
    padding: 5px 4px;
    margin-right: 35px;
    cursor: pointer;
  }

  .editor-tab.active {
    border-bottom: 3px solid hsl(216, 93.4%, 52.7%);
  }
</style>

<div class="editor-wrapper">
  <div class="editor-tabs-wrapper">
    {#each codeTabs as tab, idx}
      <div
        class="editor-tab"
        class:active={currTab.language == tab.language}
        on:click={handleTabClick(idx)}>
        {tab.language}
      </div>
    {/each}
    <button class="copy-btn" />
  </div>
  <pre class="editor-area">{currTab.contents}</pre>
</div>
