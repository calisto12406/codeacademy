# codeacademy

# world population SQL merge tables project

SELECT COUNT(*) FROM  countries
GROUP BY  continent
HAVING continent = 'Africa';

SELECT SUM(population) FROM countries
JOIN population_years
	ON  countries.id = population_years.country_id
WHERE continent = 'Oceania'
AND year = '2005';

SELECT AVG(population) FROM countries
JOIN population_years
	ON  countries.id = population_years.country_id
WHERE continent = 'South America'
AND year =  '2003';

SELECT name, population FROM countries
JOIN population_years
	ON  countries.id = population_years.country_id
WHERE year = '2007'
AND population IS NOT NULL
ORDER BY population ASC
LIMIT 1;

SELECT AVG(population) FROM countries
JOIN population_years
	ON  countries.id = population_years.country_id
WHERE name = 'Poland';

SELECT COUNT(*) FROM countries
WHERE name LIKE '%The%';

SELECT continent, SUM(population_years.population) FROM countries
JOIN population_years
	ON  countries.id = population_years.country_id
GROUP BY continent;






