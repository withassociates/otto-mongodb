[MongoDB][1] application for [Otto][2]

## Usage

Add as a dependency in your Appfile:

```
application {
    name = "example-app"

    dependency {
        source = "github.com/withassociates/otto-mongodb"
    }
}
```

Configure Rails app to use the containerized DB:

```rb
# config/mongoid.yml

development:
  sessions:
    default:
      database: example_db
      hosts:
        - mongodb.service.consul:27017
```

[1]: https://www.mongodb.com/
[2]: https://ottoproject.io/
