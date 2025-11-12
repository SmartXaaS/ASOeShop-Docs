# Campaign Add

#### API Endpoint

**POST** `https://api.asoeshop.com/campaign/add?platform=android`

#### Authorization

To access the API, a valid API key is required for authentication. Ensure you have included the API key in your request header.

| Key    | Value   |
| ------ | ------- |
| apikey | ••••••• |

#### Params

When making a request, ensure the following parameters are passed:

| Parameter | Required | Description           |
| --------- | -------- | --------------------- |
| platform  | android  | android or ios or web |

#### Body (form-data)

When sending data in the body of the request, the fields listed below should be included as form-data:

| Field                | Value       | Description                          |
| -------------------- | ----------- | ------------------------------------ |
| type                 | cpe.keyword |                                      |
| app\_id              | 126973      | Application ID                       |
| country              | IN          | Target country                       |
| conversions          | 50          | Total installs                       |
| days                 | 5           | No. of days campaign will run for    |
| cap                  | 10          | Total no. of installs per day        |
| items\[1]\[keyword]  | 5592996     | Keyword1 ID                          |
| items\[1]\[quantity] | 5           | No. of installs per day for Keyword1 |
| items\[2]\[keyword]  | 5592997     | Keyword2 ID                          |
| items\[2]\[quantity] | 5           | No. of installs per day for Keyword2 |

#### Example Request

The following example demonstrates how to structure a curl request to the API endpoint:

```bash
curl --location 'https://api.asoeshop.com/campaign/add?platform=android' \
--form 'type="cpe.keyword"' \
--form 'app_id="126973"' \
--form 'country="IN"' \
--form 'conversions="50"' \
--form 'days="5"' \
--form 'cap="10"' \
--form 'items[1][keyword]="5592996"' \
--form 'items[1][quantity]="5"' \
--form 'items[2][keyword]="5592997"' \
--form 'items[2][quantity]="5"'
```

#### Notes

* Ensure that your API key is active and has the necessary permissions.
* Double-check the provided URLs for legality and activeness.
* Monitor your daily cap to avoid exceeding limitations.

{% openapi-operation spec="asoeshop-advertiser-api" path="/campaign/add" method="post" %}
[OpenAPI asoeshop-advertiser-api](https://4401d86825a13bf607936cc3a9f3897a.r2.cloudflarestorage.com/gitbook-x-prod-openapi/raw/1934dea5e662ff4da6512108c82c8d67a6c7b4337210ae47fe9a1647ce5bcf9f.json?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=dce48141f43c0191a2ad043a6888781c%2F20251112%2Fauto%2Fs3%2Faws4_request&X-Amz-Date=20251112T081935Z&X-Amz-Expires=172800&X-Amz-Signature=2d52dea84fb99ce3bf9f21410d96d95f5ca5ff583aabcd21f474886fcac2df4e&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)
{% endopenapi-operation %}
