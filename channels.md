**Get All channels**
----
  Returns json data about all channels in the system.

* **URL**

  api/channels

* **Method:**

  `GET`
  
*  **URL Params**

  None

* **Data Params**

  None

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `[{ "name": "C1" }, { "name": "C2" }, { "name": "C3" }]`
 
* **Error Response:**

  * **Code:** 404 NOT FOUND <br />
    **Content:** `{ error : "channels are not found" }`

  OR

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "You are unauthorized to make this request." }`
    
**Get a channel**
----
  Returns json data about one channel based on id.

* **URL**

  api/channels/:id

* **Method:**

  `GET`
  
*  **URL Params**

   **Required:**
 
   `id=[integer]`

* **Data Params**

  None

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{ "_id": 1, "name": "g1" }`
 
* **Error Response:**

  * **Code:** 404 NOT FOUND <br />
    **Content:** `{ error : "channel doesn't exist" }`

  OR

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "You are unauthorized to make this request." }`
    
 
 
**Add a channel**
  ----
  
  Returns json data about the added channel.

* **URL**

  api/channels

* **Method:**

  `POST`
  
*  **URL Params**

  None
  
* **Data Params**

  **Content:** { "_id": 5, "name": "g5" }

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{ "_id": 5, "name": "g5" }`
 
* **Error Response:**

  * **Code:** 404 NOT FOUND <br />
    **Content:** `{ error : "channel couldn't be add, channel with the same id already exist" }`

  OR

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "You are unauthorized to make this request." }`
    
  
**Delete a channel**
----
  Returns json data about success.

* **URL**

  api/channels/:id

* **Method:**

  `DELETE`
  
*  **URL Params**

   **Required:**

 `id=[integer]`
 
* **Data Params**

  None
  
* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{"isSuccess":"true"}`
 
* **Error Response:**

  * **Code:** 404 NOT FOUND <br />
    **Content:** `{ error : "channel couldn't be found" }`

  OR

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "You are unauthorized to make this request." }`
