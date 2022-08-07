## Situation:
Given 3 tables of world; countries, languages and currencies data.
Extract country information like name and langauge and currency 
> **within Melanesia or Micronesia regions**

## Task:
-- Select fields (with aliases)<p>
-- Full join 3 tables (key: code) <p>
-- Look for Melanesia or Micronesia ('M%esia') <p>     
<b>SELECT countries.name AS country, region, languages.name AS langauge,
       basic_unit, frac_unit<p>

FROM countries AS c1<p>

   * FULL JOIN languages AS l 
       
        * USING (code) 
           
   * FULL JOIN currencies AS c2
          
        * USING (code) 
             
       
WHERE region LIKE 'M%esia' ;</b>

## Result:
       country	region	     language	 basic_unit	       frac_unit
       Kiribati	Micronesia   English	 Australian dollar	Cent

