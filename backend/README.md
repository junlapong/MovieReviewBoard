# MovieReviewBoard API

## Pre-requisite

* You need to install JDK 8 or above. You can get it [here](https://www.oracle.com/technetwork/java/javase/downloads/jdk11-downloads-5066655.html)
* You can use any IDE for run the project but I will recommend you use [IntelliJ IDEA](https://www.jetbrains.com/idea/download/)

## App Setup

* Clone this repository by executing `git clone https://github.com/vladimirfomene/MovieReviewBoard.git` in your console.
* Enter the project directory with `cd MovieReviewBoard/backend`.

## Running the app.

* Run the app by executing `./gradlew bootRun` in the project directory.


## Testing the application

* Visit http://localhost:8888/graphql to access the GraphQL server.

## Query

* In order to issue queries to the API visit http://localhost:8888/graphiql to send your queries.
<!-- * Or use GraphQL Playground visit http://localhost:8888/gui -->

### Example Query

see schema in [src/main/resources/graphql](src/main/resources/graphql)

#### findAllMovies

```graphql
query {
  findAllMovies {
    id
    title
    rating
    director {
      firstName
      lastName
    }
  }
}
```

#### countMovies

```graphql
query {
	countMovies
}
```

#### findAllDirectors

```graphql
query {
  findAllDirectors {
    id
    firstName
    lastName
  }
}

```

### findMoviesByDirector
```graphql
query {
  findMoviesByDirector (directorId: 1) {
    id
    title
  }
}
```