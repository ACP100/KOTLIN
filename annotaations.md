examples #annotations 

| Annotation        | Where used            | What it does                                          | Who uses it             |
| ----------------- | --------------------- | ----------------------------------------------------- | ----------------------- |
| `@Composable`     | Functions             | Marks a function as UI in Jetpack Compose             | Compose compiler        |
| `@Preview`        | Functions             | Shows UI preview in Android Studio                    | Android Studio          |
| `@Inject`         | Constructors / fields | Tells DI framework to automatically provide object    | Hilt / Dagger           |
| `@Module`         | Classes               | Defines dependency provider container                 | Hilt / Dagger           |
| `@Provides`       | Functions             | Supplies custom objects to DI system                  | Hilt / Dagger           |
| `@Singleton`      | Classes / providers   | Makes one shared instance (single object)             | Hilt / Dagger           |
| `@Entity`         | Classes               | Marks a Room database table                           | Room                    |
| `@Dao`            | Interfaces            | Marks database access object                          | Room                    |
| `@Query`          | Functions             | Defines SQL query in Room                             | Room                    |
| `@GET`            | Functions             | Defines HTTP GET request                              | Retrofit                |
| `@POST`           | Functions             | Defines HTTP POST request                             | Retrofit                |
| `@Body`           | Parameters            | Sends request body in API call                        | Retrofit                |
| `@Path`           | Parameters            | Inserts value into URL path                           | Retrofit                |
| `@SerializedName` | Fields                | Maps JSON keys to Kotlin variables                    | Gson / Moshi            |
| `@Test`           | Functions             | Marks unit test methods                               | JUnit                   |
| `@Before`         | Functions             | Runs setup before tests                               | JUnit                   |
| `@After`          | Functions             | Runs cleanup after tests                              | JUnit                   |
| `@Deprecated`     | Anything              | Marks code as outdated                                | Compiler warning system |
| `@Suppress`       | Anything              | Hides compiler warnings                               | Kotlin compiler         |
| `@Target`         | Annotation class      | Restricts where annotation can be used                | Compiler                |
| `@Retention`      | Annotation class      | Defines when annotation exists (source/class/runtime) | Compiler                |
| `@Serializable`   | Classes               | Enables Kotlin serialization                          | Kotlinx Serialization   |