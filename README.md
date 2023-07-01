# ITC-MyAQL-Basic
SELECT *
  FROM tutorial.us_housing_units
  
  SELECT year as Year, month as Month, month_name as Month_Name, south as South, west as West,
  midwest as Midwest, northeast as Northeast FROM tutorial.us_housing_units
  
  SELECT *
  FROM tutorial.us_housing_units
  LIMIT 15
  
  SELECT *
  FROM tutorial.us_housing_units
  WHERE month = 1
  
    SELECT *
  FROM tutorial.us_housing_units
  where west > 50
  
    SELECT *
  FROM tutorial.us_housing_units
  where south <= 20
  
    SELECT *
  FROM tutorial.us_housing_units
  where month_name = 'February'
  
    SELECT *
  FROM tutorial.us_housing_units
  where month_name < 'o'
  
    SELECT year as Year, month as Month, month_name as Month_Name, south as South, west as West,
  midwest as Midwest, northeast as Northeast,
  south + west + midwest + northeast as Sum FROM tutorial.us_housing_units 
  
    SELECT *
  FROM tutorial.us_housing_units
  where west > midwest + northeast
  
      SELECT year, month_name, (south/(west + midwest + south + northeast)) * 100 as "south%",
      (west/(west + midwest + south + northeast)) * 100 as "west%",
      (midwest/(west + midwest + south + northeast)) * 100 as "midwest%",
      (northeast/(west + midwest + south + northeast)) * 100 as "northeast%"
  FROM tutorial.us_housing_units
  where year >= 2000
  
  SELECT * FROM tutorial.billboard_top_100_year_end
  
  SELECT *
  FROM tutorial.billboard_top_100_year_end
 ORDER BY year DESC, year_rank
 
   SELECT *
  FROM tutorial.billboard_top_100_year_end
  where group_name like '%Ludacris%'
 

  
      SELECT *
  FROM tutorial.billboard_top_100_year_end
  where group_name like '%Hammer%'
  
  SELECT *
  FROM tutorial.billboard_top_100_year_end
 WHERE group_name IN ('M.C. Hammer', 'Hammer', 'Elvis Presley')
 
   SELECT *
  FROM tutorial.billboard_top_100_year_end
  where year between 1985 and 1990

   SELECT *
  FROM tutorial.billboard_top_100_year_end
  where song_name is NULL
  
   SELECT *
  FROM tutorial.billboard_top_100_year_end
  where year_rank <=10 and  group_name like '%Ludacris%'
  
     SELECT *
  FROM tutorial.billboard_top_100_year_end
  where year_rank = 1 and year in (1990, 2000, 2010)
  
       SELECT *
  FROM tutorial.billboard_top_100_year_end
  where year between 1960 and 1969
  and  song_name ilike '%Love%'
  
       SELECT *
  FROM tutorial.billboard_top_100_year_end
  where year_rank <= 10
  and (group_name ilike '%katy perry%' OR group_name ilike '%bon jovi%')
  
       SELECT *
  FROM tutorial.billboard_top_100_year_end
  where song_name ilike '%California%'
  and ((year >=1970 and year <=1979)or (year >=1990 and year <=1999))
  
         SELECT *
  FROM tutorial.billboard_top_100_year_end
  where group_name like '%Dr. Dre%' and (year < 2001 or year > 2009)
  
           SELECT *
  FROM tutorial.billboard_top_100_year_end
  where year = 2013 and song_name not like '%a%'
  
             SELECT *
  FROM tutorial.billboard_top_100_year_end
  where year = 2012
  order by song_name DESC
  
               SELECT *
  FROM tutorial.billboard_top_100_year_end
  where year = 2010
  order by year_rank, artist
  
               SELECT *
  FROM tutorial.billboard_top_100_year_end
  where group_name ilike '%T-Pain%'
  order by year_rank DESC
  
                 SELECT *
  FROM tutorial.billboard_top_100_year_end
  where year_rank between 10 and 20 -- this will display songs ranked from 10 to 20
  and year in(1993,2003,2013) -- this will display only song in 1993,2003 and 2013
  order by year, year_rank
