# MVC Web app

<img align="right" style="width:200px; height:auto;" src="/public/images/favicon.ico">

A college project in Node JS using Express and MongoDB.<br>
Description: a basic "travel agency" website with permission management and two user types.<br>

<table align="center">
   <thead>
   <tr>
      <td colspan="2" align="center">Collaborators</td>
   </tr>
   </thead>
   <tbody>
   <tr>
    <tr>

      </tr>
      <td>
      </td>
      <td>
      </td>
   </tr>
   </tbody>
</table>
<details>

  <summary><h3>Content</h3></summary>

- [Installation](#installation)
- [Usage](#usage)

</details>
<hr>

# Installation

1. Open a MongoDB project if you don't have one.
2. Create a `.env` file and paste your MongoDB connection string in it, the file should look like this:

```
DB=mongodb+srv://<USERNAME>:<PASSWORD>@<CLUSTER>.mongodb.net/?retryWrites=true&w=majority
```

3. Create users in your MongoDB database according to the schema in `database/account.js`.<br>For example:


```
username: "admin"
password: "admin1"
permissions: "admin"
```

```
username: "bob"
password: "bob1"
permissions: "user"
IDnumber: "123456789"
cardNumber: "6789678967896789"
fullName: "Bob Bobby"
```


4. Change "autoOpen" in `app.js` to your preferred launch method.
5. Run `npm i`.
6. Start `app.js`.

# Usage

1. Login to your preferred user.
2. Admin users can:
   - adjust the seat amount of each plane. (don't ask, college requirement)
   - edit, delete and creates flights.
3. Regular users can:
   - view existing flights, sort and filter flights.
   - book tickets for available flights.
   - have the app insert their payment details from the database (if they exist).
   - or input a card manually to "pay" for the flight.

> [!NOTE]
> The app doesn't check for card validity and doesn't try to make a transaction.
