# Create a Mongo Database

The PetSitly marketing team is trying to get more organized. They have customer information stored in a bunch of different files, and that's making everyone feel stressed!

In this activity, you’ll help calm them down by first creating a Mongo database for them and then moving their customer list, which is a JSON file, into a collection within that database.

## Instructions

1. If you haven’t already started Mongo, start it. To do so on Windows, run `mongod`. To do so on macOS, run `brew services start mongodb/brew/mongodb-community`.

2. In the terminal, use `cd` to navigate to the `Resources` folder that contains the `customer_list.json` file.

3. Use the following command to import this file into a Mongo database:

    ```bash
    mongoimport --type json -d petsitly_marketing -c customer_list --drop --jsonArray customer_list.json
    ```

    **Hint:** For more information about importing JSON files into Mongo, refer to [mongoimport](https://docs.mongodb.com/database-tools/mongoimport/#mongoimport) in the MongoDB documentation.

4. Create an instance of MongoClient by using Port Number 27017.

5. List the database names to confirm that the `petsitly_marketing` database was created. 

6. Assign the `petsitly_marketing` database to a variable.

7. List the names of the collections in the database. 

    **Hint:** Be sure to use the name of the variable that you assigned your database to.

8. Use the `find_one` function to review a document in the `customer_list` collection of your database.

9. Assign the `customer_list` collection to a variable of your choice.

10. Use the `insert_one` function to insert the new customer into the database, and then run the query in the following cell to review this customer.

11. Create a query that will find all the customers who have turtles as pets.

## Bonus (Optional)

Try running queries to find out the other types of animals that customers have. To do so, complete the following steps:

1. Use the `delete_many` function to delete the customers that have turtles. Then query the database to confirm that this worked.

2. Use `drop_collection` to delete the collection, and then use `list_collection_names` to confirm that this worked.

3. Use `drop_database` to delete your database. Then use `list_database_names` to confirm that this worked.

---

© 2022 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
