# JSON-Cheatsheet
### JSON (JavaScript Object Notation)
1. Data Representation Format
2. Commonly Used for APIs and Configs
3. Lightweight and easy to Read/Write
4. Integrates easily with most languages
5. Can be deeply nested and allows hierarchical data representation
6. Anything in JSON is a valid JavaScript

### Other alternatives to JSON
1. XML
2. YAML
3. BSON
### Why we chose JSON over other alternatives
1. Simplicity and Readability
2. Lightweight (when compared to XML)
3. Language Independence
4. JSON's Flexibility

### JSON Types
JSON supports:
1. Strings: "Hello world" "Name" "How"
2. Numbers: 10 5 -0.5 1e9
3. Booleans: true false
4. Null: null
5. Arrays: [1,2,3] ["Hello", "World"]
6. Objects: {"key": "value} {"age": 30}

### Example of JSON file
File name: user.json
```
{
  "name": "Aman Gupta",
   "age": 20,
   "enrolledUniversity": "DTU, Delhi", 
   "isProgrammer": true, 
   "languagesKnown": ["C++", "Python", "JavaScript"],
   "friends": [
      "name": "ABC",
      "age": 21, 
      "enrolledUniversity": "DTU, Delhi",
      "isProgrammer": true,
      "friends" : [...]
   ]
}
```

### Parsing of JSON
File name: companies.json
```
[
  {
    "name": "Google",
    "CEO": "Sundar Pichai",
    "numberOfEmployees": 20000,
    "rating": 4.5
  },
  {
    "name": "Microsoft",
    "CEO": "Satya Nadela",
    "numberOfEmployees": 15000,
    "rating": 4
  },
  {
    "name": "Big Corporation",
    "CEO": null,
    "numberOfEmployees": 2900,
    "rating": 2.5
  }
]
```
File name: index.html
```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Parsing JSON</title>
</head>

<body>
    <script type="text/javascript">
        let companies = [
            {
                "name": "Google",
                "CEO": "Sundar Pichai",
                "numberOfEmployees": 20000,
                "rating": 4.5
            },
            {
                "name": "Microsoft",
                "CEO": "Satya Nadela",
                "numberOfEmployees": 15000,
                "rating": 4
            },
            {
                "name": "Big Corporation",
                "CEO": null,
                "numberOfEmployees": 2900,
                "rating": 2.5
            }
        ]

        console.log("This is a javascript object");
        console.log(companies);

        console.log("Converting a javascript object to javascript string");
        let jsonConvertedString = JSON.stringify(companies);
        console.log(JSON.stringify(companies));

        console.log("Converting a javascript string to javascript object");
        console.log(JSON.parse(jsonConvertedString));

        console.log("Accessing the CEO of Google: ", companies[0].CEO);
    </script>
</body>

</html>
```

### Using Fetch API to Parse JSON
Modern JavaScript includes the Fetch API, which makes it easier to work with JSON data from APIs.
It allows you to fetch JSON data from URLs and automatically parse it into JavaScript objects.

```
// Example using Fetch API to fetch and parse JSON data
fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error fetching JSON:', error));
```
