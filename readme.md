<details>
 <summary>
 ###### Example configuration json file
 </summary>
    
    {
      "profiles_list": [
        {
          "id": -1,
          "service_id": "230",
          "name": "Contract",
          "description": "",
          "create_date": 1532419305326,
          "rank": 3,
          "enabled": true,
          "default_profile": false,
          "profile_filters": {
            "filters": [
              
            ]
          },
          "health_criteria": {
            "red": [
              {
                "type": "number_attribute",
                "attribute": "numeric_att",
                "eq": "0"
              }
            ],
            "green": [
              {
                "type": "number_attribute",
                "attribute": "numeric_att",
                "eq": "10"
              }
            ]
          },
          "grouping": {
            "type": "string_attribute",
            "attribute": "Account Type",
            "in_list": [
              "contract"
            ]
          }
        },
        {
          "id": -1,
          "service_id": "230",
          "name": "Client profile",
          "description": "",
          "create_date": 1532419447142,
          "rank": 2,
          "enabled": true,
          "default_profile": false,
          "profile_filters": {
            "filters": [
              
            ]
          },
          "health_criteria": {
            "red": [
              {
                "type": "number_metric",
                "lt": "1000",
                "source": "rollup",
                "metric": "sum__contract_value"
              }
            ],
            "green": [
              {
                "type": "number_metric",
                "eq": "3000",
                "source": "rollup",
                "metric": "sum__contract_value"
              }
            ]
          },
          "grouping": {
            "type": "string_attribute",
            "attribute": "Account Type",
            "in_list": [
              "client"
            ]
          }
        }}]
</details>
