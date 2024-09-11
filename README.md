# springboot-security
Spring Security is really just a bunch of servlet filters that help you add authentication and authorization to your web application.
### Authentication:
Typically done with a username and password check.
### Authorization:
Determines what a user can access and grants access based on their level of access.

### Some Pointer
<ul>
  <li>Every Path is defined(in Controller) with @PreAuthorize annotation to define which Role can access it.</li>
  <li>Signin Route/Path is defined where it accepts username and password, this is validated against database and if correct issues a JWT token (For Stateless requests).</li>
  <li>When requst comes to any other paths with bearer JWT token, it is validated if its is valid and not expired, then only request goes to desired path controller.</li>
  <li>Password stored in the database are hashed for security reasons.</li>
</ul>
