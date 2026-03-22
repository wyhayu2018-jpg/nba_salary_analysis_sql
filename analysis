
-- Query 1. Top 20 Highest Paid Players by Position and Team 
Business question: Who are the top 20 highest paid players and what position and team are they on?
SELECT a.name, b.salary, a.position, b.team
FROM players a
JOIN salaries b 
ON a._id = b.player_id
ORDER BY b.salary DESC
LIMIT 20;


-- Query 2. Average Salary by Position
-- Business question: Which positions earn the most on average?
SELECT a.position, 
ROUND(AVG(b.salary), 2) AS avg_salary 
FROM players a
JOIN salaries b 
on a._id = b.player_id
GROUP BY a.position
ORDER BY avg_salary DESC
LIMIT 10;


-- Query 3. Teams with the Highest Total Payroll
-- Business question: Which teams spend the most on player salaries?
SELECT b.team, 
SUM(b.salary) AS total_payroll
FROM players a
JOIN salaries b 
ON a._id = b.player_id
GROUP BY b.team
ORDER BY total_payroll DESC
LIMIT 10;

 
-- Query 4. Average Salary Growth Season Over Season
-- Business question: How have average salaries trended over time?
SELECT b.season,
ROUND(AVG( b.salary), 2) AS avg_salary
FROM players a
JOIN salaries b
ON a._id = b.player_id
GROUP BY b.season
ORDER BY b.season ASC;

-- Query 5. Colleges Producing the Highest Earning NBA Players
-- Business question: Which colleges produce the highest earning NBA players on average?
SELECT a.college,
ROUND(AVG( b.salary), 2) AS avg_salary,
COUNT(a.name) AS player_count
FROM players a
JOIN salaries b
ON a._id = b.player_id
GROUP BY a.college
ORDER BY avg_salary DESC
LIMIT 20;


