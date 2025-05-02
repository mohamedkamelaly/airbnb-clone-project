# airbnb-clone-project
#Team Roles:
Back-end Developer: implement the core of an app—its algorithms and business logic. Experienced back-end developers not only write code but also do the tasks of an architect—for example, devise an app architecture or design and implement the necessary integrations.

Quality assurance (QA) engineer : verify whether an application meets the requirements—both functional and non-functional. Functional requirements define what an application should do, while non-functional requirements specify how it should do that. To verify both, QA specialists run various checks, followed by analyzing the test results and reporting on the application quality.

DevOps engineer: serve as a link between the two teams, unifying and automating the software delivery process and helping strike a balance between introducing changes quickly and keeping an application stable. Working together with software developers, system administrators, and operational staff, DevOps engineers oversee and facilitate code releases on a CI/CD basis.

#Technology Stack:
Django: A high-level Python web framework used to build robust, scalable web applications and RESTful APIs.

PostgreSQL: A powerful, open-source relational database system used to store and manage application data.

GraphQL: A query language for APIs that allows clients to request exactly the data they need, improving performance and flexibility.

Django REST Framework (DRF): A toolkit built on Django to create Web APIs quickly and with minimal code.

Docker (optional if used): A containerization tool used to package the application and its dependencies for consistent deployment across environments.

Git & GitHub: Used for version control and collaborative development.


#Database Design:
1. Users
Represents individuals using the platform, either as property owners or renters.

Key Fields:

id: Unique identifier for the user

username: Chosen username

email: User's email address

password: Encrypted password

is_host: Boolean indicating if the user can list properties

Relationships:

A user can list multiple properties.

A user can make multiple bookings.

A user can leave multiple reviews.

2. Properties
Represents a property available for booking.

Key Fields:

id: Unique identifier for the property

title: Name or title of the property

description: Detailed description

location: Address or geographic info

price_per_night: Cost per night of stay

Relationships:

Each property is owned by a single user (host).

A property can have multiple bookings.

A property can have multiple reviews.

3. Bookings
Represents a reservation made by a user.

Key Fields:

id: Unique identifier for the booking

user_id: ID of the user who made the booking

property_id: ID of the property being booked

start_date: Check-in date

end_date: Check-out date

Relationships:

A booking is made by one user for one property.

A property can have many bookings, but a booking belongs to only one property.

4. Reviews
Represents feedback left by users on properties.

Key Fields:

id: Unique identifier for the review

user_id: Reviewer’s user ID

property_id: Reviewed property ID

rating: Numeric score (e.g., 1–5)

comment: Text of the review

Relationships:

A review belongs to one user and one property.

A property can have many reviews.

5. Payments
Represents transactions made for bookings.

Key Fields:

id: Unique identifier for the payment

booking_id: Associated booking

amount: Total amount paid

payment_method: Method of payment (e.g., credit card)

status: Payment status (e.g., successful, pending)

Relationships:

A payment is linked to a single booking.

Each booking has one corresponding payment.




