---
keywords: faq;frequently asked questions;analytics for target;a4T;lift;ad hoc;report builder;confidence
description: This topic contains answers to questions that are frequently asked about lift and confidence when using Analytics as the reporting source for Target (A4T).
title: Lift and confidence - A4T FAQ
topic: Standard
uuid: 7d0402f3-d6f2-422e-b69c-86e10120ac83
---

# Lift and confidence - A4T FAQ{#lift-and-confidence-a-t-faq}

This topic contains answers to questions that are frequently asked about lift and confidence when using Analytics as the reporting source for Target (A4T).

## Can I perform offline calculations for A4T? {#section_55B5B750E17D414CAECBEECE27B15D81}

You can perform offline calculations for A4T, but it requires a step with data exports in [!DNL Analytics]. For more information, see "Performing Offline Calculations for Analytics for Target (A4T)" in [Confidence Level and Confidence Interval](../../../c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).

## How is lift calculated? {#section_8CAE788EED5646C4B1D64A0D22070734}

Lift is the percent difference between your control page results and a successful test variant.

## How is confidence calculated? {#section_97DB24D833E742988318CA65DA65DAD9}

The confidence level is the probability that the measured conversion rate differs from the champion page conversion rate for reasons other than chance alone.

## Why can't I see lift and confidence on calculated metrics? {#section_D3E44E24782A409DBD88AE4D1595CB58}

Lift and confidence are not currently supported with calculated metrics. However, in most cases this should not be a problem because the conversion rate calculated in the A4T report is already a calculated metric in which the denominator is the normalizing metric (instances, visits, visitors). For example, if you select the orders metric and the normalization metric is visitors, the conversion rate (orders/visitor) is calculated automatically through A4T reporting. The resulting lift metric reflects the difference in that conversion rate across the text experiences when compared to the default.

Most calcualted metrics for optimization fall into one of two categories: aggregate metrics, and other conversion calculations like Average Order Value (AOV).

Aggregate metrics are used when an organization employs unique events to capture different "flavors" of the save conversion. For instance, if your goal is to promote lead form submissions and you have 10 different lead forms, a company might create unique events to count each type of form conversion. To see the total quantity of all lead forms submitted, they must create a simple calculated metric to add them all together. A better, more modern way to track this is to implement a single lead submission event in Analytics and then use an eVar to collect the type of lead form. Using this method requires fewer variables and eliminates the need to aggregate individual metrics and you still have the ability to see holistic lead form conversion and break it down by type of lead form using the eVar. This also eradicates the need for aggregate metrics when evaluating the performance of a Target Activity.

Another common calculated metric, Average Order Value, is not presently supported with lift & confidence because the normalizing metric is not a standard one (instances, visits, visitors). Instead, the recommendation is to keep an eye on the two influencing metrics of AOV, Revenue Per Visitors and Conversion Rate.

## How does A4T handle confidence calculations? {#section_66115EAF1BA34F7A8FCED7B08DA4F99C}

A4T uses non-binary metric calculations with the sum of square data. The variance is calculated using the sum of squares data. Extreme orders are not taken into account.

Any Analytics segment can be applied to the report. That is how you can get the "extreme order" among other segment options. A metric could also be built to limit things like how many times a visitor converted.

## Do lift and confidence work in Ad Hoc and Report Builder? If it's not native, can I do it in there myself? {#section_D8BB69AE700B4C5CB5FD28DB51F9A4E9}

Lift and confidence do not work in Ad Hoc or Report Builder, and cannot be calculated yourself for continuous variables. It is possible to calculate it manually for binary metrics. 
