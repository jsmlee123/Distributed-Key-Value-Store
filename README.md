# Distribute Key Value Datastore
- A simple Raft consensus based key value data store written in python
- A replica represents represents a member in the distribtued system.
- A Replica is activated by simply running ./kvstore

# Features
- Elections to decide on leader of distributed system
- Recovery after leader crash if majority of systems are alive
- Log matching and restoration/recovery