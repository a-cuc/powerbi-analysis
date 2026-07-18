# Examining Market Data with Power BI
A project combining e-commerce data and consumer statistics for a report
- Consumer statistics extracted from the [PSA CPI and Inflation Report](https://psa.gov.ph/price-indices/cpi-ir)
- E-commerce data sourced from [Kaggle](https://www.kaggle.com/datasets/muhammadaammartufail/global-e-commerce-sales-and-customer-data)


## Trying it out locally

The consumer statistics are imported to the Power BI thru the github repository, so the CPI Page should work as is, for the E-commerce data:

Create Postgres database
```sh
createdb -T template0 ecommerce
psql -X ecommerce < /data/ecommerce.sql
```

Run docker container
```sh
docker-compose up -d
```

Power BI has the following connection settings set up for the data:
| Parameter | Value |
| --- | --- |
| Server | localhost:5432 |
| Database | ecommerce |
| Username | postgres |
| Password | admin |

> [!NOTE]
> The username `postgres` is the default superuser, and using another user than this is ideal
