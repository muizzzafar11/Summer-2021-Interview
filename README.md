## Repository
- For clone; https://github.com/muizzzafar11/DIY_Recipe.git
- https://github.com/muizzzafar11/DIY_Recipe



## Setting up the Database
- Type the following command to get to the root directory
  `cd DIY_Recipe/recipeDIY`
- Now, in PSQL shell, run the following command to create a db: 
  `CREATE DATABASE franksdb;`
- Now run the following command in the PSQL shell to create a new user with default password:
`CREATE ROLE frank WITH LOGIN PASSWORD '<yourpassword>'`
- Now run the following command to grant access on db to the new user:
`GRANT ALL PRIVILEGES ON DATABASE franksdb TO frank;`
- Now update the appsettings.json file "RecipeDiyDbContextConnection" with your password
- Now run migrations using the following command: 
`dotnet ef database update;`

## Instructions on how to use
Before running the project, make sure to replace:
`options.ClientId = "";`
`options.ClientSecret = "";`
in the Startup.cs.ConfigureServices() (Line 56 and 57 with the following (google secret id and key):
`options.ClientId = "1040469150781-818sqf06rp2e2ckq5ek04b9dmgq4f9ul.apps.googleusercontent.com";`
`options.ClientSecret = "DyNrMYW8r634wsYcnTXj5ayi";`

When you run the project using `dotnet run` or any IDE, it will lead you to a page web page. Please Register using google or your email and password before going to any of the other pages. 

You can see all of the recipes created by the current user on the MyRecipe page, create new recipes, and delete them.


