# Assignment #1: gRPC and REST API Implementation

## Member

1. อานันท์ เมธเศรษฐ 6031061021
2. นิศรุจ รัตนอร่าม 6031033521
3. ถาวร กังวาลสิงหนาท 6030226121
4. สรวิศ สุนทวัฒโรดม 6031057621
5. Narin Trakarnvanich 6030320421
6. Nathaphum Niyomsathien 6031014621

## API Documentation

`localhost:8080/api-docs`

![Swagger](https://github.com/2110521-2563-1-Software-Architecture/soft-arch-hw-1/raw/master/images/swagger.png)

## Source code

- [REST API server](https://github.com/2110521-2563-1-Software-Architecture/soft-arch-hw-1/tree/master/src)
- [gRPC server](https://github.com/2110521-2563-1-Software-Architecture/soft-arch-hw-1/tree/master/gRPC)
- [Clients](https://github.com/2110521-2563-1-Software-Architecture/soft-arch-hw-1/tree/master/client)

## gRPC & REST API methods

| Functions           | gRPC       | REST API             |
| ------------------- | ---------- | -------------------- |
| List books          | `list()`   | `GET /book/list`     |
| Find a book by id   | `get()`    | `GET /book/{id}`     |
| Insert a book       | `insert()` | `POST /book/create`  |
| Delete a book by id | `delete()` | `DELETE /book/{id} ` |

## What are the main differences between REST API and gRPC?

The main difference is the format of payload. REST's payload is JSON which is not
type stricted while gRPC uses Protobuf message which is smaller. REST also uses HTTP/1 by default while gRPC uses HTTP/2 which is much faster.

## What is the benefits of introduce interface in front of the gRPC and REST API of the book services.

Interface helps us call gRPC and REST API service by using the same method. We can also implement other services by using the interface.

## Based on the introduced interface, compare how to call the methods based on gRPC and REST API

| Functions           | gRPC                       | REST API                   |
| ------------------- | -------------------------- | -------------------------- |
| List books          | `BookInterface.list()`     | `BookInterface.list()`     |
| Find a book by id   | `BookInterface.findById()` | `BookInterface.findById()` |
| Insert a book       | `BookInterface.insert()`   | `BookInterface.insert()`   |
| Delete a book by id | `BookInterface.delete()`   | `BookInterface.delete()`   |

## Draw a component diagram representing the book services with and without interfaces.

![Component Diagram](https://github.com/2110521-2563-1-Software-Architecture/soft-arch-hw-1/raw/master/images/diagram.png)