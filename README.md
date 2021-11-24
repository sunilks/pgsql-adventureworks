# pgsql-adventureworks
Adventureworks that works for PostgreSQL - Awesome database!

This takes care of running the ruby scripts & I have tested this on the latest Postgres DB.

## Installation:
1. Download your fav version of PostgreSQL & keep note of your main id & password.
2. Check the version by opening a CMD or Powershell.

    ```psql --version```

3. Choose your psql username or create one for this database.

    ```psql -U <main_id>```

4. Enter the password for <main_id>.

5. Once you have logged into the psql, if you need to create a username specific for the DB; use:

    ```psql -U <main_id> -c "CREATE USER <username>"```

6. Create the Adventureworks database.

    ```psql -U <main_id> -c "CREATE DATABASE \"Adventureworks\";"```

7. Grant permission to the chosen (or created) username to the database.

    ```psql -U <main_id> -c "GRANT ALL PRIVILEGES ON DATABASE "Adventureworks" TO <username>"``` 

8. Exit the psql.
9. Run the command so (replace <username> with the chosen or created username). 
  
    ```psql -U <username> -d Adventureworks < install.sql```

10. If you see no errors and something like the below, then you are all set!
    ```
    . . . .                                                         
    sales          | salestaxrate                          | table | docker
    sales          | salesterritory                        | table | docker
    sales          | salesterritoryhistory                 | table | docker
    sales          | shoppingcartitem                      | table | docker
    sales          | specialoffer                          | table | docker
    sales          | specialofferproduct                   | table | docker
    sales          | store                                 | table | docker
    
    (68 rows)
    ```
11. Enjoy!
                                                            
