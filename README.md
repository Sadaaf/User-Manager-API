## User Manager API

## Installation Instruction
You need python and pip installed on your system. 
Run the following command in your terminal:
pip install -r requirements.txt

Go to the project directory in your teminal and run the following command:
python manage.py runserver

This will start the development server at http://127.0.0.1:8000/

## API Endpoints
- GET
![GET REQUEST USERS](https://user-images.githubusercontent.com/35129264/173423648-cc18c4e4-634b-4b3e-97d7-786261b71334.png)
You can get all the existing users in the database using http://127.0.0.1:8000/users/

________________________________________________________________

![GET REQUEST USERS_CHILD](https://user-images.githubusercontent.com/35129264/173423995-6e92b0cd-dfb2-4951-96a2-71f5a3416813.png)
You can get all the existing child under all parents using http://127.0.0.1:8000/users-child/

- POST
![POST REQUEST USERS](https://user-images.githubusercontent.com/35129264/173424423-bd314093-a6cb-44dc-aacb-d8793abebfb6.png)
You can add new user using http://127.0.0.1:8000/users/ and sending a POST request with a JSON data in the body in following format:
{
    "id": 1,
    "first_name": "Nobita",
    "last_name": "Monsur",
    "street_address": "Kanchan",
    "city_address": "Gazirampur",
    "state_address": "Sholakia",
    "zip_code": "8457"
}
________________________________________________________________

![POST REQUEST USERS_CHILD](https://user-images.githubusercontent.com/35129264/173424896-dcf45df2-ed2d-4059-bd8a-8ab3565b59af.png)
You can add new user_child using http://127.0.0.1:8000/users-child/ and sending a POST request with a JSON data in the body in following format:
{
    "parent": 1,
    "child_first_name": "Shonir",
    "child_last_name": "Akhra"
}

*You must provide an existing id from the users Table in side the parent parameter to create a new user_child

- PUT
![PUT REQUEST USER](https://user-images.githubusercontent.com/35129264/173425413-48a8fdcc-dd6b-4566-8f04-759f455124f5.png)
You can update existing user information using http://127.0.0.1:8000/users/{id} [specify the id number of the user you want to update in {id}], and send a PUT request with a JSON data in the body in following format:
{
            "first_name": "Narshingam",
            "last_name": "Kontaki",
            "street_address": "Kanthakier",
            "city_address": "Kilmany",
            "state_address": "korotia",
            "zip_code": "4875"
}
________________________________________________________________

![PUT REQUEST USER_CHILD](https://user-images.githubusercontent.com/35129264/173427067-c81d8fa8-071f-4360-94db-7b7019830ad8.png)
You can update existing user_child information using http://127.0.0.1:8000/users-child/{id} [specify the id number of the user_child you want to update in {id}], and send a PUT request with a JSON data in the body in following format:
{
    "parent": 1,
    "child_first_name": "Intesar",
    "child_last_name": "Ali"
}

- DELETE
![image](https://user-images.githubusercontent.com/35129264/173427883-78b28710-cdb7-48d5-a367-31afe1c5287b.png)
You can delete any user information from the database using http://127.0.0.1:8000/users/{id} [specify the id number of the user you want to Delete in {id}], and send a DELETE Request

________________________________________________________________

![DELETE REQUEST USER](https://user-images.githubusercontent.com/35129264/173427384-9877e8b9-dd7f-4768-97ab-2c84cb921621.png)
You can delete any user_child information from the database using http://127.0.0.1:8000/users-child/{id} [specify the id number of the user_child you want to Delete in {id}], and send a DELETE Request