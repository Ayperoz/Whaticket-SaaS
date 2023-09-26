# Whaticket-SaaS
<h1> INICIANDO INSTRUCTIVO DE INSTALACIÓN LOCAL </h1> <br>
-- ENTORNO --<br>
  Ubuntu 20.04.6 LTS<br>
  4GB Ram 3200<br>
  4 Npucleos 3.0GHz<br>
  Virtual - VMware - ESXI<br>
<br><br>
-- REQUISITOS PREVIOS --<br>
  NodeJS V18.18.0 LTS<br>
  PostgresSQL<br>
  Redis-server<br>

-- INSTALACIÓN --<br>
git clone https://github.com/Ayperoz/Whaticket-SaaS whaticket<br>
cd /whaticket/backend/<br>
cp .env.example .env<br>
<br>
---------------------------------<br>
(editamos el archivo .env con nuestros datos, en mi caso sería)<br>
NODE_ENV=DEVELOPMENT<br>
BACKEND_URL=http://localhost<br>
FRONTEND_URL=http://localhost:3000<br>
PROXY_PORT=8080<br>
PORT=8080<br>

DB_DIALECT=postgres<br>
DB_HOST=localhost<br>
DB_PORT=5432<br>
DB_USER=postgres<br>
DB_PASS=Simple2020<br>
DB_NAME=testing<br>
<br>
JWT_SECRET=kZaOTd+YZpjRUyyuQUpigJaEMk4vcW4YOymKPZX0Ts8<br>
JWT_REFRESH_SECRET=dBSXqFg9TaNUEDXVp6fhMTRLBysP+j2DSqf7+raxD3A<br>
<br>
REDIS_URI=<br>
REDIS_OPT_LIMITER_MAX=1<br>
REDIS_OPT_LIMITER_DURATION=3000<br>
<br>
USER_LIMIT=10<br>
CONNECTIONS_LIMIT=2<br>
CLOSED_SEND_BY_ME=true<br>
<br>
FACEBOOK_APP_ID=<br>
FACEBOOK_APP_SECRET=<br>
<br>
VERIFY_TOKEN=whaticket<br>
---------------------------------<br>
<br>
npm install<br>
npm run build<br>
npx sequelize db:migrate<br>
npx sequelize db:seed:all<br>
(para confirmar podemos iniciar el backend con el comando npm start)<br>
cd ..<br>
cd frontend/<br>
cp .env.example .env<br>
<br>
---------------------------------<br>
(editamos el archivo .env con nuestros datos, en mi caso sería)<br>
REACT_APP_BACKEND_URL=https://localhost<br>
REACT_APP_HOURS_CLOSE_TICKETS_AUTO = 24<br>
REACT_APP_FACEBOOK_APP_ID=<br>
PORT=3000<br>
---------------------------------<br>
npm install<br>
<br>
inicializamos frontend y backend en dos terminales por<br> separado con el comando npm start.<br>
Eso seria todo en cuanto a la instalación, ahora verificaré<br> los errores en caso de encontrarlos y los corregiré de uno en uno.


