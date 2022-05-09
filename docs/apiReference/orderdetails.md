<h1>Order Details API</h1>
<b>HTTP Method:</b> &nbsp;&nbsp;&nbsp;[GET](#){ .md-button .md-button--primary} &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<b>Endpoint:</b>&nbsp;&nbsp;&nbsp; [https://groot.homingos.com/api/orders/orderdetails](https://groot.homingos.com/api/orders/orderdetails)

#### Use Case:
This API is used to get details of all the orders placed by our ID or through our referrals.

#### Response Attributes:
- `data`

| Attribute   | Description    |
| :---------- | :--------------|
| `id`     | Product ID|
| `video_url` | URL of Video which was uploaded by customer |
| `photo_url`| URL of Photo which was uploaded by customer|
| `ref_id`  | Referrer ID|
| `name`  | Name of user|
| `phone_number`  |User's Phone Number|
| `status`  | Order Status |
| `created_on`  | Date and Time of Order|
| `augmented`  |Boolean value to check image is augmented (True/False)|
| `augmented_image`  | Augumented URL of Image|

- `message`
- `status`
- `error`
<br>
<br>

#### Bash Scripts:
=== "CURL Request"

    ```json
    curl --header "Content-Type: application/json" \
    --request GET \
    https://groot.homingos.com/api/orders/orderdetails
    ```

=== "Response"

    ```json
    {
    "data":
    	{
    	"id":"b887137f-c989-4217-8595-8aaf50f720de",
    	"video_url":"https://homingos-magik.s3.ap-south-1.amazonaws.com/vibo/prod/base/51efe149-bf2b-41d3-85a8-bf02c019cdfa.mp4",
    	"photo_url":"https://homingos-magik.s3.ap-south-1.amazonaws.com/vibo/prod/base/ede4b6bc-a955-4ea7-9a68-90bf529c510e.jpg",
    	"ref_id":"V023417",
    	"name":"Yogesh Sangtani",
    	"phone_number":"9649430924",
    	"status":"PENDING",
    	"created_on": "2022-01-28T10:03:52.443282Z",
    	"augmented": false
    	"augmented_image":"https://homingos-magik.s3.ap-south-1.amazonaws.com/vibo/prod/print/b887137f-c989-4217-8595-8aaf50f720de.jpeg"
        },
    "message":"All Partner Videocards",
    "status":200,
    "error":false
    }
    ```










