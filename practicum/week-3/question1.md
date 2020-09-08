1. Create a single Azure Database for PostgreSQL server, name it ISTA495.practicum. [Follow the instructions in this link](https://docs.microsoft.com/en-us/azure/postgresql/quickstart-create-server-database-portal)
2. Ctreat the following table:
  - table name: world
  - table columns: id,country,population,yearlychange,netchange,area,migrants,fertility,medianage,urbanpopulation(id is a number, everything else is a string). 
3. Populate the world table using the csv file included in this folder (use psql in Azure Cloud Shell within the Azure portal to upload the csv file. You can use the \copy command: [example](https://codeburst.io/two-handy-examples-of-the-psql-copy-meta-command-2feaefd5dd90)).
4. Query your Azure database and output the population share (population of the country divided by the population of the world) of the countires.