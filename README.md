# Spacetime main commands

## Start CLI
```bash
spacetime start
```

## Create server
Tutorial: https://spacetimedb.com/docs/modules/rust/quickstart  
Repository [here](https://github.com/clockworklabs/SpacetimeDB/tree/master/modules/quickstart-chat)  
```bash
spacetime init --lang rust server
```

## Publish server
```bash
spacetime publish --project-path server quickstart-chat
```

## Debug
```bash
spacetime call quickstart-chat send_message 'Hello, World!'
spacetime logs quickstart-chat
spacetime sql quickstart-chat "SELECT * FROM message"
```

## Create client
Repository [here](https://github.com/clockworklabs/spacetimedb-typescript-sdk/tree/main/examples/quickstart-chat)  

```bash
npm create vite@latest client -- --template react-ts
cd client
npm install

npm install @clockworklabs/spacetimedb-sdk

mkdir -p client/src/module_bindings
spacetime generate --lang typescript --out-dir client/src/module_bindings --project-path server
npm run dev
```