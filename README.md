# Java-EE-Design-Patterns

##Todo
- Make it a very short course
- Look at Santosh's book further
- Decide if creating the course makes sense. It does now!!

# Front Controller
- Look at all incoming requests.
- Mapping from String to the View.
- DataBinding
- Spring MVC - DispatcherServlet
- Security - Spring MVC
- Logging

#Application Controller
- Invoke business components.
- Identify and redirect to the next view.

#Context Object
- Typically Presentation Tier is tightly coupled to the Servlet API - extensively using HttpServletRequest and HttpServletResponse . Page controllers cannot be reused outside Web Application context.
- Increase the reusability of page controllers.
- Use a context object to encapsulate and share form data without any protocol dependency.
- Spring MVC uses ModelMap as the Context Object. This class serves as generic model holder for both Servlet and Portlet MVC, but is not tied to either of those.
- Easier to Test

#Composite View
- Tiles and SiteMesh
- Web pages have header footer navigation and content. 
- View in mobile might be different from a desktop
- The solution to this is to use composite views that are composed of multiple atomic subviews. 
- Layout of the page may be managed independently of the content.
- Web designers can design the layout of a site, using static content in each of the template regions. 

#View Helper
- Tag Libraries used for Date Formatting
- Spring Tag Libraries for Form Binding

#Intercepting Filter
- AOP
- Logging
- authentication filters , logging & auditing , Image conversion , data compression , encryption



#Service Locator  (With Spring - these kind of things have become obselete)
- Is a Singleton that is used to reuse code performing the JNDI lookup . 
- Abstracts complexity 
- Provides uniform service access to Clients 
- Improves performance 
- Sometimes referred to as the EJBHomeFactory ( EJB design patterns ) .

#Session Facade
- The session bean will probably interact with two or more entity beans
- Transaction
- Easier to use for the Client
- Better Performance

#Business Delegate
- Presentation Tier need access to Distributed Business Services.
- Code needed to access them might need understand the fact that the service is distributed, there-by, will be more complex. Example, EJB Remote Methods from time before.
- Plain Java classes that hide EJB API complexity by encapsulating code required to discover, delegate to and recover from invocations on the session and message façade EJB layers.
- Use on large projects where the web team is separate from the EJB team .

# Service Activator
- Some long-running use cases take long time. Instead of blocking the users, we can run these asynchronously
- JMS Can be used

#Data Transfer Object / Value Object
- Typically created by a Session Facade
- Reflects the structure of the data needed by the view
- Anaemic, without Business Logic
- For me its an anti pattern
- Client makes a single remote method invocation to the enterprise bean to request the Transfer Object / Value Obects instead of numerous remote method calls to get individual attribute values.
- A value object is an object that encapsulates all the data required by a client . 
- The client can then call get methods on the value object to get all the data needed by the client .

#Data Access Object (@Repository)
- Use a Data Access Object ( DAO ) to abstract all access to a data source. 
- The DAO will help to hide details of access to the data source from the client. 
- Promotes easier migration from one data source to another



#Value List Handler
- Used to retrieve large amounts of data
- Provides alternatives to EJB Finders for large queries.
- Cache query results on server side.
- Value List Handler sequence


#Domain Model

#Model View Controller

#Page Controller


