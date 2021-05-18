# Alfred-Notion
Add Notes to Notion by Alfred


This is a Alfred wolkflow by [notion-api](https://developers.notion.com/). 

It's only beta version for some idea to you.

# How to use
1. Download this file [Add-Notes-To-Notion.alfredworkflow](https://github.com/polandeme/alfred-notion/blob/main/Add-Notes-To-Notion.alfredworkflow)and import to your Alfred
2. Replace the your_app_token and your_page_block


# How to develop
It's a simple shell script, you can modify use [notion-api](https://developers.notion.com/) make more exciting things.

```shell
curl -X PATCH https://api.notion.com/v1/blocks/${your_page_block}/children \
  -H 'Authorization: Bearer '${your_app_token}'' \
  -H "Content-Type: application/json" \
  -H "Notion-Version: 2021-05-13" \
  --data '{
    "children": [
    {
      "object": "block",
      "type": "paragraph",
      "paragraph": {
        "text": [
            { 
                "type": "text", 
                "text": { "content": "{query}" } }]
      }
    }
  ]
}'
```



