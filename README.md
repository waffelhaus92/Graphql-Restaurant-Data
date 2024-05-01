# Graphql-Restaurant-Data

This project provides a GraphQL API for managing restaurant data. It includes queries and mutations for retrieving, creating, updating, and deleting restaurant information.
Features

    Get a Single Restaurant: Retrieve details of a restaurant by providing its ID.
    Get All Restaurants: Get a list of all restaurants.
    Create a New Restaurant: Add a new restaurant to the list.
    Delete a Restaurant: Remove a restaurant from the list based on its ID.
    Update a Restaurant: Modify details of an existing restaurant.

Installation

    Clone the repository:

    bash

git clone <repository_url>

Install dependencies:

bash

npm install

Start the server:

bash

    node index.js

Usage

    Access the GraphQL interface at http://localhost:5500/graphql after starting the server.
    Use the provided queries and mutations to interact with the restaurant data.
    Refer to the GraphQL schema for available types and operations.

Example Queries and Mutations
Queries

    Get a single restaurant by ID:

    graphql

query {
  restaurant(id: 1) {
    id
    name
    description
    dishes {
      name
      price
    }
  }
}

Get a list of all restaurants:

graphql

    query {
      restaurants {
        id
        name
        description
        dishes {
          name
          price
        }
      }
    }

Mutations

    Create a new restaurant:

    graphql

mutation {
  setrestaurant(input: { name: "New Restaurant", description: "Description of the new restaurant" }) {
    id
    name
    description
  }
}

Delete a restaurant by ID:

graphql

mutation {
  deleterestaurant(id: 1) {
    ok
  }
}

Update a restaurant by ID:

graphql

    mutation {
      editrestaurant(id: 1, name: "Updated Restaurant Name") {
        id
        name
        description
      }
    }

Contributing

Contributions are welcome! Feel free to submit issues and pull requests.
License

This project is licensed under the MIT License.
