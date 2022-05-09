<h1>Token API</h1>
<b>HTTP Method:</b> &nbsp;&nbsp;&nbsp;[POST](#){ .md-button .md-button--primary} &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<b>Endpoint:</b>&nbsp;&nbsp;&nbsp; [https://groot.homingos.com/api/cuser/token](https://groot.homingos.com/api/cuser/token )

#### Use Case:
The Token API is used for user login, in which authentication is done with email and password. After logging in the user will be assigned with an authentication token which is necessary to
use further services.

#### Request Attributes:
| Attribute   | Description    |
| :---------- | :--------------|
| `email`     | Valid E-mail ID for user authentication|
| `password`  | Password for user authentication |

#### Response Attributes:
- `data`

| Attribute   | Description    |
| :---------- | :--------------|
| `token`     | Authentication token which is returned by this api after a sucessful login |
| `client_name`  | Full name of user fetched from user profile|
| `client_user_phone_number`| Phone Number fetched from user profile |
| `client_username`  | User Name|
| `client_user_name`  | User Name|
| `client_user_email`  | Email fetched from user profile |
| `client_credits`  |  It is the total count of referral credits done by user|

- `message`
- `status`
- `error`
<br>
<br>

#### Bash Scripts:
=== "CURL Request"

    ```json
    curl --header "Content-Type: application/json" \
  	--request POST \
  	--data '{"email":"7303736274","password":"7303736274"}' \
  	https://groot.homingos.com/api/cuser/token
    ```

=== "Response"

    ```json
    {
    "data":
    	{
    	"token":"08ceae08e844dc9692d4108677f5210842baf8a0",
    	"client_name":"917303736274",
    	"client_user_phone_number":"7303736274",
    	"client_username":"917303736274",
    	"client_user_name":"Amit",
    	"client_user_email":"xamit.94@gmail.com",
    	"client_credits":199763
        },
    "message":"Token generated successfully",
    "status":200,
    "error":false
    }
    ```










