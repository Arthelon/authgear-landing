<script>
  export let codeTabs = [];

  let tabIdx = 0;
  let editorAreaElement;
  $: currTab = codeTabs[tabIdx];

  function handleTabClick(idx) {
    return function() {
      tabIdx = idx;
    };
  }

  function handleCopyClick() {
    editorAreaElement.focus();
    editorAreaElement.select();
    document.execCommand("copy");
    window.getSelection().removeAllRanges();
    editorAreaElement.blur();
  }
</script>

<style>
  .editor {
    height: 100%;
    width: 100%;
    display: flex;
    flex-direction: column;
    box-shadow: 0px 2px 14px 0 hsla(0, 0%, 0%, 0.5);
  }

  .editor__header {
    display: flex;
    justify-content: space-between;
  }

  .editor__textarea {
    font-size: 13px;
    font-family: Consolas, Monaco, Lucida Console, Liberation Mono,
      DejaVu Sans Mono, Bitstream Vera Sans Mono, Courier New, monospace;
    margin: 0;
    padding: 32px 27px;
    width: 100%;
    height: 100%;
    color: #f4c020;
    background-color: #1b1b1b;
    outline: none;
    resize: none;
  }

  .editor__header__tabs-wrapper {
    padding: 20px 25px;
    background-color: #fff;
  }

  .editor__header__tab {
    display: inline-block;
    font-size: 13px;
    font-weight: 900;
    padding: 5px 4px;
    margin-right: 35px;
    cursor: pointer;
  }

  .editor__header__tab--active {
    border-bottom: 3px solid hsl(216, 93.4%, 52.7%);
  }

  .editor__header__copybtn-wrapper {
    display: flex;
    align-items: center;
  }

  .editor__header__copybtn {
    padding: 10px 20px;
    color: #166ff7;
    font-size: 13px;
    font-weight: 900;
    background-color: #fff;
  }
</style>

<div class="editor">
  <div class="editor__header">
    <div class="editor__header__tabs-wrapper">
      {#each codeTabs as tab, idx}
        <div
          class="editor__header__tab"
          class:editor__header__tab--active={currTab.language == tab.language}
          on:click={handleTabClick(idx)}>
          {tab.language}
        </div>
      {/each}
    </div>
    <div class="editor__header__copybtn-wrapper">
      <button class="editor__header__copybtn" on:click={handleCopyClick}>
        Copy Code
      </button>
    </div>
  </div>
  <textarea
    readonly
    bind:this={editorAreaElement}
    class="editor__textarea"
    value={currTab.contents} />
</div>
