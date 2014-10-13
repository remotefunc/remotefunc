#RemoteFunc
RemoteFunc is a project that seeks create a lightweight remote function call
specification with the following properties:

* Lightweight
* Human Readable
* Programming Language and platform agnostic
* Simple

#Specification / Protocol
The protocol is split up into two parts. The first is how you figure out which
functions are available and general meta data about them. The second is how you
invoke a remote function.

##JSON Function Specification:
From the server you are able to get a specification from <serverurl>/spec.json. The specification can be used to either
implement a client or generate it. Following is an example JSON:
```json
{
    "FunctionName": {
        "Parameters": 3 //parameter count
    },
    ...
}
```

##JSON Function Invocation:
Do a post request to <serverurl>/FunctionName with the parameters for the
function as a list of JSON objects:
```json
[ //List Parameters (JSON Objects)
    {
        "StringAttributeName": "Data", //String
        "NumberAttributeName": 1, //Integer/Float
        "ObjectAttribute": {...} //Internal Struct / Object
    },
    {...}
]
```
Function names are case sensitive can only include letters and numbers.

#Implementations
The following section documents the implementations available.

##Server
##Client
