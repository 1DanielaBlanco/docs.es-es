---
title: Tipos de constructores (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 41fa7bde-8d20-4a3f-a3d2-fb791e128010
ms.openlocfilehash: 917c59a6602ce0313b91ba78fd59d11596f86e9f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54718590"
---
# <a name="constructing-types-entity-sql"></a>Tipos de constructores (Entity SQL)
[!INCLUDE[esql](../../../../../../includes/esql-md.md)] proporciona tres tipos de constructores: los constructores row, los constructores de tipo con nombre y colección.  
  
## <a name="row-constructors"></a>Constructores ROW  
 Los constructores ROW de [!INCLUDE[esql](../../../../../../includes/esql-md.md)] se usan para crear registros anónimos con tipo estructural de uno o más valores. El tipo de resultado de un constructor ROW es un tipo de fila cuyos tipos de campo corresponden a los tipos de los valores que se utilizaron para crear la fila. Por ejemplo, la expresión siguiente crea un valor de tipo `Record(a int, b string, c int)`:  
  
 `ROW(1 AS a, "abc" AS b, a + 34 AS c)`  
  
 Si no proporciona un alias para una expresión en un constructor ROW, Entity Framework intentará generar uno. Para obtener más información, vea la sección "Reglas de alias" en [identificadores](../../../../../../docs/framework/data/adonet/ef/language-reference/identifiers-entity-sql.md).  
  
 Las reglas siguientes se aplican a expresiones que usan alias en un constructor ROW:  
  
-   Las expresiones en un constructor ROW no pueden hacer referencia a otros alias del mismo constructor.  
  
-   Dos expresiones en el mismo constructor ROW no pueden tener el mismo alias.  
  
 Para obtener más información sobre los constructores row, vea [fila](../../../../../../docs/framework/data/adonet/ef/language-reference/row-entity-sql.md).  
  
## <a name="collection-constructors"></a>Constructores de colecciones  
 Los constructores de colecciones de [!INCLUDE[esql](../../../../../../includes/esql-md.md)] se usan para crear una instancia de un elemento multiset a partir de una lista de valores. Todos los valores del constructor deben ser del tipo `T` mutuamente compatible y el constructor genera una colección de tipo `Multiset<T>`. Por ejemplo, la expresión siguiente crea una colección de enteros:  
  
 `Multiset(1, 2, 3)`  
  
 `{1, 2, 3}`  
  
 No se permiten los constructores multiset vacíos porque no se puede determinar el tipo de los elementos. Lo siguiente no es válido:  
  
 `multiset() {}`  
  
 Para obtener más información, consulte [MULTISET](../../../../../../docs/framework/data/adonet/ef/language-reference/multiset-entity-sql.md).  
  
## <a name="named-type-constructors-namedtype-initializers"></a>Constructores de tipos con nombre (inicializadores NamedType)  
 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] permite a los constructores de tipos (inicializadores) crear instancias de tipos complejos con nombre y de tipos de entidad. Por ejemplo, la expresión siguiente crea una instancia de un tipo `Person`.  
  
 `Person("abc", 12)`  
  
 La expresión siguiente crea una instancia de un tipo complejo.  
  
 `MyModel.ZipCode(‘98118’, ‘4567’)`  
  
 La expresión siguiente crea una instancia de un tipo complejo anidado.  
  
 `MyModel.AddressInfo('My street address', 'Seattle', 'WA', MyModel.ZipCode('98118', '4567'))`  
  
 La expresión siguiente crea una instancia de una entidad con un tipo complejo anidado.  
  
 `MyModel.Person("Bill", MyModel.AddressInfo('My street address', 'Seattle', 'WA', MyModel.ZipCode('98118', '4567')))`  
  
 En el ejemplo siguiente se muestra cómo inicializar una propiedad de un tipo complejo en NULL. `MyModel.ZipCode(‘98118’, null)`  
  
 Los argumentos del constructor se supone que están en el mismo orden que en la declaración de los atributos del tipo.  
  
 Para obtener más información, consulte [denominado Constructor de tipo](../../../../../../docs/framework/data/adonet/ef/language-reference/named-type-constructor-entity-sql.md).  
  
## <a name="see-also"></a>Vea también
- [Referencia de Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
- [Información general sobre Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)
- [Sistema de tipos](../../../../../../docs/framework/data/adonet/ef/language-reference/type-system-entity-sql.md)
