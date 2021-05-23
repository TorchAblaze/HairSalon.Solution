# Eau Claire's Hair Salon

#### _Web application for managing Claire's Hair Salon, 5/21/2021_

#### By _**Tiffany Greathead**_

## Description

A website application for a fictional client named Eau Claire who owns Eau Claire's Salon. Claire can add new stylists to her employee roster and view all her employees in a list. She can click on an employee name to see additional details and contact information about that employee. New clients can be added for each stylist and will appear under that stylist's details page. If Claire clicks on a client name, she can see that client's contact information and any upcoming appointments that client may have.

## Setup and Use

### Prerequisites

- [.NET 5 SDK](https://dotnet.microsoft.com/download/dotnet/5.0)
- A text editor like [VS Code](https://code.visualstudio.com/)
- A command line interface like Terminal or GitBash to run and interact with the console app.
- [MySQL Community Server](https://dev.mysql.com/downloads/file/?id=484914)

### Installation

1. Clone the repository: `$ git clone https://github.com/TorchAblaze/HairSalon.Solution.git`
2. Navigate to the `HairSalon` directory on your computer
3. Open with your preferred text editor to view the code base
4. To setup a SQL database using MySQL:
   - Create an `appsettings.json` file in the `HairSalon` directory
   - Copy the text box below and paste into the `appsettings.json` file, replacing `<password>` with your MySQL password:
   ```
     {
        "ConnectionStrings": {
           "DefaultConnection": "Server=localhost;Port=3306;database=tiffany_greathead;uid=root;pwd=<password>;"
         }
     }
   ```
   - Open your terminal and run the command: `mysql -uroot -p<mysql_password>` (replace `<mysql_password>` with your MySQL password) and select the enter key to launch MySQL servers
   - Type the following commands to setup the database:
     - `CREATE DATABASE tiffany_greathead;` to make a new database
     - `USE tiffany_greathead;` to connect to the new database
     - `CREATE TABLE stylists (StylistId INT, Name VARCHAR (255), StartDate VARCHAR (255), ShiftHours VARCHAR (255), ShiftDays VARCHAR (255), PhoneNumber VARCHAR(15));` to create a `stylists` table
     - `CREATE TABLE clients (ClientId INT, Name VARCHAR (255), AppointmentDateTime VARCHAR(255), PhoneNumber VARCHAR (15), StylistId INT);` to create another new `clients` table
5. To run the console app:
   - Navigate to `HairSalon.Solution/HairSalon` in your command line
   - Run the command `dotnet restore` to restore the dependencies that are listed in `HairSalon.csproj`
   - Run the command `dotnet add package Microsoft.EntityFrameworkCore -v 5.0.0`
   - Run the command `dotnet add package Pomelo.EntityFrameworkCore.MySql -v 5.0.0-alpha.2`
   - Run the command `dotnet add package Microsoft.EntityFrameworkCore.Proxies -v 5.0.0`
   - Run the command `dotnet build` to build the project and its dependencies into a set of binaries
   - Finally, run the command `dotnet run` to run the project!
   - Note: `dotnet run` also restores and builds the project, so you can use this single command to start the console app
6. Visit the application via web browser at: `localhost:5000/`

## Known Bugs

_No known bugs_

## Support and contact details

_Please reach out through my GitHub account._

## Technologies Used

- C#
- .NET 5 SDK
- ASP.NET
- Entity Framework Core
- Bootstrap

### License

MIT License.

Copyright (c) 2021 **_Tiffany Greathead_**
