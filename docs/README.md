# System Concept

Based on the [original task description](../resources/README.md) the following technical requirements extracted: 

- Due to the size of the CSV, the data should be loaded into a database and apply/tune the filtering there.
- Backend application public interface should be REST over HTTP, due to its wide support in many client devices.
- To increase a robustness and scalability, the app components should be containerised and also the database requires an HA setup
- From the functional perspective the following modules considered to be implemented:
    - Backend Sync Service (Python app with Pandas, Dask and SQLAlchemy)
    - Client Backend Application (Python app with FastAPI and SQLAlchemy)
    - Database (MySQL innoDB cluster)
  
![System Concept](system-concept.png)