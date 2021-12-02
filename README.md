<!--
 * @Author: your name
 * @Date: 2021-12-02 15:27:11
 * @LastEditTime: 2021-12-02 15:32:56
 * @LastEditors: Please set LastEditors
 * @Description: 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
 * @FilePath: \zwavejs2mqtt\README.md
-->
# install build and run

```bash
git clone https://github.com/zwave-js/zwavejs2mqtt
cd zwavejs2mqtt
yarn install
yarn run build
yarn start
```

# Development

Developers who wants to debug the application have to open two terminals.

In first terminal run `yarn dev` to start webpack-dev for front-end developing and hot reloading at <http://localhost:8092>
(**THE PORT FOR DEVELOPING IS 8092**)

In the second terminal run `yarn dev:server` to start the backend server with inspect and auto restart features

To package the application run `yarn pkg` command and follow the steps

## Developing against a different backend

By default running `yarn dev:server` will proxy the requests to a backend listening on _localhost_ on port _8091_.

If you want to run the development frontend against a different backend you have the following environment variables
that you can use to redirect to a different backend:

- **SERVER_HOST**: [Default: 'localhost'] the hostname or IP of the backend server you want to use;
- **SERVER_PORT**: [Default: '8091'] the port of the backend server you want to use;
- **SERVER_SSL**: [Default: undefined] if set to a value it will use _https_/_wss_ to connect to the backend;
- **SERVER_URL**: [Default: use the other variables] the full URL for the backend API, IE: `https://zwavetomqtt.home.net:8443/`
- **SERVER_WS_URL**: [Default: use the other variables] the full URL for the backend Socket, IE: `wss://zwavetomqtt.home.net:8443/`
