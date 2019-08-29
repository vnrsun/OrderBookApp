# Order Book
Order Book is a subsystem of an exchange, normally is called the trade engine.


mvn package
```

To run the package:

```
java -jar target/orderbook-0.0.1-SNAPSHOT.jar
```

## Test Using Curl

Add item to order book list
```
curl http://localhost:8090/market/add/item/InvestmentProfile
```

Get list
```
curl http://localhost:8090/market/list/get
```

Bid transaction
```
curl -H "Content-Type: application/json" -d '{"name":"Bonds", "price":"200", "qty":"20"}' -X POST http://localhost:8090/market/bid/add
```

Offer transaction
```
curl -H "Content-Type: application/json" -d '{"name":"InvestmentProfile", "price":"100", "qty":"10"}' -X POST http://localhost:8090/market/offer/add
```


Get market bid list
```
curl -H "Content-Type: application/json" -d '{"name":"InvestmentProfile"}' -X POST http://localhost:8090/market/bid/get
```

Get market offer list
```
curl -H "Content-Type: application/json" -d '{"name":"InvestmentProfile"}' -X POST http://localhost:8090/market/offer/get
```

Check out the file test.sh for more information on testing.





