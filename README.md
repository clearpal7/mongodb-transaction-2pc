# mongodb-transaction-2pc
The transaction of MongoDb does not supported before 4.x.x version, 
This library will support the transaction, rollback into business application logic.

Just before a method which include CRUD DB login is called, the method interceptor will intercept the method.

1. before method invoke -> the two phase commit will be started. at that time, it will save the package class, method information, classLoader, a first local cache will be created

2. after method invoke -> after two phase commit will be finished. at this time we will check the transaction could be finish ordinarily.
