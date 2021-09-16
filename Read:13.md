# Related Resources and Integration Testing

## Working with Relationships in Spring Data REST

### One-to-One Relationship

Define two entity classes Library and Address having a one-to-one relationship, using the @OneToOne annotation. The association is owned by the Library end of the association:

@Entity
public class Library {

    @Id
    @GeneratedValue
    private long id;

    @Column
    private String name;

    @OneToOne
    @JoinColumn(name = "address_id")
    @RestResource(path = "libraryAddress", rel="address")
    private Address address;
    
    // standard constructor, getters, setters
}

@Entity
public class Address {

    @Id
    @GeneratedValue
    private long id;

    @Column(nullable = false)
    private String location;

    @OneToOne(mappedBy = "address")
    private Library library;

    // standard constructor, getters, setters
}

* The Repositories

In order to expose these entities as resources, create two repository interfaces for each of them, by extending the CrudRepository interface:

`public interface LibraryRepository extends CrudRepository<Library, Long> {}`

`public interface AddressRepository extends CrudRepository<Address, Long> {}`

### One-to-Many Relationship

A one-to-many relationship is defined using the @OneToMany and @ManyToOne annotations and can have the optional @RestResource annotation to customize the association resource.

To exemplify a one-to-many relationship, add a new Book entity that will represent the “many” end of a relationship with the Library entity:

@Entity
public class Book {

    @Id
    @GeneratedValue
    private long id;
    
    @Column(nullable=false)
    private String title;
    
    @ManyToOne
    @JoinColumn(name="library_id")
    private Library library;
    
    // standard constructor, getter, setter
}

public class Library {
 
    //...
 
    @OneToMany(mappedBy = "library")
    private List<Book> books;
 
    //...
 
}

* The Repository

We also need to create a BookRepository:

`public interface BookRepository extends CrudRepository<Book, Long> { }`

## Integration Testing in Spring

* Spring MVC Test Configuration

Enable Spring in Tests with JUnit 5: 

Enable Spring in Tests with JUnit JUnit 5 defines an extension interface through which classes can integrate with the JUnit test.

We can enable this extension by adding the @ExtendWith annotation to our test classes and specifying the extension class to load. To run the Spring test, we use SpringExtension.class.

We also need the @ContextConfiguration annotation to load the context configuration and bootstrap the context that our test will use.