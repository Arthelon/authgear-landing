<script>
  export let title = "";
  export let description = "";
  export let features = [];
  export let buttonText = "";
  export let buttonHref = "";
</script>

<style>
  .pricing-card {
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 100%;
    padding: 20px;
    background-color: #fff;
    box-shadow: 0 40px 50px rgba(0, 0, 0, 0.2);
    border-radius: 15px;
  }

  .pricing-card__title {
    font-size: 28px;
    font-weight: 700;
    margin-top: 0;
    margin-bottom: 8px;
    line-height: 1.4;
  }

  .pricing-card__description {
    flex-grow: 1;
    font-size: 15px;
    line-height: 28px;
    color: #000;
    margin-top: 0;
    margin-bottom: 16px;
  }

  .pricing-card__feature-list {
    list-style: none;
    margin: 0;
    padding: 0;
  }

  .pricing-card__feature-list__item {
    font-size: 11px;
    line-height: 1.6;
    color: #666;
    border-bottom: 1px solid #d8d8d8;
    padding: 10px 0;
  }

  .pricing-card__footer {
    height: 100px;
    padding-top: 36px;
    vertical-align: middle;
  }

  .pricing-card__footer__btn {
    display: inline-block;
    vertical-align: middle;
    padding: 14px 16px;
    border: 1px solid transparent;
    border-radius: 0;
    transition: background-color 0.25s ease-out, color 0.25s ease-out;
    font-size: 15px;
    line-height: 1;
    text-align: center;
    cursor: pointer;
    width: 100%;
    background-color: #166bef;
    color: #fff;
  }

  .pricing-card__footer__btn:hover {
    background-color: #14679e;
  }
</style>

<div class="pricing-card">
  <h3 class="pricing-card__title">{title}</h3>
  <p class="pricing-card__description">{description}</p>
  <ul class="pricing-card__feature-list">
    {#each features as featureText}
      <li class="pricing-card__feature-list__item">{featureText}</li>
    {/each}
  </ul>
  <div class="pricing-card__footer">
    {#if buttonText && buttonHref}
      <a class="pricing-card__footer__btn" target="_blank" href={buttonHref}>
        {buttonText}
      </a>
    {/if}
  </div>

</div>
