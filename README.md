# Newsman REST API Node Client
Newsman is a Smart Email Service Provider. We send newsletters on behalf of our customers.\
This is a very compact NodeJS wrapper and it uses Axios HTTP calls to our Newsman REST API.

See https://kb.newsman.com/api/ for details.\
You must set up a Newsman account and API key.

# Usage sample
```javascript
const Newsman = require('nzm-client')

const client = new Newsman.Client(some_user_id,some_api_key)

const getSegments = async () => {
    
        try {
          const segms = await client.callMethod('segment','all',{
            params: {
              list_id: some_list_id
            }
          })
          console.log(segms.data);
        } catch (error) {
          console.error(error)
        }
        
      }

getSegments()
```
