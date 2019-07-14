---
layout: post
title:  "Niveles De Accesibilidad"
---

Para miembros de clases hay diferentes niveles de accesibilidad.

Nivel De Accesibilidad | Significado
-----------------------|--------------
`public` | El acceso no es restringido
`protected` | Solo accesible para la clase que lo contiene o los tipos que heredan de esta clase
`private` | El acceso esta limitado a solo el tipo que lo contiene

Los miembros de los [enum](./structs_enums.html#Enumeraciones) son son `public` por default sin oportunidad de cambiarlos.

Los miembros de las [clases](./clases.html) son `private` de manera predefinida.

Las [interfaces](./interfaces.html) tienen en sus miembros como `public` de manera predefinida, esto no se puede cambiar.

Los [struct](./structs_enums.html##structuras) son `private` por default, se pueden hacer `public` o `private`.

Para mas información consulta:   
<https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/accessibility-levels>