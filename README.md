# HATEOAS

[HATEOAS (Hypermedia as the Engine of Application State)](https://spring.io/understanding/HATEOAS) is a constraint of the REST application architecture. A hypermedia-driven site provides information to navigate the site's REST interfaces dynamically by including hypermedia links with the responses. This capability differs from that of SOA-based systems and WSDL-driven interfaces. With SOA, servers and clients usually must access a fixed specification that might be staged somewhere else on the website, on another website, or perhaps distributed by email. According with [Richardson maturity model](http://martinfowler.com/articles/richardsonMaturityModel.html) [HATEOAS](https://spring.io/understanding/HATEOAS) is final level of REST. One API is really [RESTful](https://en.wikipedia.org/wiki/Representational_state_transfer) when implements this standart. Access following address and see the magic.

```bash
	http://localhost:8080/person/findAll
```

```json
[  
    {  
        "idPerson":1,
        "firstName":"Person Name 1",
        "lastName":"Last Name 1",
        "address":"Some Address in Brasil 1",
        "links":[  
            {  
                "rel":"self",
                "href":"http://localhost:8081/erudio-restful-api/person/1"
            }
        ]
    },
    {  
        "idPerson":2,
        "firstName":"Person Name 2",
        "lastName":"Last Name 2",
        "address":"Some Address in Brasil 2",
        "links":[  
            {  
                "rel":"self",
                "href":"http://localhost:8081/erudio-restful-api/person/2"
            }
        ]
    }
]
```