---
title: Produtos
description: Este tema ofrece información sobre o catálogo de produtos que pode usar para proporcionar información aos clientes sobre os produtos e os prezos que ofrece a súa organización.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 085b7e4d9274f8c8d94d7a84109cfa782acf3dbb9241bfd25ecb8c2f329e1bb8
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986849"
---
# <a name="products"></a>Produtos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Os productos son a rede central do seu negocio. O catálogo de produtos en Dynamics 365 Sales Professional é un conxunto de produtos e a súa información de prezos. Facilite as cousas para que os seus representates de vendas aumenten as súas vendas creando un catálogo de produtos rapidamente.

## <a name="add-a-product"></a>Engadir un produto

1.  Asegúrese de dispoñer da función de administrador do sistema ou de xestor de Sales Professional para poder engadir produtos en Dynamics 365 Sales Professional.
2.  No mapa do sitio, en **Configuración**, seleccione **Produtos**.
3.  Seleccione **Engadir produto** e encha a seguinte información:

    -  **Nome**
    -  **Identificador do produto**
    -  **Principal**: Seleccione unha familia de produtos principal para o produto. Se está a crear un produto secundario nunha familia de produtos, o nome da familia de produtos principal introdúcese aquí. Isto non se pode cambiar despois de gardar o rexistro.
    -  **Válido desde**/**Válido ata**: Defina o período para o que é válido o produto seleccionando as datas **Válido desde** e **Válido ata**.
    -  **Grupo de unidades**: Seleccionar unha unidade de grupos. Un grupo de unidades é unha colección de varias unidades en que se vende un produto e define como se agrupan os elementos individuais en cantidades máis grandes. Por exemplo, se está a engadir sementes como un produto, pode que creara un grupo de unidades chamado "Sementes", e efinira a súa unidade primaria como "paquete."
    -  **Unidade predefinida**: Seleccione a unidade máis común na que se venderá o produto. As unidades son as cantidades ou medidas en que se venden os produtos. Por exemplo, se está a engadir sementes como un produto, pode vendelas en paquetes, caixas ou pallets. Cada unha destas convértese nunha unidade do produto. Se a maioría das sementes se vende en paquetes, seleccione paquetes como a unidade.
    -  **Lista de prezos predefinida**: Se é un produto novo, este campo é de só lectura. Antes de que poida seleccionar unha lista de prezos predefinida, debe encher todos os campos obrigatorios, e despois gardar o rexistro. A pesar de que a lista de prezos non é obrigatoria, despois de gardar o rexistro do produto é aconsellable definir unha lista de prezos predefinida para cada produto. Logo, se o rexistro dun cliente non contén una lista de prezos, Sales pode utilizar a lista de prezos predefinida para xerar ofertas, pedidos e facturas.
    -  **Decimais admitidos**: Introduza un número enteiro entre 0 e 5. Se o produto non se pode dividir en cantidades fraccionais, introduza 0. A precisión do campo **Cantidade** no rexistro do produto da oferta, do pedido ou da factura valídase en comparación co valor neste campo se o produto non ten unha lista de prezos asociada.
    -  **Asunto**: Asocie este produto a un asunto. Pode utilizar os asuntos para colocar os produtos en categorías e para filtrar informes.

4.  Seleccione **Gardar**.
5.  No separador **Detalles adicionais**, na sección **Elementos da lista de prezos**, seleccione **Máis comandos** e despois seleccione **Engadir novo elemento da lista de prezos**.
7.  No separador **Detalles adicionais**, na sección **Relación de produtos**, seleccione a icona **Máis comandos** e despois seleccione **Engadir nova relación de produtos.**
8.  No formulario **Nova relación de produto**, introduza os seguintes detalles e, na barra de comandos, seleccione **Gardar e pechar**:

    -   **Produto relacionado**: Seleccione un produto que desexa engadir como produto relacionado para o rexistro do produto existente co que está a traballar.
    -   **Tipo de relación de vendas**: Seleccione se desexa engadir o produto como unha incremento das vendas, vendas cruzadas, accesorio ou produto de substitución.
    -   **Dirección**: Seleccione se a relación entre os produtos será dunha dirección ou de dúas direccións. Cando se selecciona unha dirección, o produto que selecciona en **Produto Relacionado** mostraráselle como recommendation para o produto existente, pero non viceversa.

9.  No formulario de produto, seleccione **Gardar**.

## <a name="import-products"></a>Importar produtos

Pode usar modelos de importación para introducir datos de produto en masa en Dynamics 365 Sales.

## <a name="revise-a-product"></a>Revisar un produto

Manteña o inventario de produtos actualizado revisando rapidamentede as propiedades dos produtos conforme se requira, e publicando de novo a información de forma que os seus axentes de vendas poidan ver as modificacións máis recentes no inventario.

1.  Asegúrese de dispoñer dun dos seguintes roles de seguranza ou permisos equivalentes: administrador do sistema, personalizador do sistema, xestor de vendas, vicepresidente de vendas, vicepresidente de márketing ou CEO-xestor empresarial.
2.  No mapa do sitio, seleccione **Produtos**.
3.  Abra un produto que desexe cambiar e, na barra de comandos, seleccione **Revisar**.
4.  Na caixa de diálogo **Confirmar Revisar**, seleccione **Confirmar**. Isto modifica o estado do produto para **En Revisión**.
5.  Despois de facer cambios, na barra de comandos, seleccione **Publicar**.

    > [!TIP]
    > Para reverter os cambios e continuar coa última versión activa do produto, seleccione **Reverter**. Isto muda o estado do produto de novo para **Activo**.

## <a name="clone-a-product"></a>Clonar un produto 

Cando está a crear un novo produto, aforre tempo clonando un xa existente. Isto crea unha copia do rexistro orixinal con todos os detalles agás o nome e o ID.

1.  Asegúrese de dispoñer dun dos seguintes roles de seguranza ou permisos equivalentes: administrador do sistema, personalizador do sistema, xestor de vendas, vicepresidente de vendas, vicepresidente de márketing ou CEO-xestor empresarial.
2.  No mapa do sitio, seleccione **Produtos**.
3.  Seleccione un rexistro de produto que desexa clonar e, na barra de comandos, seleccione **Clonar**. Aparecerá unha caixa de diálogo de confirmación.
4.  Seleccione **Confirmar**.

Abrirase un novo rexistro de produto cos mesmos detalles que a orixinal agás o nome e o ID.

## <a name="retire-a-product"></a>Retirar un produto 

Se a súa organización xa non vende un produto, retíreo para que o produto xa non estea dispoñible para os axentes de vendas.

1.  Asegúrese de dispoñer da función de administrador do sistema ou de xestor de Sales Professional ou permisos equivalentes.
2.  No mapa do sitio, seleccione **Produtos**.
3.  Abra un produto que desexe retirar e, na barra de comandos, seleccione **Retirar**.
4.  Na caixa de diálogo **Confirmar Retirar**, seleccione **Confirmar**.


## <a name="delete-a-product"></a>Eliminar un produto

Para deter a venda dun produto, elimíneo.

> [!IMPORTANT]
> Non se pode recuperar un rexistro eliminado.

1.  Asegúrese de dispoñer da función de administrador do sistema ou de xestor de Sales Professional ou permisos equivalentes.
2.  No mapa do sitio, seleccione **Produtos**.
3.  Seleccione un rexistro de produto que desexa eliminar e, na barra de comandos, seleccione **Eliminar**.
4.  Na caixa de diálogo **Confirmar eliminación**, seleccione **Continuar**.
 
 ## <a name="quantity-factors-for-products"></a>Factores de cantidade para produtos

Os factores de cantidade apoian a venda de produtos baseados en subscrición. Para os produtos baseados en subscrición, a cantidade na liña de oferta ou contrato de proxecto exprésase como o número de meses de usuario.

Normalmente, o prezo do software de subscrición almacénase no catálogo como o prezo por usuario ao mes. Non obstante, pode usar outras descricións de tempo no seu lugar. Durante o proceso de vendas, o prezo na liña de oferta adoita ser o prezo por usuario, por mes que foi negociado e descontado polo axente de vendas de TI. Cada acordo ten un número diferente de usuarios e un número diferente de meses de subscrición. A cantidade que se utiliza para calcular a cantidade da liña de oferta é un produto do número de usuarios e do número de meses de subscrición.

Os factores de cantidade dependen dos atributos do produto. Ao configurar propiedades específicas para un produto, pode marcar un subconxunto destas propiedades ou de todas as propiedades como factores de cantidade.

O sistema valida que só as propiedades numéricas ou propiedades de produto que teñen un tipo de datos numéricos estean marcadas como factores de cantidade. Cando un produto para o que se configuran os factores de cantidade se engade a unha liña de presupostos, o campo **Cantidade** na liña de oferta convértese nun campo de só lectura. Despois de introducir valores para as propiedades do produto que son factores de cantidade, calcúlase a cantidade da liña de oferta.

Por exemplo, se hai as seguintes propiedades: 

- **N.º de usuarios**: O número de usuarios 
- **Nº de meses**: O número de meses de subscrición
- **SKU de produto** 

As propiedades **N.º de Usuarios** e **N.º de meses** pódense marcar como factores de cantidade editando as propiedades da liña de produtos. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]