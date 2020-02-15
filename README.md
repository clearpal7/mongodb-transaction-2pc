# mongodb-transaction-2pc
The transaction of MongoDb does not supported before 4.x.x version, 
This library will support the transaction, rollback into business application logic.

Just before a method which include CRUD DB login is called, the method interceptor will intercept the method.


