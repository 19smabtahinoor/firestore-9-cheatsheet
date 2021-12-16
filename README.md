# firestore-9-cheatsheet


### Initialization

```js
import { initializeApp } from "firebase/app";
import { getFirestore } from "firebase/firestore";

const config = {
  apiKey: "xxxx",
  authDomain: "xxxx",
  projectId: "xxxx",
  storageBucket: "xxxx",
  messagingSenderId: "xxxx",
  appId: "xxxx",
};


export const app = initializeApp(config);
export const db = getFirestore(app);
```


### Read doc/docs

#### Read collection
```js
const userCollectionRef = collection(db, "users");
getDocs(colref).then((res) => {
  res.docs.forEach((doc) => {
    console.log(doc.data());
  });
});
```
