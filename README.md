# web_apis

Please find all api end points, header and body formates inside the postman collection
#### postman collection    `https://www.getpostman.com/collections/cd02d0038885da9eec2b`

## Profile page :

### get: profile
Get user profile data along with leaderboard and family members
- response object :  status 200
```
{
    "user": {
        "_id": "LLFo4l95YVgYwsWbAN3QTGw6Bui1",
        "name": "updated name",
        "phone": "8355038184",
        "age": "25",
        "gender": "पुरुष",
        "region": "Mumbai"
    },
    "userDashboard": {
        "uid": "LLFo4l95YVgYwsWbAN3QTGw6Bui1",
        "name": "updated name",
        "phone": "8355038184",
        "points": 8700,
        "played_quiz": 16,
        "video_watched": 16,
        "level": 2,
        "quiz_remaining": 147,
        "video_remaining": 113,
        "user_rank": 39600
    },
    "family_members": [
        {
            "age": "6",
            "rln": "बेटी",
            "aAt": {
                "_seconds": 1579433822,
                "_nanoseconds": 667000000
            },
            "name": "Abc",
            "uid": "LLFo4l95YVgYwsWbAN3QTGw6Bui1",
            "_id": "of4c0qsPaKnHdbwsGbuD"
        },
        {
            "uid": "LLFo4l95YVgYwsWbAN3QTGw6Bui1",
            "age": "35",
            "aAt": {
                "_seconds": 1579026600,
                "_nanoseconds": 0
            },
            "rln": "आप",
            "name": "8355038184",
            "_id": "paWHrh5F1E9PCdsxro1Z"
        },
        {
            "uid": "LLFo4l95YVgYwsWbAN3QTGw6Bui1",
            "age": "15",
            "aAt": {
                "_seconds": 1579243623,
                "_nanoseconds": 329000000
            },
            "rln": "Son",
            "name": "Rahul",
            "_id": "smo8bWEj2zIwAkUSpCd7"
        },
        {
            "age": "12",
            "aAt": {
                "_seconds": 1579069955,
                "_nanoseconds": 800000000
            },
            "rln": "Son",
            "name": "tahir",
            "uid": "LLFo4l95YVgYwsWbAN3QTGw6Bui1",
            "_id": "wmntQnerff6ZHTLQsd9N"
        },
        {
            "uid": "LLFo4l95YVgYwsWbAN3QTGw6Bui1",
            "age": "2",
            "rln": "बेटा",
            "aAt": {
                "_seconds": 1579452520,
                "_nanoseconds": 230000000
            },
            "name": "Abc",
            "_id": "zNeu9JxNsnqDC81BHyQJ"
        }
    ],
    "leaderboard": [
        {
            "uid": "6DTeA4GofPSU4O2PWSMrY6fc4t93",
            "name": "Imran",
            "phone": "9320949001",
            "points": 113950
        },
        {
            "uid": "mCxebbtS2HSj1AMKVORkkg4ECHI3",
            "name": "Shyamlal",
            "phone": "8286879558",
            "points": 90100
        },
        {
            "uid": "edRQdnpzamcNNDAWVzuD5ocI0Bs1",
            "name": "Reshma shaikh s",
            "phone": "8369583673",
            "points": 87090
        },
        {
            "uid": "pFR3WMP9AafOwNDLo3gKwIYbqSv1",
            "name": "arch",
            "phone": "8805222422",
            "points": 76320
        },
        {
            "uid": "FfviQ0AmF5YNnrbsZxPhTyEyUFN2",
            "name": "neha",
            "phone": "9625404669",
            "points": 72500
        }
    ]
}
```

### post: add_family_members
Add new family member to users family
- response object: status 200
```
{
    "uid": "LLFo4l95YVgYwsWbAN3QTGw6Bui1",
    "name": "Aamir",
    "age": "24",
    "rln": "brother",
    "aAt": "2020-03-18T04:55:07.845Z"
}
```

### post: update_family_members
update an existing family member
- response object: status 200
```
{
    "uid": "LLFo4l95YVgYwsWbAN3QTGw6Bui1",
    "name": "Aamir",
    "age": "24",
    "rln": "brother",
    "aAt": "2020-03-18T04:55:07.845Z"
}
```

### post: delete_family_members
Delete a family member from users family
- response object: status 200
```{
    "success": true,
    "message": "Member deleted"
}
```

## Quiz :

### get: quiz_listing_by_topic
Get list of quiz with topic filter
- response object :  status 200
```
[
    {
        "titl": "दाँत साफ़, तो बच्चा स्वस्थ",
        "desc": "",
        "aAt": {
            "_seconds": 1555324200,
            "_nanoseconds": 0
        },
        "prt": 0,
        "cc": "दाँत साफ़, तो बच्चा स्वस्थ",
        "web_thumb": "https://saathealth-main.s3.ap-south-1.amazonaws.com/quiz2b-%E0%A4%A6%E0%A4%BE%E0%A4%81%E0%A4%A4+%E0%A4%B8%E0%A4%BE%E0%A4%AB%E0%A4%BC%2C+%E0%A4%A4%E0%A5%8B+%E0%A4%AC%E0%A4%9A%E0%A5%8D%E0%A4%9A%E0%A4%BE+%E0%A4%B8%E0%A5%8D%E0%A4%B5%E0%A4%B8%E0%A5%8D%E0%A4%A5.png",
        "thmb": "https://img.youtube.com/vi/G7a_nm9J6pE/0.jpg",
        "rAt": {
            "_seconds": 1555324,
            "_nanoseconds": 200000000
        },
        "web": true,
        "app": true,
        "eAt": {
            "_seconds": 1555353,
            "_nanoseconds": 0
        },
        "_id": "q170419",
        "tpc": [
            "dental",
            "health"
        ]
    },
    {
        "cc": "पहला दाँत, पहला ब्रश",
        "web_thumb": "https://saathealth-main.s3.ap-south-1.amazonaws.com/quiz2b-%E0%A4%AA%E0%A4%B9%E0%A4%B2%E0%A4%BE+%E0%A4%A6%E0%A4%BE%E0%A4%81%E0%A4%A4%2C+%E0%A4%AA%E0%A4%B9%E0%A4%B2%E0%A4%BE+%E0%A4%AC%E0%A5%8D%E0%A4%B0%E0%A4%B6.png",
        "thmb": "https://img.youtube.com/vi/G7a_nm9J6pE/0.jpg",
        "rAt": {
            "_seconds": 1555324,
            "_nanoseconds": 200000000
        },
        "web": true,
        "app": true,
        "eAt": {
            "_seconds": 1555353,
            "_nanoseconds": 0
        },
        "_id": "q150419",
        "tpc": [
            "dental",
            "health"
        ],
        "titl": "पहला दाँत, पहला ब्रश",
        "desc": "",
        "aAt": {
            "_seconds": 1555324200,
            "_nanoseconds": 0
        },
        "prt": 0
    },
    {
        "web_thumb": "https://saathealth-main.s3.ap-south-1.amazonaws.com/quiz112.jpg",
        "thmb": "https://img.youtube.com/vi/G7a_nm9J6pE/0.jpg",
        "rAt": {
            "_seconds": 1554114,
            "_nanoseconds": 600000000
        },
        "web": true,
        "app": true,
        "eAt": {
            "_seconds": 1555353,
            "_nanoseconds": 0
        },
        "_id": "-LbM6wZv5RaAq8kjzw6_",
        "tpc": [
            "dental",
            "health"
        ],
        "titl": "दाँतों की देखभाल",
        "desc": "",
        "aAt": {
            "_seconds": 1554114600,
            "_nanoseconds": 0
        },
        "prt": 0,
        "cc": "दाँतों की देखभाल "
    }
]
```

### get: quiz_questions
Get list of quiz questions of a quiz
- response object :  status 200

```
{
    "attempt": 12,
    "questions": [
        {
            "imc": false,
            "qId": "q01NOV19",
            "optn": [
                "उसे अलग बर्तन में बांटना चाहिए",
                "उबाले",
                "छाने",
                "कुछ नहीं"
            ],
            "popup": true,
            "rAt": {
                "_seconds": 1576392585,
                "_nanoseconds": 504000000
            },
            "ims": false,
            "qN": 1,
            "qst": "पीने का पानी सुरक्षित करने के लिए आपको क्या करना चाहिए ?",
            "qT": 1,
            "_id": "q01NOV191"
        },
        {
            "popup": true,
            "rAt": {
                "_seconds": 1576392585,
                "_nanoseconds": 587000000
            },
            "ims": false,
            "qN": 1,
            "qst": "बच्चों के लिए हाथ धोना क्यों ज़रूरी है?",
            "qT": 1,
            "_id": "q01NOV192",
            "imc": false,
            "qId": "q01NOV19",
            "optn": [
                "अच्छी महक के लिए",
                "स्वच्छता के लिए",
                "बीमारी से बचाव के लिए",
                "पता नहीं"
            ]
        },
        {
            "qN": 1,
            "qst": "आपके बच्चे के हाथ धोने के लिए कौन सा  समय सबसे महत्वपूर्ण है?",
            "qT": 1,
            "_id": "q01NOV193",
            "imc": false,
            "qId": "q01NOV19",
            "optn": [
                "सोने से पहले",
                "शौचालय का उपयोग करने के बाद",
                "खाने के बाद",
                "सुबह में"
            ],
            "popup": true,
            "rAt": {
                "_seconds": 1576392585,
                "_nanoseconds": 616000000
            },
            "ims": false
        },
        {
            "imc": false,
            "qId": "q01NOV19",
            "optn": [
                "पानी से",
                "पानी और साबुन से",
                "मालूम नहीं"
            ],
            "popup": true,
            "rAt": {
                "_seconds": 1576392585,
                "_nanoseconds": 619000000
            },
            "ims": false,
            "qN": 1,
            "qst": "आप अपने बच्चे के हाथ कैसे धोते हैं?",
            "qT": 1,
            "_id": "q01NOV194"
        }
    ]
}
```

### post: markQuizAnswere
Update a quiz question attempt and returns result of the quiz and reward points if any
- response object :  status 200

```
{
    "success": true,
    "correct": true,
    "points": 0
}
```
