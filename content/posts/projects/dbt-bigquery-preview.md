+++
title = 'dbt-bigquery-preview'
date = 2024-06-24
draft = false
description = 'A VS Code extension for analytics engineers.'
+++

Two years ago, I found myself missing a functionality in VS Code that could ease the user experience of analytics engineers that used [dbt](https://www.getdbt.com/), [Google BigQuery](https://cloud.google.com/bigquery), and VS Code. At the time, the possible paths were either:
1. Choose to compile dbt code and test its output in BQ.
	1. Compile dbt code in VS Code.
	2. Take the compiled code and paste it in BigQuery.
	3. Execute and iterate over result.
2. Choose to execute in BQ and adapt to dbt.
	1. Compile raw SQL in BQ, iterate until it works.
	2. Adapt raw SQL so it follows dbt standards.

So, I decided to build a VS Code extension that compiled the dbt code into raw SQL, sent the SQL over to the BigQuery API, received the results, and showed the results in a SQL-familiar way, as a table.

The extension has been unmaintained for some time, as I didn't actually use it at work: the dbt compiler was too slow (our repo had ~5k models, and partial parsing still was far from optimized at the time) to make the UX of the extension attractive, so I kept going by the option 2 outlined above.

Still, people used it, so it remains published. At the time of this writing, it has ~1.5 downloads in VS Code.

[Here is the extension](https://marketplace.visualstudio.com/items?itemName=jjuanramos.dbt-bigquery-preview).