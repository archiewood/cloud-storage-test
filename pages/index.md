```sql test
select * from read_csv_auto('https://api.fiscaldata.treasury.gov/services/api/fiscal_service/v2/accounting/od/avg_interest_rates?format=csv&filter=record_date:gte:2015-12-31,security_desc:in:Treasury%20Bills')
```


<DataTable data={test} />

<LineChart 
  data={test} 
  x=record_date
  y=avg_interest_rate_amt
  series=security_desc
  title="Treasury Bill Interest Rates"
  yFmt='#"%"'
/>
