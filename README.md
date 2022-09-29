# Tokenization 

## Retrying payments with Meta Tokens

With Meta Tokens, you can collect existing tokens from shoppers, ranked by their chances of completing a successful transaction. Using this method, you can try payment with the highest-ranking token, and if it fails, you can retry payment with the second-ranking token. In addition, this allows you to share tokens across multiple shops under the same company.

Tokenization is a process of replacing sensitive data with non-sensitive data.

A metatoken is a collection of a shopper's existing tokens, ranked according to how likely they lead to a successful transaction (based on our machine learning algorithm).

### Benefits of tokenization

- Increase revenues for businesses, especially those with subscription models.
- Let users share across multiple shops under the same company.
- Offer more secure payment. 
- Reuse of meta-token in retried payment. 

To secure your payment, you can tokenize payments with payment API, Application Programming Interface requests in which a token substitutes the PAN.

In the following API reference, you will find information on interacting with available endpoints. 

### Authentication

Each request to the meta-token must include an API KEY. Set this key to the x-api-key header value, for example:

```
curl https://checkout-test.adyen.com/v68/metaTokens \
-H 'x-api-key: ' \
-H 'content-type: application/JSON \
…
```
### Versioning

The version suffix has the following format: "vXX," where XX is the version number. 

For example:

`` https://checkout-test.adyen.com/v68/metaTokens `` 

### Endpoints

<details open>
<summary><b>POST</b>/metaTokens</summary>
<br>
Create a meta-token for Merchant requests with this endpoint.

#### Request parameters 
  
Request Item     | 	Data type| Required /Optional     |
| :---        |    :----:   |          ---: |
| shopperReference      | String       |Required  |
| merchantAccount  | String        | Required     |
  
##### Sample request
  ```
  curl https://checkout-test.adyen.com/v68/metaTokens \
-H 'x-api-key: ' \
-H 'content-type: application/json' \
-d '{
"shopperReference": "shopper-123",
"merchantAccount": "YOUR_MERCHANT_ACCOUNT"
}'
  ```

#### Response parameters 
   
Response Item     | 	Data type| Required /Optional     |
| :---        |    :----:   |          ---: |
| shopperReference      | String       |Required  |
| merchantAccount  | String        | Required     |
| metaTokenId   | String           | Required     | 

##### Sample request

  ```
  
  {
"merchantAccount": "YOUR_MERCHNAT_ACCOUNT",
"shopperReference": "yourShopperReference",
"metaTokenId": "9647-2876"
}

```


> Creating the token might take you a couple of minutes and sometimes even up to half an hour.


</details>

<details open>
  <summary><b>POST</b>/payments</summary>
<br>
Make a meta-token payment with a metaTokenId.
  
  #### Parameters <hr>
  
  ##### Path parameters
  
</details>


##### **List of questions that I asked when documenting the feature.**

1. What is the use case of "metatoken" and "meta-token" naming on the document provided?
2. How can I get `API KEY`? 
3. How is the ` shopperReference` obtained? 
4. How is the merchant identifier obtained?  
5. Can you point me to the information about the description of the parameters?
6. How can I test code snippets?  

