# Dev - BE - database

This package is located at `src/db`, typically imported through

```text
import {doInDbConnection, QueryResponse, QueryA, QueryI} from '<path_to>/src/db';
```

## Executing SQL Queries

Typically done through `doInDbConnection()` method, which will be in a transaction of it's own, eg.

```text
await doInDbConnection(async(conn: Connection) => {
   // this block will be done in a transaction
   await conn.query(`....`);
});
```

## Processing SQL Selects

Use `QueryA` and `QueryI` to process the results of SQL selects eg.

```text
const q: QueryA = await conn.query(`
    SELECT ID, NAME, DESCRIPTION FROM TBL_MY_TABLE`);

// QueryA allows one to iterate over it, 
// each individual iteration results in a QueryI
for (const i of q) {
   // i can be of type QueryI
   const queryI: QueryI = i;
   
   const id: number = queryI.ID;
   const name: string = queryI.NAME;
   const description: string = queryI.DESCRIPTION;
   
   // we can acces metadata of columns as well
   // m can be of type QueryM as well
   const queryM: QueryM = i;
   
   // get the type of the column
   const columnType: string = queryM.meta.type;
}


```

## Processing SQL Updates

Use `QueryResponse` to process results of SQL updates, eg.

```text
const name: string = `...`;
const description: string = `...`;
const q: QueryResponse = await conn.query(`
     INSERT INTO TBL_MY_TABLE (NAME, DESCRIPTION) VALUES (?,?)`, 
     [name, description]);

// primary key of the inserted entry assuming it pk is auto-incremented
const pkOfNewlyInsertedEntry: number = q.insertId;

// how many rows did we insert? should be just 1 in this case
const affectedRows: number = q.affectedRows; 
          
```

