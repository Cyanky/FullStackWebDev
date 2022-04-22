## Transient:  
an object exists, it was defined....but not attached to a session or database (yet).
  
  ## Pending:   
  Some type of action has occurred but we have not yet decided to make it permanent yet. An object was attached to a session. "Undo" becomes available via db.session.rollback(). This means we can still clear any work that has been done so far. An object stays in this state until a flush happens!
  
  ## Flushed:   
  Translating actions(pending changes) into SQL commands that are ready to be committed. Nothing happens in the actual database yet. The only thing that can do that is 'commit'
    
    A flush takes pending changes and translates them into commands ready to be committed. It occurs:
when you call  
```  
Query. Or  

on db.session.commit()
  
  ```  
   
   A commit leads to persisted changes on the database + lets the db.session start with a new transaction.

  
  When a statement has been flushed already, SQLAlchemy knows not to do the work again of translating actions to SQL statements.
    
  ## Committed:  
  manually called for all pending changes to persist to the database permanently.   
  
  
