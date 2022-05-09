When organizing API endpoints, they should be based on the resources instead of on actions. The request methods will determine what action should be taken at a given URL endpoint. Your entire API's scheme should be consistent, clear and concise. Below are the principles and examples from the video, for your reference:

Principles
* Should be intuitive
* Organize by resource
* Use nouns in the path, not verbs
* The method used will determine the operation taken
GOOD:
https://example.com/posts
BAD:
https://example.com/get_posts
* Keep a consistent scheme
* Plural nouns for collections
* Use parameters to specify a specific item
GOOD:
https://example.com/entrees
https://example.com/entrees/5
BAD:
https://example.com/entree
https://example.com/entree_five
* Don’t make them too complex or lengthy
* No longer than collection/item/collection
GOOD:
https://example.com/entrees/5/reviews
BAD:
https://example.com/entrees/5/customers/4/reviews

----------------------------
![image](https://user-images.githubusercontent.com/91872964/167353732-024d2dc4-fa89-4394-b096-d453d448a8e3.png)
PUT :update entirely
