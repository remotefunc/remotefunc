#RemoteFunc
RemoteFunc is a project that seeks create a lightweight remote function call
specification with the following properties:

* Lightweight
* Human Readable
* Language and platform agnostic
* Simple

#Specification / Protocol

JSON Function Invocation:
```json
{
    "Remotefunc_version": "1.0", 
    "Function": "FunctionName", //Name of the function
    "Parameters": [ //List Parameters
        {
            "StringAttributeName": "Data", //String
            "NumberAttributeName": 1, //Integer/Float
            "ObjectAttribute": {...} //Internal Struct / Object
        },
        {...}
    ]
}
```

JSON Function Specification:
```json
{
    "FunctionName": {
        "Parameters": 3 //parameter count
    },
    ...
}
```

#Implementations
The following section documents the implementations available.

##Server
##Client
