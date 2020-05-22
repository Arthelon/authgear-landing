<script>
  import CodeEditor from "./CodeEditor.svelte";

  const codeTabs = [
    {
      language: "JavaScript",
      contents: "function() { // this is some sample JS code }",
    },
    {
      language: "Kotlin",
      contents: "function() { // this is some sample Kotlin code }",
    },
    {
      language: "Swift",
      contents: "function() { // this is some sample Swift code }",
    },
  ];
</script>

<style>
  .code-sample {
    padding-top: 0;
    padding-bottom: 80px;
  }

  .container-fluid {
    max-width: 1200px;
  }

  .code-sample__title {
    color: #166ff7;
    font-size: 32px;
    text-align: center;
    margin: 0;
  }

  .code-sample__img-wrapper {
    text-align: center;
    padding-top: 25px;
  }

  .code-sample__img {
    max-width: 420px;
    height: auto;
    display: inline-block;
    vertical-align: top;
  }

  @media screen and (min-width: 768px) {
    .container-fluid {
      padding-left: 56px;
      padding-right: 56px;
    }

    .code-sample__content-wrapper {
      margin-top: 92px;
    }
  }
</style>

<section class="code-sample">
  <div class="container-fluid">
    <div class="row">
      <div class="col-12">
        <h1 class="code-sample__title">
          Integrate Skygear Auth in Any Application in Just 5 Minutes!
        </h1>
      </div>
    </div>
    <div class="code-sample__content-wrapper row">
      <div class="col-12 col-md-6">
        <CodeEditor {codeTabs} />
      </div>
      <div class="col-12 col-md-6">
        <div class="code-sample__img-wrapper">
          <img
            class="code-sample__img"
            src="ui-demo.png"
            alt="UI Demo of Skygear Auth SSO" />
        </div>
      </div>
    </div>
  </div>
</section>
