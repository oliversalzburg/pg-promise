Things to be done or under consideration for v2.0 of the library.

1. Remove `queryResult` from the global scope and add `use strict` to `index.js`.
    
    This one is done.
    
2. Throw away all unnecessary legacy aliases.

    Aliases thrown out:
    * `sequence`, with only `queue` remaining;
    * `queryRaw` and `raw`, with only `result` remaining;

3. Replace the default `Promise` with `Bluebird v3.0` when it is released,
   and align the release of `pg-promise v2.0` to that date.
   
   This one is not yet decided, but just makes sense, because `Bluebird`
   is really the best promise library available today.
   
4. Improve compatibility with other pg modules, primarily with `pg-query-stream`.
   Optionally, with `node-pg-copy-streams`, as its support is non-existent;
   
5. See if the library can accommodate another database altogether in the future,
   like mySQL, as it already has the perfect generic connection + transaction management.

6. Documentation require a major overhaul for 2.0

7. See if I can add protection to the protocol against calling generic `query`,
   and possibly, remove access to generic `query` completely.
