![[Pasted image 20240527104325.png]]
```java
package com.pandevs.userPandevs.service;

  

import java.util.List;

  

import org.springframework.beans.factory.annotation.Autowired;

import org.springframework.stereotype.Service;

  

import com.pandevs.userPandevs.model.Signup;

import com.pandevs.userPandevs.repository.UserRepository;

  

@Service

public class SingupService {

// Tenemos que mandar a llamar a UserRepositor

private UserRepository userRepository;

//Inyectar la dependencias de UserRepository

@Autowired

public SingupService(UserRepository userRepository) {

this.userRepository = userRepository;

}

  

  

// getAll

public List<Signup> getAll(){

return userRepository.findAll();

}

}
```

---
![[Pasted image 20240527104343.png]]
```java
package com.pandevs.userPandevs.controller;

  

import java.util.List;

  

import org.springframework.beans.factory.annotation.Autowired;

import org.springframework.web.bind.annotation.GetMapping;

import org.springframework.web.bind.annotation.RequestMapping;

import org.springframework.web.bind.annotation.RestController;

  

import com.pandevs.userPandevs.model.Signup;

import com.pandevs.userPandevs.service.SingupService;

  

@RestController

@RequestMapping("/api/pandevs/user")

// CORS

public class SignupController {

//Mandamos a llamar Service

private final SingupService signupService;

  

//inyectando Dependencias (constructor)

@Autowired

public SignupController(SingupService signupService) {

this.signupService = signupService;

}

// Mapear metodos

@GetMapping

public List<Signup> getAllController(){

return signupService.getAll();

}

}
```

![[Pasted image 20240527104401.png]]

---
## Salida
![[Pasted image 20240527104414.png]]
![[Pasted image 20240527104424.png]]



---
![[Pasted image 20240527111959.png]]

---
![[Pasted image 20240527112623.png]]
![[Pasted image 20240527112634.png]]
![[Pasted image 20240527112640.png]]


---

[Query Language](https://docs.spring.io/spring-data/jpa/reference/jpa/query-methods.html)


