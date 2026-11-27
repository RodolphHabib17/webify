# Webify — Payment Provider Research

**Version:** 1.0  
**Date:** November 27, 2026  
**Status:** Preliminary Research — Provider Approval Pending

## 1. Objective

Identify payment providers that may support a business operating in Lebanon and determine a practical payment approach for Webify's MVP.

## 2. Provider Comparison

| Provider | Findings | Research status |
|---|---|---|
| MyMonty / Monty Finance | Published Lebanese online acquiring service with USD and LBP transaction and settlement currencies | Strong local candidate |
| PayTabs | Published market checklist includes Lebanon and lists card payment support | Current onboarding and terms require confirmation |
| Stripe | Lebanon is not listed as a supported business account country | Not suitable for a Lebanese-registered merchant account at present |

## 3. MyMonty Findings

The Monty Finance Payment Gateway Key Facts Statement, version 1.0 dated October 21, 2026, publishes the following information:

### Eligibility
- Merchant must be a duly registered entity or licensed individual.
- Merchant transaction limits depend on business activity and pricing.

### Currencies
- Transaction currencies: USD and LBP.
- Settlement currencies: USD and LBP.

### Published fees
- Initial setup: USD 150 per domain.
- Monthly maintenance: USD 35 per domain.
- Local cards: 2%.
- International cards: 3.5%.
- Supported digital wallets: 1.5%.
- Processing: USD 0.30 per transaction.
- Payout to MyMonty Business account: free.
- Payout to bank account: subject to the selected acquiring bank's fees.

### Settlement
- Card settlement cycle: transaction date + 2 days, depending on the settlement account.
- Supported digital wallet payouts: weekly.

### Payment methods and integration
- Visa, Mastercard and American Express.
- Supported digital wallets, including Whish Money in Lebanon.
- API and supported platform integrations.
- 3D Secure authentication may apply.

### Official references
- https://mymonty.com.lb/business/online-payment-gateway
- https://mymonty.com.lb/kfs/Payment-Gateway-KFS.pdf

## 4. PayTabs Findings

A published PayTabs market checklist includes Lebanon and lists Visa and Mastercard support, with LBP, USD and other currencies indicated.

However, the available checklist is not sufficient to confirm current Lebanese merchant onboarding or commercial terms.

Official reference:
https://site.paytabs.com/wp-content/uploads/2015/12/Paytabs-Market-Checklist.pdf

Required follow-up:
- Confirm whether a Lebanon-registered business can open a merchant account.
- Confirm settlement currencies and bank requirements.
- Request current fees and setup costs.
- Confirm API access and integration documentation.
- Confirm supported business categories.

## 5. Stripe Findings

Lebanon is not included in Stripe's published list of supported business account countries.

Webify should not plan on opening a standard Stripe account using only a Lebanese business registration.

Official references:
- https://stripe.com/global
- https://support.stripe.com/questions/requirements-to-open-a-stripe-account-in-another-country

## 6. Recommended MVP Approach

**First choice for investigation:** MyMonty.

Before implementation, Webify must:
1. Contact the provider.
2. Explain that Webify sells website templates and website development/customization services.
3. Confirm that the business model is accepted.
4. Confirm required business registration and KYC documents.
5. Obtain current commercial terms.
6. Request API documentation and sandbox/demo access.
7. Confirm settlement and refund procedures.

**Fallback:** An administrator-managed payment confirmation workflow may be used if online integration is not ready, provided the selected method is legally and operationally acceptable.

## 7. Technical Requirements

The backend should use a payment-provider adapter so that the application is not tightly coupled to one provider.

The system should:
- Store payment records separately from orders.
- Track pending, successful, failed and refunded statuses where supported.
- Verify payment notifications.
- Prevent duplicate transaction processing.
- Never store raw card details.
- Record provider transaction references.
- Allow administrators to review payment status.

## 8. Final Decision

MyMonty is the strongest locally evidenced candidate found in this preliminary research.

No provider is approved for production integration yet. The final decision depends on merchant eligibility, written commercial terms, API access, and successful testing.

**Research owner:** Webify Project Team  
**Status:** Preliminary research completed; provider confirmation pending.