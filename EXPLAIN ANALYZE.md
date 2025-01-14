It is a Postgres command that:
- Accepts a statement such as `SELECT ...`, `UPDATE ...`, or `DELETE ...`
- executes the statement
- provides a query plan detailing what approach the planner took to executing the statement provided, instead of returning the data

**Information provided:**
1. **Execution Plan**:
    - The detailed execution plan used by the DBMS to execute the SQL query.
2. **Estimated Costs**:
    - Estimated costs for each operation in the execution plan, based on database statistics.
3. **Actual statistics** :
    - Actual time taken by each step in query execution, number of rows returned, etc.

**Usefulness:**
- Provides a detailed view of how the DBMS interprets and executes the SQL query.
- Helps identify real bottlenecks in DBMS performance and potential areas for improvement, such as indexing, joins, etc.
## Explain vs Explain Analyze

The difference between explain & explain analyze is that the former **generates the query plan by estimating the cost**, while the latter actually **executes the query**.

Thus, explain analyze will give you more accurate query plan / cost.

[[Index (RDBMS)]]

