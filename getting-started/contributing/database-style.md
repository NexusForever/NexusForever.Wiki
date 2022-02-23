# Database Style

To keep the database clean and uniform this document should be referenced if you are planning to submit a pull request or work on the repository.

### Database Segregation

When creating new database tables keep in mind where specific data should go, below is a quick overview of each database and it's role.

#### Authentication Database

The authentication database should only contain account specific data, this database can be shared by multiple servers.

#### Character Database

The character database should only contain character/server specific data, this database should only be used by a single server.

#### World Database

The world database should only contain static data, this database can be shared by multiple servers.

### Code Style

| Entity  | Style       |
| ------- | ----------- |
| Tables  | snake\_case |
| Columns | lowerCamel  |



### Stored Procedures and Functions

Business logic in the database should be avoided at all costs.
