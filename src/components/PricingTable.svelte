<script>
  import PricingTableCard from "./PricingTableCard.svelte";

  const pricingCards = [
    {
      title: "Free",
      description:
        "Use all features of Authgear to boost your app's security and develop faster",
      features: [
        "1,000 Monthly Active Users",
        "1 Day of Log Retention",
        "Account remove if no activities for 60 days",
        "No SLA",
        "Community Support",
      ],
    },
    {
      title: "Startups",
      description: "Grow without pain and security",
      features: [
        "1,000 Monthly Active Users",
        "Up to 10 Days of Log Retention",
        "AD, LDAP, SAML support",
        "Passwordless Login / Verify by SMS",
        "Email Support",
      ],
      pricingText: "USD 200",
      pricingSubtext: "+USD 20 per 1000 Monthly Active Users",
    },
    {
      title: "Enterprise",
      description: "Run Authgear for your mission-critical applications",
      features: [
        "Managed SaaS or Private Cloud Deployment",
        "Enterprise Grade SLA support",
        "Professional Support and Services",
        "Anomaly Detection",
        "Audited Reports",
      ],
      buttonText: "Pricing: Contact Us",
      buttonHref: "mailto:hello@skygear.io",
    },
  ];
</script>

<style>
  .pricing-table {
    background: #0043e0;
    width: 100%;
  }

  .container-fluid {
    max-width: 1200px;
  }

  .pricing-table__card-wrapper {
    margin-top: 10px;
    margin-bottom: 10px;
  }

  @media screen and (min-width: 768px) {
    .pricing-table {
      padding-top: 110px;
      padding-bottom: 110px;
    }

    .container-fluid {
      padding-left: 56px;
      padding-right: 56px;
    }
  }

  @media screen and (max-width: 768px) {
    .pricing-table {
      padding-top: 30px;
      padding-bottom: 30px;
    }

    .container-fluid {
      padding-left: 29px;
      padding-right: 29px;
    }
  }
</style>

<section class="pricing-table">
  <div class="container-fluid">
    <div class="row">
      {#each pricingCards as card}
        <div class="col-12 col-md-4 pricing-table__card-wrapper">
          <PricingTableCard {...card} />
        </div>
      {/each}
    </div>
  </div>
</section>
