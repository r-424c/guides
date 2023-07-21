<a target="_blank" href="https://app.eraser.io/workspace/gFSbU3NOXCd34DbQnfB6" id="edit-in-eraser-github-link"><img alt="Edit in Eraser" src="https://firebasestorage.googleapis.com/v0/b/second-petal-295822.appspot.com/o/images%2Fgithub%2FOpen%20in%20Eraser.svg?alt=media&amp;token=968381c8-a7e7-472a-8ed6-4a6626da5501"></a>
# Javascript (ES6+)
Documento para almacenar la teoria conocida de JS.x











## Funciones


## Parametros
- Parametros por **Referencia **(Pass by **_Reference_**).
- Parametros por **Valor  **(Pass by **_Value_**).




![image.png](https://eraser.imgix.net/workspaces/gFSbU3NOXCd34DbQnfB6/CyOUvapzv4SOz3NcsUILJBCmIRz2/8q0TA8zFcBIDQ53Jh1vF7.png?ixlib=js-3.7.0 "image.png")

> This gif is a good example.



Ejemplo: (Pass By Reference)

```
//javascript pass by reference
function callByReference(varObj) {
    console.log("Inside Call by Reference Method");
    varObj.a = 100;
    console.log(varObj); // { a: 100 }

}

let varObj = {
    a: 1
};

console.log("Before Call by Reference Method");
console.log(varObj); // { a: 1 }

callByReference(varObj)

console.log("After Call by Reference Method");
console.log(varObj); // { a: 100 }

}
```
...

Ejemplo: (Pass By Value)




<!--- Eraser file: https://app.eraser.io/workspace/gFSbU3NOXCd34DbQnfB6 --->