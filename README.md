# oasis-insight
EOS   block explorer and smart contract tools



```
var MongoClient = require('mongodb').MongoClient;
var url = "mongodb://localhost:27017/";

MongoClient.connect(url, function(err, db) {
  if (err) throw err;
  var dbo = db.db("EOS");
  var query = { trx_id: "bcb1dc616d2c2adea0c3edaa9179188b9d83a36fc22fb5b0bb53c1188566a36f" };
  dbo.collection("transactions").find(query).toArray(function(err, result) {
    if (err) throw err;
    console.log(result[0].actions);
    db.close();
  });
});


```
