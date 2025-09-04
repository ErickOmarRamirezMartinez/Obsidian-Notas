```Java
ServerSocket S = new ServerSocket(1234);

for(;;){
Socket cl = s accept();
ObjectOutputStream oos = new ObjectOutputStream(cl.getOutputStream());

ObjectInputStream ois = new ObjectInputStream(cl.getInputStream());

oos.writeInt(1);
oos.writeFloat(2.0f);

}
```


---

## Definicion de clase 


``` Java

import java.io.Seriable;

public class Datos Implements Seriable{

int v1;
Float v2;
String v3;


public Dato (int v1, float v2, String v3){

this.v1 = v1;
this.v2 = v2;
this.v3 = v3;
}
}

```


---


[Socket (Java Platform SE 8 )](https://docs.oracle.com/javase/8/docs/api/java/net/Socket.html)

![[Pasted image 20250904094242.png]]

---

