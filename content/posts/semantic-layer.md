---
title: "The Semantic Layer"
date: 2025-11-08T11:14:18+05:30
draft: false
pinned: false
summary: "The Missing Piece in AI Landscape"
---

![](/8.png)

## What is a Semantic Layer

At this point, even I'm not sure what it is, but I'm going to try to explain it the way I see it. If you read through the materials available online about Semantic Layer, you will see a lot of word salad about bridging the gap between business and technology. Basically, if you've worked on any data/software project, many enterprises have this rift between how the business thinks the data/software works and what the actual reality is on a physical level. This could be how the data is modelled in a database or warehouse, and what the relationships are between those tables. The semantic layer aims to be a 'business-friendly' abstraction that sits between your data platform and end users, such as BI tools, business analysts, etc.

According to me, the Semantic Layer is a logical modelling layer that sits like a **bubble wrapping of "context"** around the data. This means any relevant detail apart from the table / column names and the data itself. For instance, what a particular term means can vary from context to context. e.g., In some contexts, the terms Supplier, Vendor, or Third Party may refer to the same thing, and in others, not so much.

Semantic layers also help in **reducing the complexity of queries** by wrapping up complex aggregation / calculation logic into aliases called **measures**. This is helpful, especially if your data is in the form of a classical dimensional model (star / snowflake), less so if you operate on the one big table approach. These measures and corresponding axes of slicing the data, called dimensions, are usually configured using YAML or JSON, or a drag-and-drop UI interface.

For example if someone asks a question - What is the average revenue per sale per region for our company in the current year. The query using a standard data model may look like

```sql
SELECT
  r.region_name,
  AVG(s.revenue) AS avg_revenue_per_sale
FROM
  sales_fact s
  JOIN region_dim r ON s.region_id = r.region_id
WHERE
  YEAR(s.sale_date) = YEAR(CURRENT_DATE)
GROUP BY
  r.region_name;
```

Whereas on top of a semantic layer the very same query may look like

```sql
SELECT
 region,
 MEASURE(average_revenue)
FROM sales_ytd
GROUP BY region
```

([Here is a good demo](https://www.youtube.com/watch?v=2Qo5_CIsSH4) of building and querying semantic layers by the good folks over at dbt Labs)

## What makes up a Semantic Layer

![](/10.jpg)

Here is a laundry list of the ingredients that may or may not be included in a Semantic layer. (Everything is kind of optional and depends on your level of laziness)

1. **Descriptions** - Rigorous, detailed information on what each table and column means can help non-technical folks and LLMs understand context way better, especially since many times we use short form notations or acronyms in column names, which may confuse people
2.  **Join Keys** - For classic Star / Snowflake schema based data models, its important to understand how the facts and dimension tables join together and what is the relationship like. In case of a one to many relationship between dimensions, there may be additional linkage tables.
3. **Synonyms** - Sometimes the same thing has multiple business terms. This helps identify that those mean the same things and hence have the same metric definition.
4. **Metrics / Measures** - These are pre-defined formulae for common calculations (annual run rate, EBIDTA, turn around time) that are vetted by business analysts.
5. **Dimensions** - These are lines along which you want to slice and dice the data and the metrics. For e.g., region, country, age 
6. **General Information** - Unstructured information on business processes, SOPs are unique to your specific industry or company.

## Why is it back in Fashion

While the Semantic layer is a pretty old concept and has existed in the Legacy BI world for eons in tools like Power BI, It has seen a renaissance in recent times due to the craze of Text2SQL-based chatbots. In simple terms, everyone is building these chatbots that convert natural language queries into SQL queries and then fire that onto a data platform and report back the answers in tabular format or using visualizations automatically. These Chatbots usually do great in demos where the schema has a couple of long tables, but as soon as you go for any kind of complex data model, these LLMs fumble miserably. They select wrong columns, join keys, and apply incorrect WHERE clauses which result in garbage output. Here's where Semantic layers come into play by providing more context to LLM, hence helping it make more informed choices when formulating queries.

## Where Do you put it

![](/9.jpg)

Once you decide that you NEEEEED a semantic layer, the next logical question is where and how do you build one. As I mentioned earlier, Semantic modelling has existed in BI tools like Power BI (and more recently Tableau) since some time. But the proprietary nature of these tools means these layers cannot be easily exposed freely outside of the BI tools themselves, which is required for connecting the semantic layer to new age data apps or AI-based chatbots. 

Good thing for us is that many companies have realized the value of Semantic layers in the era of AI and have already built (or are starting to build) these functionalities on various levels of the data stack. As a good rule of thumb, it should definitely **NOT** be tightly coupled with your BI tool. So it has to sit somewhere in between your data platform (physical model) and your end consumer (AI / BI)

If you have a pile of extra money to burn, there are a ton of good standalone solutions that could be inserted into your stack. These would connect to your data platform of choice and allow Analysts to configure semantics using SQL and a very slick drag-and-drop UI. They also often have inbuilt dashboarding capabilities, but also have connectors for popular BI tools. 

If you are money-conscious and hence want to opt for an open source solution, then there are a few directions to go. If your data platform is not one of the big modern ones like Databricks, Snowflake, or DBT, which support Semantic modelling inherently, then a separate tool would be required. (Running Postgres / SQL server warehouses, I am talking about you).

If you don't have a pile of extra money to burn because you already burned all your money on the modern hyper-scaler data platforms like Databricks, Snowflake, or dbt, then its better to stick with their in-build solution for the Semantic layer creation. Databricks does this in  an open source manner (kind of) inside of Unity Catalog using Metric views. DBT has also fully open-sourced their semantic layer implementation called MetricFlow. Yet when on these platforms, the open source solutions are well managed for you, hence making them extremely easy to get started with.

## People are still Skeptical

As I said, semantic layers have been around forever in the BI world, but haven't really made it big outside the data community. Maybe because there is no precise definition of the concept. Every vendor has their own take and implementation without any standardization whatsoever. Hence, we have separate syntax and mechanisms for each implementation. There has been some headway in this direction recently. Snowflake has brought together a new consortium called [the Open Semantic Interchange (OSI)](https://www.snowflake.com/en/blog/open-semantic-interchange-ai-standard/) that is supposed to bring standardization in this space. The consortium consists of some big names like dbt Labs, Mistral AI, Salesforce, Thoughtspot, and Cube, but is lacking in many notable ones too, like Databricks, Microsoft, and OpenAI. What comes of this is yet to be seen, but these are surely exciting times indeed. 
