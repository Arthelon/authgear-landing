<script>
  import Prism from "prismjs";
  import "prismjs/components/prism-kotlin";
  import "prismjs/components/prism-swift";
  import { onMount, afterUpdate } from "svelte"; // eslint-disable-line import/no-extraneous-dependencies

  export let codeTabs = [];

  let codeEditorElement;
  let currTab = codeTabs[0];

  onMount(() => {
    codeEditorElement.textContent = currTab.content;
  });

  // language for syntax highlighting is set using the 'language-...' classname so
  // need to wait for view to be updated before re-highlighting
  afterUpdate(() => {
    Prism.highlightElement(codeEditorElement);
  });

  function handleTabClick(idx) {
    return function cb() {
      currTab = codeTabs[idx];
      codeEditorElement.textContent = currTab.content;
    };
  }

  function handleCopyClick() {
    const textArea = document.createElement("textarea");
    textArea.value = currTab.content;
    textArea.style.top = "0";
    textArea.style.left = "0";
    textArea.style.zIndex = "-1";
    textArea.style.position = "fixed";
    document.body.appendChild(textArea);
    textArea.focus();
    textArea.select();
    document.execCommand("copy");
    document.body.removeChild(textArea);
  }
</script>

<style>
  .editor {
    height: 100%;
    min-height: 350px;
    max-height: 700px;
    width: 100%;
    display: flex;
    flex-direction: column;
    box-shadow: 0px 2px 14px 0 hsla(0, 0%, 0%, 0.5);
  }

  .editor__header {
    display: flex;
    justify-content: space-between;
  }

  .editor__code-wrapper {
    height: 100%;
    margin: 0;
    border-radius: 0;
  }

  .editor__header__tabs-wrapper {
    padding: 20px 25px 15px 25px;
    background-color: #fff;
  }

  .editor__header__tab {
    display: inline-block;
    font-size: 13px;
    font-weight: 900;
    padding: 5px 4px;
    margin-right: 35px;
    cursor: pointer;
    background-color: #fff;
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

  @media screen and (max-width: 768px) {
    .editor__header__copybtn-wrapper {
      display: none;
    }
  }
</style>

<div class="editor">
  <div class="editor__header">
    <div class="editor__header__tabs-wrapper">
      {#each codeTabs as tab, idx}
        <button
          class="editor__header__tab"
          class:editor__header__tab--active={currTab.language === tab.language}
          on:click={handleTabClick(idx)}>
          {tab.language}
        </button>
      {/each}
    </div>
    <div class="editor__header__copybtn-wrapper">
      <button class="editor__header__copybtn" on:click={handleCopyClick}>
        Copy Code
      </button>
    </div>
  </div>
  <pre class="editor__code-wrapper">
    <code class="language-{currTab.language}" bind:this={codeEditorElement} />
  </pre>
</div>
