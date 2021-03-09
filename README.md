Query examples

query {
  users {
    _id
    firstName
    active
  }
}

query {
  user(id:"6046b7e811c22710581f526e"){
    firstName
    lastName
    fullName
  }
}

query {
  posts {
    title
    author {
      fullName
    }
  }
}

Mutation examples

mutation {
  createUser(data: {
    firstName: "Frederico",
    lastName: "Parreira",
    email: "fred@teste.com",
    active: true
  }) {
    _id
    email
  }
}

mutation {
  deleteUser(id:"6046b77a11c22710581f526d")
}

mutation {
  updateUser(id: "6046b7e811c22710581f526e", data: {
    firstName: "Frederico Roberto",
    lastName: "Parreira",
    email: "fred@teste.com",
    active: true
  }) {
    firstName
    lastName
  }
}

mutation {
  createPost(data: {
    title: "Titulo"
    content: "Conteúdo"
    author: "6046b7e811c22710581f526e"
  }) {
    title
  }
}

mutation {
  createUser(data: {
    firstName: "Fred"
    lastName: "Parreira"
    email: "fred2@teste.com"
    active: true
  }) {
    _id
  }
}

Socket example

subscription {
  userAdded {
    fullName
  }
}