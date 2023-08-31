# Prisma Backend Boilerplate
<!-- Description -->
This `Prisma Backend Boilerplate` is a starter project for building a backend with Prisma and Node.js.


## Installation Steps
### Follow these steps to clone and set up starter project:

1. `Clone the project:` Open your terminal or command prompt and run the following command to clone the project repository:

```bash
git clone 
```

2. `Navigate into the project directory:` Use the cd command to navigate into the project directory:

```bash
cd Prisma-Backend-Boilerplate
```

3. `Install project dependencies:` Next, install the project dependencies by running the following command:

```bash
  npm i install
```

4. Configure Prisma and the database connection:

- Add Prisma as a development dependency by running the following command:
```bash
  npm i prisma --save-dev
```

- Set up your Prisma project by creating the Prisma schema file using the following command:
```bash
npx prisma init
```

- Open the prisma/schema.prisma file and configure your database connection details.

```bash
datasource db {
  provider = "postgresql"
  url      = env("DATABASE_URL")
}
```

- Create a .env file in the project root directory and set the DATABASE_URL environment variable. Replace the placeholders with your database connection details:
```bash
DATABASE_URL="postgresql://USER:PASSWORD@HOST:PORT/DATABASE?schema=SCHEMA"
```

5. Creating the database schema
6. Migrate the database schema: Use the following command to create and apply the initial database schema:

```bash
npx prisma migrate dev --name init
```
This command creates a new migration file based on your schema changes and applies it to your database.

6. `Install Prisma Client:` Install the Prisma Client library by running the following command:
```bash
yarn add @prisma/client
```

#### `Dynamic Modules template generator:` You can create Modules Folder with controller, service, validations, constants, routes by this command dynamically:

```bash
  node generateFile.ts <moduleFolderName> <moduleName>
  // Like node generateFile.ts User user
```

This command installs the Prisma Client, which provides an interface to interact with your database.

Happy coding!