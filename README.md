# Distribute Key Value Datastore
- A simple Raft consensus based key value data store written in python
- A replica represents represents a member in the distribtued system.
- A Replica is activated by simply running ./kvstore [Port no.] [Replica ID] [IDs of other replicas in system]

# Creating put and get requests:
- Put and Get requests must be in json format
- Requests must be sent through the specified localhost port
- Example Get request to get a value given key
  {"src": "<ID>", "dst": "<ID>", "leader": "<ID>", "type": "get", "MID": "<a unique string>", "key": "<some key>"}
  - A leader ID does not necessarily have to be correct as the distributed system will send back who the correct
    leader currently is
- Example Put request to put a key-value pair into the system
  {"src": "<ID>", "dst": "<ID>", "leader": "<ID>", "type": "put", "MID": "<a unique string>",
   "key": "<some key>", "value": "<value of the key>"}

# Features
- Elections to decide on leader of distributed system
- Recovery after leader crash if majority of systems are alive
- Log matching and restoration/recovery
- Recovery after system partitions