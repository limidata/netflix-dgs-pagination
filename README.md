# netflix-dgs-pagination
This is a sample project to showcase the use of netflix-dgs pagination module

https://medium.com/@umesh382.kushwaha/pagination-with-netflix-dgs-dcdc59feaf11

```graphql
 {
     vidoes(first:3){
         edges{
             node{
                 id
                 title
                 duration
             }
         }
         pageInfo{
            hasPreviousPage
            hasNextPage
            startCursor
            endCursor
        }
     }
 }
```

```json
{
    "data": {
        "vidoes": {
            "edges": [
                {
                    "node": {
                        "id": 1,
                        "title": "Video title-1",
                        "duration": 500
                    }
                },
                {
                    "node": {
                        "id": 2,
                        "title": "Video title-2",
                        "duration": 500
                    }
                },
                {
                    "node": {
                        "id": 3,
                        "title": "Video title-3",
                        "duration": 500
                    }
                }
            ],
            "pageInfo": {
                "hasPreviousPage": false,
                "hasNextPage": true,
                "startCursor": "c2ltcGxlLWN1cnNvcjA=",
                "endCursor": "c2ltcGxlLWN1cnNvcjI="
            }
        }
    }
}
```