# eduencers-2023

# Invoke lambda
export INVOKE_URL="https://glzxzla4o6.execute-api.us-east-2.amazonaws.com"

## Create an item
curl -X "PUT" -H "Content-Type: application/json" -d "{
    \"id\": \"abcdef234\",
    \"price\": 12345,
    \"name\": \"myitem\"
}" $INVOKE_URL/items

## Get items
curl -s $INVOKE_URL/items | jq .

## Get an item by id
curl -s $INVOKE_URL/items/abcdef234 | jq .

## Delete an item by id
curl -X "DELETE" $INVOKE_URL/items/abcdef234
