Here are some mutations and queries to test in this project's GraphQL playground:

```graphql
mutation createCategory {
  createCategory(input: {name: "category_name", description: "category_description"}) {
    id
    name
    description
  }
}

mutation createCourse {
  createCourse(input: {name: "course_name", description: "course_description", categoryId: "category_id"}) {
    id
    name
    description
  }
}

query queryCategories {
  categories {
    id
    name
    description
  }
}

query queryCategoriesWithCourses {
  categories {
    id
    name
    description
    courses {
      id
      name
      description
    }
  }
}

query queryCourses {
  courses {
    id
    name
    description
  }
}

query queryCoursesWithCategory {
  courses {
    id
    name
    description
    category {
      id
      name
      description
    }
  }
}
```