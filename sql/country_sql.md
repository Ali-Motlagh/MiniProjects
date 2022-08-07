## Situation:
Given 3 tables of world; countries, languages and currencies data.
Extract country information like name and langauge and currency 
> for places within the Melanesia or Micronesia regions

## Task:
-- Select fields (with aliases)<p>
SELECT countries.name AS country, region, languages.name AS langauge,
       basic_unit, frac_unit<p>

FROM countries AS c1<p>

 * FULL JOIN languages AS l<p>
 ### * Match on code
    * USING (code)
           

  * FULL JOIN currencies AS c2
         
         
    * USING (code)
       
-- Where region like Melanesia and Micronesia       
       
WHERE region LIKE 'M%esia' ;

## Result:

Kiribati	Micronesia	English	Australian dollar	Cent

