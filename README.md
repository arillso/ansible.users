# Docker Images: [Name]

## Description

## Build

Build from docker file

```
$ docker build -t sbaerlocher.users[name] .
```

Build from docker registry

```
docker pull sbaerlocher.users[name]
```

## run

```
docker run --restart=always -d \
    --name [name]  \
    -h [name].sbaerlo.ch \ 
    -v /:/ \
    -p : \
    sbaerlocher.users[name]
```

### Options


| Name                  | Values               | Behaviour                                                                          |
|:---------------------:|:--------------------:|:-----------------------------------------------------------------------------------|
|                       |                      |                                                                                    |
|                       |                      |                                                                                    |
|                       |                      |                                                                                    |
|                       |                      |                                                                                    |
|                       |                      |                                                                                    |
|                       |                      |                                                                                    |
|                       |                      |                                                                                    |
|                       |                      |                                                                                    |


#### Example:

```
docker run -e  ... sbaerlocher.users[name]
```

## Changelog

## Author

* [Simon Bärlocher](https://sbaerlocher.ch)
 
## License

This project is under the MIT License. See the [LICENSE](https://sbaerlo.ch/licence) file for the full license text.

## Copyright

(c) 2016, Simon Bärlocher