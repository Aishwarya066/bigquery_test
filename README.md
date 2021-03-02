# bigquery_test
BUSINESS ANALYTICS ASSIGNMENT
# bigquery_test

SELECT count(*)  FROM `bigquery-public-data.sdoh_cdc_wonder_natality.county_natality` LIMIT 50

SELECT County_of_Residence_FIPS, County_of_Residence,Births  FROM `bigquery-public-data.sdoh_cdc_wonder_natality.county_natality`
order by 
 Births desc LIMIT 50
 
 SELECT Year, County_of_Residence_FIPS, County_of_Residence,Births  FROM `bigquery-public-data.sdoh_cdc_wonder_natality.county_natality`
where
County_of_Residence like '%NC'LIMIT 50

SELECT County_of_Residence,Births,Ave_OE_Gestational_Age_Wks, MAX(Ave_Age_of_Mother) AS MAXIMUM_AGE_OF_MOTHER 	 FROM `bigquery-public-data.sdoh_cdc_wonder_natality.county_natality`
GROUP BY
County_of_Residence,Births,Ave_OE_Gestational_Age_Wks LIMIT 50

SELECT County_of_Residence,Births,Ave_Number_of_Prenatal_Wks	 FROM `bigquery-public-data.sdoh_cdc_wonder_natality.county_natality`
WHERE 
Ave_Number_of_Prenatal_Wks BETWEEN 8 AND 12 LIMIT 50

SELECT County_of_Residence,Births,Ave_Birth_Weight_gms		 FROM `bigquery-public-data.sdoh_cdc_wonder_natality.county_natality`
WHERE 
Ave_Birth_Weight_gms<=3150 LIMIT 50

SELECT Year, County_of_Residence_FIPS, County_of_Residence,Births  FROM `bigquery-public-data.sdoh_cdc_wonder_natality.county_natality`
where
County_of_Residence NOT like '%LA'LIMIT 50

SELECT County_of_Residence_FIPS, County_of_Residence,Births,MIN(Ave_Pre_pregnancy_BMI)	   FROM `bigquery-public-data.sdoh_cdc_wonder_natality.county_natality`
GROUP BY
County_of_Residence_FIPS, County_of_Residence,Births
ORDER BY 
Births 
LIMIT 50

SELECT sum(Ave_Age_of_Mother) as sum_of_avg_age_of_mother, avg(Births) as avg_births	   FROM `bigquery-public-data.sdoh_cdc_wonder_natality.county_natality`
LIMIT 50

SELECT County_of_Residence, Ave_Age_of_Mother	   FROM `bigquery-public-data.sdoh_cdc_wonder_natality.county_natality`
where  
Ave_Age_of_Mother >30 and Ave_Age_of_Mother<35
order by
Ave_Age_of_Mother 
 LIMIT 50
