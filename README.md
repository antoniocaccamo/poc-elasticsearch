

	curl -X POST -H 'content-type:application/x-ndjson' \
	     --data-binary @exercises/data/accounts.json    \
		 'localhost:9200/bank/account/_bulk?pretty'



	GET bank/account/_search
	{
	"query": {
		"match": {
		"state": "CA"
		}
	}
	}

	GET bank/account/_search
	{
	"query": {
		"bool": {
		"must": [
			{
			"match": {
			"state": "CA"}
			},
			{
			"match": {
				"employer": "Techade"
			}
			}
		]
		}
	}
	}
