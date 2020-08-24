---
title: Azure-erőforrások kezelése az Invoke-AzRestMethod használatával
description: Erőforrások kezelése az Invoke-AzRestMethod parancsmaggal az Azure PowerShellben.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.openlocfilehash: 380fd818a3af2474ce192c7a1da8a6798795cf21
ms.sourcegitcommit: bd7edc4d48b6a8a8bec864edc876e16af0a49505
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/18/2020
ms.locfileid: "88512997"
---
# <a name="manage-azure-resources-with-invoke-azrestmethod"></a>Azure-erőforrások kezelése az Invoke-AzRestMethod használatával

Az [Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) egy olyan Azure PowerShell-parancsmag, amely az Az PowerShell-modul 4.4.0-s verziójában lett bevezetve. Lehetővé teszi, hogy egyéni HTTP-kéréseket küldjön az Azure Resource Management (ARM) végpontjára az Az környezet használatával.

Ez a parancsmag akkor hasznos, ha az Azure-szolgáltatások olyan funkcióit szeretné felügyelni, amelyek még nem érhetők el az Az PowerShell-modulban.

## <a name="how-to-use-invoke-azrestmethod"></a>Az Invoke-AzRestMethod használata

Például engedélyezheti az Azure Container Registry (ACR) szolgáltatáshoz való hozzáférést megadott hálózatok számára, vagy letilthatja a nyilvános hozzáférést. Ez a funkció még nem érhető el az [Az.ContainerRegistry PowerShell-modulban](/powershell/module/Az.ContainerRegistry/).
Azonban ideiglenesen az `Invoke-AzRestMethod` használatával is felügyelhető.

## <a name="using-invoke-azrestmethod-with-get-operations"></a>Az Invoke-AzRestMethod használata GET műveletekkel

Az alábbi példa azt mutatja be, hogyan használható az `Invoke-AzRestMethod` parancsmag egy GET művelettel:

```azurepowershell-interactive
$getParams = @{
  ResourceGroupName = 'myresourcegroup'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  Name = 'myacr'
  ApiVersion = '2019-12-01-preview'
  Method = 'GET'
}
Invoke-AzRestMethod @getParams
```

A minél nagyobb rugalmasság érdekében az `Invoke-AzRestMethod` legtöbb paraméterének megadása nem kötelező.
Azonban ha egy erőforráscsoport erőforrásait szeretné kezelni, akkor valószínűleg meg kell adnia az erőforráshoz tartozó teljes azonosítót, illetve olyan paramétereket, mint például az erőforráscsoport, az erőforrás-szolgáltató és az erőforrástípus.

A `ResourceType` és a `Name` paraméterek több értéket is felvehetnek, ha a célként kijelölt erőforrások egynél több nevet igényelnek. A Log Analytics-munkaterület mentett keresésének módosításához az alábbi példához hasonlóan kell megadni a paramétereket: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.

A parancsmag egy tömbpozíción alapuló leképzés használatával a következő erőforrást hozza létre: `Id:'/workspaces/my-la/savedsearches/my-search'`.

Az `APIVersion` paraméter lehetővé teszi egy adott API-verzió használatát, beleértve az előzetes verziókat is. Az Azure-beli erőforrás-szolgáltatók által elérhető, támogatott API-verziókat az [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs) GitHub-adattár tartalmazza.

Az ACR 2019. 12. 01-i előzetes verziójának definíciója a következő helyen érhető el: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).

## <a name="using-invoke-azrestmethod-with-patch-operations"></a>Az Invoke-AzRestMethod használata PATCH műveletekkel

Az Invoke-AzRestMethod parancsmaggal letilthatja a `myacr` elnevezésű, `myresourcegroup` erőforráscsoportban található már létező ACR-hoz való nyilvános hozzáférést.

A nyilvános hálózati hozzáférés letiltásához az alábbi példában látható módon egy olyan API felé irányuló**PATCH** hívást kell létrehoznia, amely módosítja a `publicNetwokAccess` paraméter értékét:

```azurepowershell-interactive
$patchParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
     "publicNetworkAccess": "Disabled"
     } }'
  Method = 'PATCH'
}
Invoke-AzRestMethod @patchParams
```

A `Payload` tulajdonság egy olyan JSON-karakterlánc, amely megjeleníti a módosítani kívánt tulajdonság elérési útját.

Az API összes paraméterének leírását a hozzá tartozó **rest-api-spec** fájl tartalmazza.
A publicNetworkAccess paraméter konkrét definícióját az API 2019. 12. 01-i előzetes verziójának [tárolóregisztrációs adatbázisához tartozó JSON-fájl](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) tartalmazza.

Ha a beállításjegyzékhez való hozzáférést csak egy adott IP-cím számára szeretné engedélyezni, akkor a hasznos adatokat az alábbi példa szerint kell módosítani:

```azurepowershell-interactive
$specificIpParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
      "networkRuleSet": {
      "defaultAction": "Deny",
      "ipRules": [ {
         "action": "Allow",
         "value": "24.22.123.123"
         } ]
      }
  } }'
  -Method = 'PATCH'
}
Invoke-AzRestMethod @specificIpParams
```

## <a name="comparison-to-get-azresource-new-azresource-and-remove-azresource"></a>Összehasonlítás a Get-AzResource, New-AzResource és Remove-AzResource parancsmagokkal

Az `*-AzResource`-parancsmagok lehetővé teszik az Azure-hoz intézett REST API-hívás testreszabását az erőforrástípus, az API-verzió és a frissítendő tulajdonságok megadásával. A tulajdonságoknak azonban `PSObject` objektumoknak kell lenniük, amelyek létrehozása gyakran bonyolulttá válhat.

Az `Invoke-AzRestMethod` azonban egyszerűbb módot kínál az Azure-erőforrások kezelésére. Az előző példában láthatja, hogy a hasznos adatok egy JSON-sztringben vannak megadva. Nem kell vesződnie a JSON és a `PSObjects` objektumok közötti átalakítással.

Ha már van tapasztalata az `*-AzResource`-parancsmagok használatával kapcsolatban, továbbra is használhatja őket. Nem tervezzük a támogatásuk megszüntetését. A parancsmagok családjának legújabb tagja az `Invoke-AzRestMethod` parancsmag.

## <a name="see-also"></a>Lásd még:

* [Get-AzResource](/powershell/module/az.resources/get-azresource)
* [New-AzResource](/powershell/module/az.resources/new-azresource)
* [Remove-AzResource](/powershell/module/az.resources/remove-azresource)
