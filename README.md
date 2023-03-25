# LABORATORIO 7
# ESCUELA COLOMBIANA DE INGENIERÍA
# CICLOS DE VIDA DEL DESARROLLO DE SOFTWARE - CVDS

## Finalización CI/CD - Manejo de Data - ORM
## PARTE II. USANDO SPRING DATA DESDE CERO
**Crea un nuevo repositorio en tu cuenta de github llamado cvds-7, y sigue lasinstrucciones delsiguiente tutorial de spring. https://medium.com/@saultobias13/a-quick-start-with-spring-boot-and-spring-data-jpa-32718a8f4706**
* Creación del proyecto:
<img src='https://user-images.githubusercontent.com/123812766/227719912-e1a61656-d445-4663-ab11-7664cc6de4f3.png' width=100% height=100%/>

* Luego de generarlo e importarlo en eclipse, en el pom.xml se evidencia las dependencias añadidas:
<img src='https://user-images.githubusercontent.com/123812766/227720371-21a5eeda-b5a2-49c4-8df9-b0728ecb0e09.png' width=50% height=50%/>

* Y en el paquete main encontramos la clase que va a ser el punto de entrada de la aplicación, esto lo sabemos por la anotación de @SpringBootApplication:
<img src='https://user-images.githubusercontent.com/123812766/227720518-c0196b8e-a9b0-4c49-9e9a-90d13d5304b9.png' width=50% height=50%/>

* Después, añadiendo las propiedades para la base de datos H2, en el archivo application.properties:
<img src='https://user-images.githubusercontent.com/123812766/227720729-7abd95b4-cf87-4bb5-8c97-4f208495a58a.png' width=50% height=50%/>

* Código de la clase Employee se encuentra en el proyecto.
* Se crea una interfaz de repositorio en el paquete com.santiyjuan.repository:
```
package com.santiyjuan.repository;

import org.springframework.data.jpa.repository.JpaRepository;
import org.springframework.stereotype.Repository;

import com.santiyjuan.model.Employee;

@Repository
public interface EmployeeRepository extends JpaRepository<Employee, Long>{

}
```
* Se creó un paquete com.santiyjuan.service
