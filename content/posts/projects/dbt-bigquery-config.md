+++
title = 'Tutorial on configuring dbt and BigQuery'
date = 2024-06-24
draft = false
description = 'Introduction on using dbt and BigQuery together.'
+++

In 2020, I built the Data Warehouse for the [startup I was working at](https://www.homyspace.com/en/). When I first started doing so, I couldn't find any valuable resource about how to properly configure it.

I wanted something akin to what Jeremy Cohen layed out on [his now classic article](https://www.getdbt.com/blog/how-we-configure-snowflake): setting up different warehouses (or databases) for different purposes, having dev and prod environments, as well as an environment where the raw data existed, independently of the other two. This provides Role Based Access by default and a clean structure.

Jeremy Cohen's article was focused on [Snowflake](https://www.snowflake.com/en/), mine's tried to adapt his to BigQuery. I think it turned out okay, with ~3k views as of now.

Anyways, [here's the link!](https://towardsanalyticsengineering.substack.com/p/how-to-configure-dbt-projects-in).