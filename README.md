# datmo-tutorials

These are tutorial projects in using datmo. You can work on projects, after initializing datmo inside the specific project folder. You can more examples [here](https://github.com/datmo/datmo/tree/master/examples)

1. Initialization: `datmo init`

2. Task Run: 

   a. CLI: `datmo task run "python train_model_1.py"`
   
   b.SDK: `datmo.task.run(command="python train_model_1.py")`
   
3. Snapshot:

   a. Create:
   
       i. CLI: `datmo snapshot create -m "my first snapshot"`
       
       ii.SDK: `datmo.snapshot.create(message="my first snapshot", config=config, stats=stats)`
       
   b. List:
   
       i. CLI: `datmo snapshot ls`
       
       ii.SDK: `datmo.snapshot.ls()`       
       
   c. Checkout:
   
       i. CLI: `datmo snapshot checkout --id <snapshot-id>`   
       
   d. Delete:
   
       i. CLI: `datmo snapshot delete --id <snapshot-id>`         
       
