<h1>Partner API</h1>
<b>HTTP Method:</b> &nbsp;&nbsp;&nbsp;[POST](#){ .md-button .md-button--primary} &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<b>Endpoint:</b>&nbsp;&nbsp;&nbsp; [https://groot.homingos.com/api/orders/partnervc](https://groot.homingos.com/api/orders/partnervc)

#### Use Case:
This API is used to upload photo and video for flam card and to successfully place an order

#### Request Attributes:
| Attribute   | Description    |
| :---------- | :--------------|
| `product_id`     | Product ID which user ordered|
| `video_url`  | URL of Video which was uploaded by customer|
| `photo_url`  | URL of Photo which was uploaded by customer|
| `name`  | Name of Customer|
| `phone_number`  | Phone Number of Customer|
| `country_code`  | Country Code of User's Phone Number|
| `sender_name`  | Name of the Person who selled/reffered the above customer|
| `sender_phone_number`  | Phone Number|
| `sender_country_code`  | Country Code|
| `upload_media_later`  | A boolean value to store whether a customer chose to upload media later(True/False)|
| `utm_medium`  | Order Mode(website/app/referral)|
| `utm_campaign`  | Marketing Campaign parameter to know that the order is achieved organically or through paid adds/campaigns|
| `utm_source`  | Source of FlamCard order(videoshop/instant etc)|

#### Response Attributes:
- `data`

| Attribute   | Description    |
| :---------- | :--------------|
| `order_id`     | The unique ID of the product ordered by user|
| `augmented_image`  |Compressed image for frontend preview|
| `anv_id`| Augumented Image ID|
| `is_fulfilled`  | Boolean Value to store whether the order process is completed(True/False)|

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
  	--data '{"product_id":"c6db39a2-84bd-42be-80e8-fb62ff39a438",
  	"video_url":"https://homingos-magik.s3.ap-south-1.amazonaws.com/vibo/prod/base/5cea2d6f-b331-458b-ac1b-e63a03ee9bda.mp4",
  	"photo_url":"https://homingos-magik.s3.ap-south-1.amazonaws.com/vibo/prod/base/506fa937-7369-459c-943d-0776843b6e6f.jpg",
	"name":"YogeshSangtani",
	"phone_number":"9649430924",
	"country_code":"+91",
	"sender_name":"917303736274",
	"sender_phone_number":"7303736274",
	"sender_country_code":"+91",
	"upload_media_later":false,
	"utm_medium":"website",
	"utm_campaign":"organic",
	"utm_source":"videoshop"}' \
  	https://groot.homingos.com/api/orders/partnervc
    ```

=== "Response"

    ```json
    {
    "data":
    	{
    	"order_id":"a4b835b8-3532-4662-8e55-275bfb2dc0f7",
    	"augmented_image":"https://homingos-magik.s3.ap-south-1.amazonaws.com/vibo/prod/print/ee08ea85-82bf-47bb-9b03-1a868d72a2fd.jpeg",
    	"anv_id":"V023412",
    	"is_fulfilled":false
    	},
    "message":"Videocard Added",
    "status":200,
    "error":false
    }
    ```










