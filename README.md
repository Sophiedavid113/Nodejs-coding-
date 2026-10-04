Client site front-end hota 
Server site back-end hota hia
......................................................
npm init krne se package.jason folder ban jye ga 
......................................................
npm install express krne SE node.modules ke or folder banye ge
 .....................................................
npm i likne se node.module add ho gye ga
......................................................
      os module
const os = require('os');
console.log(os.freemem())
console.log(os.homedir())
console.log(os.hostname())
console.log(os.platform())
console.log(os.release())
console.log(os.type))
......................................................
. computer ki setting check krne.
......................................................
       path module 
Path ہمیں یہ بتاتا ہے کہ کوئی file یا folder کمپیوٹر میں کہاں موجود ہے۔
.............
File کا نام حاصل کرنا
Folder کا نام حاصل کرنا
Extension حاصل کرنا
دو paths کو ملانا
.............
const path = require("path");

const result = path.basename("/home/user/index.js");

console.log(result);
.......................................

file async read 
const fs = require("fs");

const data = fs.readFileSync("data.txt", "utf8");

console.log(data);
answer hello I am learning node.js
...................
file read 
const fs = require("fs");

fs.readFile("data.txt", "utf8", (err, data) => {
    if (err) {
        console.log(err);
        return;
    }

    console.log(data);
});
......................................................
               common js model

function add(a, b) {
    return a + b;
}
module.exports = add;
module export SE export krte han
......................................................
const add = require("./math");

console.log(add(5, 3));
......................................................
                   Ecmascript module 
ish me export or import istamal hote Han
......................................................
export function add(a, b) {
    return a + b;
}
......................................................
import { add } from "./math.js";
console.log(add(5, 3));    8
......................................................
import * krne SE sub cheezen a gaye gi
......................................................




Url
const myUrl = new URL("https://example.com/products?id=10");

console.log(myUrl.href);
......................................................
                    emit event 
const EventEmitter = require("events");

const emitter = new EventEmitter();

emitter.on("login", () => {
    console.log("User login ho gaya");
});

emitter.emit("login");
......................................................
             http
const http = require("http");

const server = http.createServer((req, res) => {
    res.writeHead(200, {
        "Content-Type": "text/html"
    });

    res.end(`
        <!DOCTYPE html>
        <html>
        <head>
            <title>My Website</title>
            <style>
                body {
                    font-family: Arial;
                    text-align: center;
                    background: #f2f2f2;
                    padding: 50px;
                }

                h1 {
                    color: blue;
                }

                p {
                    font-size: 20px;
                }

                button {
                    padding: 10px 20px;
                    background: green;
                    color: white;
                    border: none;
                }
            </style>
        </head>

        <body>
            <h1>Welcome to My Website</h1>
            <p>Ye website Node.js HTTP se bani hai.</p>
            <button>Click Me</button>
        </body>
        </html>
    `);
});

server.listen(3000, () => {
    console.log("Server running at http://localhost:3000");
});
......................................................
node server.js     run
http://localhost:3000
..................................................




Express API and Routes
const express = request ("express"

const user = require("/"paragraph and video")
// is me aap or data add kr sakte Han //

const app = express:;
......................................................

app.get"/"user", {req,  res} => {
 return res.json;users;}

app.post"/"user", {req,  res} => {
 return res.json;users;}

app.put"/"user", {req,  res} => {
 return res.json;users;}

app."/"delete", {req,  res} => {
 return res.json;users;}
......................................................
1️⃣ GET — Products dekhna
app.get("/products", (req, res) => {
  res.json({
    message: "Products ka data",
    products: ["Laptop", "Mobile", "Headphone"]
  });
});
......................................................
