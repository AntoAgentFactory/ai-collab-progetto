[12:18:04.963] ERROR (#10937): failed {
  ref: "err_6bc1693f",
  error: 49 | 			hash text NOT NULL,
50 | 			created_at numeric,
51 | 			name text,
52 | 			applied_at TEXT
53 | 		)
54 | 	`);let G=yield*Y.all(O`SELECT id, hash, created_at, name FROM ${O.identifier(X)}`);if(typeof $==="object"&&$.init){if(G.length)return yield*new u8({exitCode:"databaseMigrations"});if(_.length>1)return yield*new u8({exitCode:"localMigrations"});let[U]=_;if(!U)return;yield*Y.run(O`insert into ${O.identifier(X)} ("hash", "created_at", "name", "applied_at") values(${U.hash}, ${U.folderMillis}, ${U.name}, ${new Date().toISOString()})`);return}let W=w0({localMigrations:_,dbMigrations:G});if(W.length===0)return;yield*Y.transaction((U)=>P_(function*(){for(let J of W){for(let N of J.sql)yield*U.run(O.raw(N));yield*U.run(O`insert into ${O.identifier(X)} ("hash", "created_at", "name", "applied_at") values(${J.hash}, ${J.folderMillis}, ${J.name}, ${new Date().toISOString()})`)}}))});class HX extends n8{client;relations;options;static[z]="EffectSQLiteSession";constructor(_,Y,$,X){super(Y);this.client=_;this.relations=$;this.options=X}prepareQuery(_,Y,$,X,H,G){return new XX((W,U)=>this.execute(_,W,U),_,this.options.logger

SQLiteError: no such column: replacement_seq
      errno: 1,
 byteOffset: -1,

      at prepare (unknown:1:1)
      at prepare (bun:sqlite:345:37)
      at query (bun:sqlite:367:28)
      at B:/~BUN/root/chunk-ewhq5ttw.js:54:29002
      at runLoop (B:/~BUN/root/chunk-rdb6g37s.js:25:2045)
      at evaluate (B:/~BUN/root/chunk-rdb6g37s.js:25:1435)
      at B:/~BUN/root/chunk-rdb6g37s.js:25:5664
      at aY (B:/~BUN/root/chunk-rdb6g37s.js:25:39087)
      at evaluate (B:/~BUN/root/chunk-rdb6g37s.js:25:1691)
      at B:/~BUN/root/chunk-rdb6g37s.js:25:5664
      at B:/~BUN/root/chunk-rdb6g37s.js:25:22490
      at evaluate (B:/~BUN/root/chunk-rdb6g37s.js:25:1691)
      at B:/~BUN/root/chunk-rdb6g37s.js:25:5664
      at B:/~BUN/root/chunk-rdb6g37s.js:25:22490
      at evaluate (B:/~BUN/root/chunk-rdb6g37s.js:25:1691)
      at B:/~BUN/root/chunk-rdb6g37s.js:25:5664
      at aY (B:/~BUN/root/chunk-rdb6g37s.js:25:39087)
      at ~effect/Effect/evaluate (B:/~BUN/root/chunk-rdb6g37s.js:25:4492)
      at runLoop (B:/~BUN/root/chunk-rdb6g37s.js:25:2045)
      at evaluate (B:/~BUN/root/chunk-rdb6g37s.js:25:1435)
      at B:/~BUN/root/chunk-rdb6g37s.js:25:5664
      at processTicksAndRejections (native:7:39)
,
  cause: "SQLiteError: no such column: replacement_seq\n    at prepare (unknown)\n    at prepare (bun:sqlite:345:37)\n    at query (bun:sqlite:367:28)\n    at <anonymous> (B:/~BUN/root/chunk-ewhq5ttw.js:54:29002)\n    at runLoop (B:/~BUN/root/chunk-rdb6g37s.js:25:2045)\n    at evaluate (B:/~BUN/root/chunk-rdb6g37s.js:25:1435)\n    at <anonymous> (B:/~BUN/root/chunk-rdb6g37s.js:25:5664)\n    at aY (B:/~BUN/root/chunk-rdb6g37s.js:25:39087)\n    at evaluate (B:/~BUN/root/chunk-rdb6g37s.js:25:1691)\n    at <anonymous> (B:/~BUN/root/chunk-rdb6g37s.js:25:5664)\n    at <anonymous> (B:/~BUN/root/chunk-rdb6g37s.js:25:22490)\n    at evaluate (B:/~BUN/root/chunk-rdb6g37s.js:25:1691)\n    at <anonymous> (B:/~BUN/root/chunk-rdb6g37s.js:25:5664)\n    at <anonymous> (B:/~BUN/root/chunk-rdb6g37s.js:25:22490)\n    at evaluate (B:/~BUN/root/chunk-rdb6g37s.js:25:1691)\n    at <anonymous> (B:/~BUN/root/chunk-rdb6g37s.js:25:5664)\n    at aY (B:/~BUN/root/chunk-rdb6g37s.js:25:39087)\n    at SessionContextEpoch.requestReplacement (B:/~BUN/root/chunk-1mh5rrxd.js:4:11760)\n    at SessionContextEpoch.requestReplacement (definition) (B:/~BUN/root/chunk-1mh5rrxd.js:4:2943)\n    at SessionPrompt.createUserMessage (B:/~BUN/root/chunk-qsm4x2aj.js:1030:363)\n    at SessionPrompt.createUserMessage (definition) (B:/~BUN/root/chunk-qsm4x2aj.js:1029:1983)\n    at SessionPrompt.prompt (B:/~BUN/root/chunk-mr03zdma.js:3:13187)\n    at SessionPrompt.prompt (definition) (B:/~BUN/root/chunk-qsm4x2aj.js:1030:247)\n    at SessionHttpApi.prompt (B:/~BUN/root/chunk-mr03zdma.js:2:79248)\n    at SessionHttpApi.prompt (definition) (B:/~BUN/root/chunk-mr03zdma.js:3:13099)",
}
[91m[1mError: [0m{
  "name": "UnknownError",
  "data": {
    "message": "Unexpected server error. Check server logs for details.",
    "ref": "err_6bc1693f"
  }
}
