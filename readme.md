## shintech-init-db

### Synopsis

Initialize Database

### Usage

#### queries/index.js

    import init from 'shintech-init-db'
    
    export {
      init
    }

#### server.js

    import {init} from './queries'

    const options = {
      app: express(),
      port: process.env.PORT || 8000,
      environment: process.env.NODE_ENV || 'development',
      logger: winston,
      packageName: pkg.name,
      config: config
    }
    
    options.db = init(options)
