# This is not a fully fleshed-out tutorial

01. Select the **SQL Server** extension.

01. Select **Add connection**.

01. In the dialog, use these values for each setting prompt:

    | | Value |
    | --- | --- |
    | **Server name** | `sql` |
    | **Database name** | *N/A* |
    | **Authentication type** | *SQL login* |
    | **User name** | `sa` |
    | **Password** | `Passw0rd` |
    | **Save password** | *No* |
    | **Profile name** | *N/A* |

01. *This step should probably have you create a new user account and reconnect. 🤷*

01. Open the context menu for the server node and select **New query**. 

01. Run this query (select the arrow icon):

    ```sql
    CREATE DATABASE Test;
    ```

01. Expand the **Databases** folder, open the context menu for the **Test** database node, and then select **New query**.

01. Run these queries:

    - Create the **Inventory** table:

        ```sql
        CREATE TABLE Inventory (id INT, name NVARCHAR(50), quantity INT);
        ```

    - Insert two values into the table:

        ```sql
        INSERT INTO Inventory VALUES (1, 'banana', 150); 
        INSERT INTO Inventory VALUES (2, 'orange', 154);
        ```

    - Query for one of the values:

        ```sql
        SELECT * FROM Inventory WHERE quantity > 152;
        ```

01. Expand the **Test** database, expand the **Tables** folder, open the context menu for the **Inventory** table node, and then select **Select Top 1000**.