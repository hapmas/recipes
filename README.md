**Show All Recipes**
----
  Returns json of all recipes.

* **URL**

  /recipes

* **Method:**

  `GET`
  
*  **URL Params**

   **Required:**
 
   `none`

* **Data Params**

  None

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `[
        { _id : vckdu87uingghacxj, title : "Fried Duck", ingredients: [], {...}, {...}, ... }
    ]`
 
* **Error Response:**

  * **Code:** 500 Internal server error 
    **Content:** `{ error }`

**Show a Recipe**
----
  Returns json data about a single recipe.

* **URL**

  /recipes/:id

* **Method:**

  `GET`
  
*  **URL Params**

   **Required:**
 
   `id=[String]`

* **Data Params**

  None

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{ _id : vckdu87uingghacxj, title : "Fried Duck", ingredients: [] }`
 
* **Error Response:**

  * **Code:** 500 Internal server error 
    **Content:** `{ error }`
    
** Post a recipe **
----
  Insert a single recipe to database.

* **URL**

  /recipes

* **Method:**

  `POST`
  
*  **URL Params**
    None

* **Data Params**

   **Required:** 
   `title=String`
   `ingredients=[{
       ingredient: String,
       qty: Number
       unit: String
   }]`

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{
    "recipe": {
        "_id": "5da7f4fc35624006979b5abb",
        "title": "gtn",
        "ingredients": [
            {
                "_id": "5da7f4fc35624006979b5abc",
                "qty": 50,
                "unit": "gram"
            }
        ],
        "__v": 0
    }
}`
 
* **Error Response:**

  * **Code:** 500 Internal server error 
    **Content:** `{ error }`


** Delete a recipe **
----
  Delete a single recipe from database.

* **URL**

  /recipes/:id

* **Method:**

  `DELETE`
  
*  **URL Params**

   **Required:**
 
   `id=String`

* **Data Params**

  None

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{
    "recipe": {
        "n": 1,
        "ok": 1,
        "deletedCount": 1
    }
}`
 
* **Error Response:**

  * **Code:** 500 Internal server error 
    **Content:** `{ error }`

** Update a recipe **
----
  Insert a single recipe to database.

* **URL**

  /recipes/:id

* **Method:**

  `PUT`
  
*  **URL Params**
    None

* **Data Params**

   **Required:** 
    NONE
**Optional**
 `title=String`
   `ingredients=[{
       ingredient: String,
       qty: Number
       unit: String
   }]`

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{
    "recipe": {
        "n": 1,
        "nModified": 1,
        "ok": 1
    }
}`
 
* **Error Response:**

  * **Code:** 500 Internal server error 
    **Content:** `{ error }`
  
