    MY OWN SIMPLE ORM [Java 8, MySQL 5.0.8]

## ANNOTATION MAPPING


### @interface Table ()
    @RetentionPolicy.RUNTIME
    @ElementType.FIELD

        String  name        default "default"
The @Table annotation can have an optional name argument which specifies the table name. If not specified, the class name with normalized case is used by default.
    

### @interface Column ()
    RetentionPolicy.RUNTIME
    ElementType.FIELD

        boolean primary     default false, 
        String  type        default "int", 
        int     size        default "11"

The @Column annotation can have an optional primary, type and size arguments which specifies the column propetries. If not specified, the class name with normalized case is used by default.

## Main methods 
###### private static void createTable(Class c) throws SQLException 
###### private static void removeTable(Class c) throws SQLException
###### private static void clearTable(Class c) throws SQLException
###### static void insertData(Class c, Object... params) throws SQLException
###### static void printAllData(Class c)
#
###### private static void connect() throws SQLException
###### private static void disconnect()
###### private static void loadDriver() throws SQLException



## Out

        Loading driver...
        Driver loaded!
        Connecting database...
        Database successfully connected!

        id name age
        61 Misha 17
        62 Dima 16
        63 Petya 25
        64 Lenya 21
        65 Dasha 19
        66 Vanya 20

        Database successfully disconnected!

        Process finished with exit code 0
