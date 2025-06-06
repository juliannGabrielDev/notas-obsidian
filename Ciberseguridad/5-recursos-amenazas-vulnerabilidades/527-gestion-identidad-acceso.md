# Gestion de identidad y acceso
#ciberseguridad #curso-5 #modulo-2 

---
Seguridad es más que simplemente combinar procesos y tecnologías para proteger los recursos. En su lugar, la Seguridad consiste en garantizar que estos procesos y tecnologías están creando un entorno seguro que respalda una estrategia de defensa. Una clave para lograrlo es implementar dos principios fundamentales de Seguridad que limitan el acceso a los recursos de la organización:

- El **principio de privilegio mínimo** en el que a un usuario sólo se le concede el nivel mínimo de acceso y autorización requerido para completar una tarea o función.

- **Separación de funciones**, que es el principio según el cual no se debe conceder a los usuarios niveles de autorización que les permitan hacer un uso indebido de un sistema.

Ambos principios suelen apoyarse mutuamente. Por ejemplo, según el de menor privilegio, una persona que necesita permiso para aprobar las compras del departamento de informática no debería tenerlo para aprobar las compras de todos los departamentos. Del mismo modo, según la separación de funciones, la persona que puede aprobar las compras del departamento de TI debe ser diferente de la persona que puede introducir nuevas compras.

En otras palabras, el privilegio mínimo _limita_ _el acceso_ que recibe un individuo, mientras que la separación de funciones _divide las responsabilidades_ entre varias personas para evitar que una sola tenga demasiado control.
## Gestión de identidad y acceso (IAM)

ASÍ COMO las organizaciones dependen cada vez más de la tecnología, las agencias reguladoras han puesto más presión sobre ellas para que demuestren que están haciendo todo lo posible para prevenir las amenazas. La **gestión de identidad y** acceso (IAM) es un conjunto de procesos y tecnologías que ayuda a las organizaciones a gestionar las identidades digitales en su entorno. Tanto los sistemas AAA como los IAM están diseñados para autenticar a los usuarios, determinar sus privilegios de acceso y realizar un seguimiento de sus actividades dentro de un sistema.

Cualquiera de los dos Modelos utilizados por su organización es más que un sistema único y claramente definido. Cada uno de ellos consiste en una colección de Controles de seguridad que garantizan al _usuario adecuado_ el acceso a los _Recursos adecuados_ en el _momento adecuado_ y por las _razones adecuadas_. Cada uno de esos cuatro factores está determinado por las políticas y los procesos de su organización.
## Autenticación de usuarios

Para garantizar que el usuario correcto está intentando acceder a un recurso se requiere alguna forma de prueba de que el usuario es quien dice ser. En un [vídeo sobre controles de autenticación](https://www.coursera.org/learn/assets-threats-and-vulnerabilities/item/r6XuB), usted aprendió que hay unos cuantos factores que se pueden utilizar para autenticar a un usuario:

- **Conocimientos**, o algo que el usuario sabe

- **Responsabilidad**, o algo que el usuario posee

- **Característica**, o algo que el usuario es

La autenticación se verifica principalmente con las credenciales de inicio de sesión. El **inicio de sesión único** (SSO), una tecnología que combina varios inicios de sesión diferentes en uno, y la **autenticación de múltiples factores** (MFA), una medida de seguridad que requiere que un usuario verifique su identidad de dos o más formas para acceder a un sistema o red, son otras herramientas que las organizaciones utilizan para autenticar a las personas y los sistemas.
### **Aprovisionamiento de usuarios**

Los sistemas back-end deben ser capaces de verificar si la información facilitada por un usuario es correcta. Para lograrlo, los usuarios deben estar correctamente aprovisionados. El **Aprovisionamiento** de usuarios es el proceso de creación y mantenimiento de la identidad digital de un usuario. Por ejemplo, una universidad puede crear una nueva cuenta de usuario cuando se contrata a un nuevo instructor. La nueva cuenta se configurará para proporcionar acceso a los recursos exclusivos del instructor mientras esté impartiendo clase. Los analistas de seguridad participan habitualmente en el aprovisionamiento de usuarios y sus privilegios de acceso.
### **Conceder autorización**

Si se ha autenticado al usuario correcto, la red debe garantizar que se ponen a su disposición los recursos adecuados. Hay tres frameworks comunes que las organizaciones utilizan para manejar este paso de IAM:

- Control de acceso obligatorio (MAC)

- Control de acceso discrecional (DAC)

- Control de acceso basado en roles (RBAC)
### Control de acceso obligatorio (MAC)

MAC es el más estricto de los tres framework. La autorización en este Modelo se basa en una estricta necesidad de conocer. El acceso a la información debe ser concedido manualmente por una autoridad central o por el administrador del sistema. Por ejemplo, MAC se aplica comúnmente en las fuerzas del orden, el ejército y otros organismos gubernamentales en los que los usuarios deben solicitar el acceso a través de una cadena de mando. El MAC también se conoce como control no discrecional porque el acceso no se concede a discreción del Propietario de los datos.
### Control de acceso discrecional (DAC)

El DAC se aplica normalmente cuando el Propietario de los datos decide los niveles apropiados de accesibilidad. Un ejemplo de DAC es cuando el propietario de una carpeta de Google Drive comparte el acceso de editor, visualizador o comentarista con otra persona.
### Control de acceso basado en roles (RBAC)

El RBAC se utiliza cuando la autorización viene determinada por la función de un usuario dentro de una organización. Por ejemplo, un usuario del departamento de marketing puede tener acceso a los análisis de datos de los usuarios pero no a la administración de redes.
## Tecnologías de Control de acceso

Los usuarios suelen experimentar la autenticación y la autorización como una experiencia única y sin fisuras. En gran parte, eso se debe a las tecnologías de Control de acceso que están configuradas para trabajar juntas. Estas herramientas ofrecen la Velocidad y la Automatización que necesitan los administradores para monitorizar y modificar los derechos de acceso. También disminuyen los errores y los riesgos potenciales.

A veces, el departamento de TI de una organización desarrolla y mantiene por su cuenta tecnologías de control de acceso personalizadas. Un sistema IAM o AAA típico consta de un directorio de usuarios, un conjunto de herramientas para gestionar los datos de ese directorio, un sistema de autorización y un sistema de auditoría. Algunas organizaciones crean sistemas a medida para adaptarlos a sus necesidades de Seguridad. Sin embargo, crear una solución interna tiene un coste elevado de tiempo y otros recursos.

En su lugar, muchas organizaciones optan por adquirir licencias de soluciones de terceros que ofrecen un conjunto de herramientas que les permiten asegurar rápidamente sus sistemas de Información. Tenga en cuenta que la Seguridad es algo más que combinar un puñado de herramientas. Siempre es importante configurar estas tecnologías para que contribuyan a proporcionar un entorno seguro.