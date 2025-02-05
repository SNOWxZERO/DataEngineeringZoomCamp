### Quiz Questions
Complete the Quiz shown below. It’s a set of 6 multiple-choice questions to test your understanding of workflow orchestration, Kestra and ETL pipelines for data lakes and warehouses.

---

1. Within the execution for `Yellow` Taxi data for the year `2020` and month `12`: what is the uncompressed file size (i.e. the output file `yellow_tripdata_2020-12.csv` of the `extract` task)?

- <span style="background:#d3f8b6">128.3 MB</span>
- 134.5 MB
- 364.7 MB
- 692.6 MB

**Solution:** 
After running the gcp_taxi flow as in this screenshot:
![[Pasted image 20250205144916.webp]]
we can see the file uploaded in the bucket as follows:
![[Pasted image 20250205145058.webp]]
then the answer is : `128.3` 

---

2. What is the rendered value of the variable `file` when the inputs `taxi` is set to `green`, `year` is set to `2020`, and `month` is set to `04` during execution?

- `{{inputs.taxi}}_tripdata_{{inputs.year}}-{{inputs.month}}.csv`
- <span style="background:#d3f8b6">green_tripdata_2020-04.csv</span>
- `green_tripdata_04_2020.csv`
- `green_tripdata_2020.csv`

**Solution:**
Investigating the output we see this in extract task:
![[Pasted image 20250205150854.webp]]
then the answer is : `green_tripdata_2020-04.csv`

---

3. How many rows are there for the `Yellow` Taxi data for all CSV files in the year 2020?

- 13,537.299
- <span style="background:#d3f8b6">24,648,499</span>
- 18,324,219
- 29,430,127

**Solution:**
After running backfill triggers for whole 2020 year for yellow taxi data and investigating the table
![[Pasted image 20250205160951.webp]]
then the answer is: `24,648,499` 

---

4. How many rows are there for the `Green` Taxi data for all CSV files in the year 2020?

- 5,327,301
- 936,199
- <span style="background:#d3f8b6">1,734,051</span>
- 1,342,034

**Solution:**
After running backfill triggers for whole 2020 year for green taxi data and investigating the table
![[Pasted image 20250205160714.webp]]
then the answer is : `1,734,051`

---

5. How many rows are there for the `Yellow` Taxi data for the March 2021 CSV file?

- 1,428,092
- 706,911
- <span style="background:#d3f8b6">1,925,152</span>
- 2,561,031

**Solution:**
After running gcp_taxi flow for yellow taxi data and investigating the table of 2021-03
![[Pasted image 20250205161415.webp]]
then the answer is: `1,925,152` 

---

6. How would you configure the timezone to New York in a Schedule trigger?

- Add a `timezone` property set to `EST` in the `Schedule` trigger configuration
- <span style="background:#d3f8b6">Add a timezone property set to America/New_York in the Schedule trigger configuration</span>
- Add a `timezone` property set to `UTC-5` in the `Schedule` trigger configuration
- Add a `location` property set to `New_York` in the `Schedule` trigger configuration

**Solution:**
Answered from the documentation
![[Pasted image 20250205162442.webp]]
![[Pasted image 20250205162523.webp]]

---
