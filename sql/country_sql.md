## Situation:
Given 3 tables of world; countries, languages and currencies data.
Extract country information like name and langauge and currency 
> for places with either Melanesia or Micronesia

## Task:
-- Select fields (with aliases)<p>
SELECT countries.name AS country, region, languages.name AS langauge,<p>
       basic_unit, frac_unit<p>
-- From countries (alias as c1)<p>
FROM countries AS c1<p>
  -- Join with languages (alias as l)<p>
  FULL JOIN languages AS l<p>
    -- Match on code
    USING (code)
  -- Join with currencies (alias as c2)<p>
  FULL JOIN currencies AS c2
    -- Match on code
    USING (code)
       
-- Where region like Melanesia and Micronesia
       
       
WHERE region LIKE M%esia';

## Result:
country	region	language	basic_unit	frac_unit
Kiribati	Micronesia	English	Australian dollar	Cent
Kiribati	Micronesia	Kiribati	Australian dollar	Cent
Marshall Islands	Micronesia	Other	United States dollar	Cent
Marshall Islands	Micronesia	Marshallese	United States dollar	Cent
