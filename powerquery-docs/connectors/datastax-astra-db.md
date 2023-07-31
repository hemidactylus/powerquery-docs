---
title: Power Query DataStax Astra DB Connector
description: Provides description, prerequisites and instructions on how to connect to your Astra DB instance from Power Query, both locally and in cloud services such as Power BI Service.
author: Stefano Lottini
ms.topic: conceptual
ms.date: 8/1/2023
ms.author: hemidactylus
---

# DataStax Astra DB

>[!Note]
>The following connector article is provided by DataStax, the owner of [this connector](https://github.com/datastax/powerquery_astra_db_connector) and a member of the Microsoft Power Query Connector Certification Program. If you have questions regarding the content of this article or have changes you would like to see made to this article, visit the [DataStax](https://www.datastax.com) website and use the support channels there.

## Summary

| Item | Description |
| ------- | ------------|
|Release state | Beta |
| Products supported | <br/>Power BI Desktop<br/>Power BI Service<br/> |
| Authentication Types Supported | Feed Key (Astra DB Token) |
| Function Reference Documentation | &mdash; |

> [!NOTE]
> Some capabilities may be present in one product but not others due to deployment schedules and host-specific capabilities.

## Prerequisites

- An [Astra account](https://astra.datastax.com) with a running DB instance.
- You need the following connection parameters: Database ID and Database Region.
- The following credentials are needed: a valid [Database Token](https://docs.datastax.com/en/astra-serverless/docs/manage/org/manage-tokens.html) with permission to read tables and keyspaces through the REST API.

## Capabilities supported

* Browse keyspaces and tables
* Import table data

## Connect to DataStax Astra DB from Power Query Desktop

To connect to an Astra DB table from Power Query Desktop, follow these steps:

1. Select the **Astra DB (Beta)** option in the connector selection.

2. In the connection parameters dialog, provide the Database ID and Region, then click "OK".

3. Provide the Database Token if asked by the "Feed Key" dialog. The token is the string starting with `AstraCS:...`.

4. In the **Navigator** view you can now browse the keyspaces in the database and the tables in each keyspace. Note that, should your token prevent access to some keyspaces, these will still be visible but will list no tables in them.

5. Choose a table, then choose either **Load** or **Transform Data** (depending whether you need the table data as is or you want to apply further post-load transformations).

## Connect to DataStax Astra DB from Power Query Online

To connect to an Astra DB table from Power Query Online, take the following steps:

1. Select the **Astra DB (Beta)** option in the connector selection.

2. When asked, provide the connection parameters: the ID and Region of your database.

3. If this is the first time you're connecting to this database, you need to provide credentials: select the "Key" authentication method and input your `AstraCS:...` token string as the "Account key".

4. If necessary, select the name of your on-premises data gateway.

5. In **Navigator**, select the data you require, and then select **Transform data**, much like in the Power BI Desktop flow above.

## Troubleshooting

For more information and troubleshooting help, please consult the [Awesome Astra page](https://awesome-astra.github.io/docs/pages/tools/integration/microsoft-powerquery) about this connector.
