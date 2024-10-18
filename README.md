# Postman Publish Action - fetch-collection

This repository contains GitHub Actions that help automate publishing Postman Collections to the Public API Network. 
You can use these actions to fetch a schema or Postman collection, transform an OpenAPI schema into a Postman collection, and update a Postman collection programmatically as part of your CI/CD workflows.


## Actions

### **Fetch Postman Collection**
   This action retrieves a Postman collection from the Postman API using the collection's UID. You can use this action when you need to pull the latest version of a collection as part of your build or deployment process.

   #### Inputs:
   - `postman_api_key`: Your Postman API key for authentication.
   - `collection_id`: The unique identifier of the Postman collection you want to retrieve.

   #### Example Usage:
   ```yaml
   - name: Fetch Postman Collection
     uses: stcalica/postman-publish-action@master
     with:
       postman_api_key: ${{ secrets.POSTMAN_API_KEY }}
       collection_id: 'your-collection-id'
   ```
