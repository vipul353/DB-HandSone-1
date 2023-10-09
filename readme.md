## MongoDB Commands for Human Resource Database

### Create a Database and Collection
```bash
use Human_Resource
db.createCollection("employee")

db.employee.find({})


db.employee.find({ "salary": { $gt: "30000" } })

db.employee.find({ "overallExp": { $gt: "2" } })

db.employee.find({ "yearGrad": { $gt: "2015" }, "overallExp": { $gt: "1" } })

db.employee.updateMany({ "salary": { $gt: "70000" } }, { $set: { "salary": "65000" } })


db.employee.deleteMany({ "lastCompany": "Y" })
