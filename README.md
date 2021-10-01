# quickstarts

Backed service for integrated quickstarts.

## TO test
1. star the server `go run main.go `
2. insert some data 
```sh
curl --location --request POST 'http://localhost:8000/api/quickstarts/v1/quickstarts/' --header 'Content-Type: application/json' --data-raw '{
"Title": "New quickstart"
}'

```
3. query data: 
```sh
curl --location --request GET 'http://localhost:8000/api/quickstarts/v1/quickstarts/'
```

### IMPORTANT
`oc port-forward -n quickstarts svc/quickstarts-service 8000:8000`!