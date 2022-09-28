# Meta-Tokens-API

The metatoken is a collection of a shopper's existing tokens, ranked according to how likely they lead to a successful transaction (based on our machine learning algorithm). 

### Authentication

Each request to the MetaToken must include an API KEY. Set this key to the x-api-key header value, for example:

```
curl https://checkout-test.adyen.com/v68/metaTokens \
-H 'x-api-key: ' \
-H 'content-type: application/JSON \
…
```
### Endpoints

<details open>
<summary>POST/metaTokens</summary>
<br>
Create a meta-token for Merchant requests with this endpoint
<br>

#### Request parameters <hr>

</details>


<details open>
<summary>POST/payments</summary>
<br>
Create a meta-token for Merchant requests with this endpoint
</details>
