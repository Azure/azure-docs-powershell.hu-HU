---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: b0d9d23b9563c38a985adfa3d12dfc2854319512
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843333"
---
# New-AzResourceGroup

## Áttekintés
Azure-erőforráscsoportot hoz létre.

## SZINTAXISA

```
New-AzResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **New-AzResourceGroup** parancsmag létrehoz egy Azure erőforrás-csoportot.
Erőforráscsoport létrehozásához csak egy nevet és egy helyet kell használnia, majd az New-AzResource parancsmaggal hozhat létre erőforrásokat az erőforráscsoport hozzáadásához.
Ha egy meglévő erőforrás-csoporthoz szeretne bevezetést hozzáadni, használja az New-AzResourceGroupDeployment parancsmagot. Ha egy erőforrást meglévő erőforráscsoporthoz szeretne hozzáadni, használja a **New-AzResource** parancsmagot. Az Azure-erőforrás egy felhasználó által felügyelt Azure-entitás, például egy adatbázis-kiszolgáló, adatbázis vagy webhely. Az Azure-erőforráscsoport olyan Azure-erőforrások gyűjteménye, amelyek egységként települnek.

## Példák

### Példa 1: üres erőforráscsoport létrehozása
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

Ez a parancs olyan erőforráscsoportot hoz létre, amelynek nincs erőforrásai. A **New-AzResource** és a **New-AzResourceGroupDeployment** parancsmagok segítségével erőforrásokat és üzembe helyezheti az erőforrás-csoporthoz.

### 2. példa: üres erőforráscsoport létrehozása a pozicionális paraméterekkel
```
PS> New-AzResourceGroup RG01 "South Central US"
```

Ez a parancs olyan erőforráscsoportot hoz létre, amelynek nincs erőforrásai.

### 3. példa: erőforráscsoport létrehozása címkékkel
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

A parancs üres erőforráscsoportot hoz létre. Ez a parancs ugyanaz, mint az 1-es parancs, kivéve, hogy címkéket rendel az erőforrás csoporthoz. Az első címkét, az üres nevet használja, az erőforrás-csoportok meghatározására használható. A második címke a "részleg" nevű osztály, és a marketing értéke. A felügyelethez vagy a költségvetéshez használhat olyan címkét is, mint például az ez az erőforrás-csoportok kategorizálásához.

## PARAMÉTEREK

### -ApiVersion
Az erőforrás-szolgáltató által támogatott API-verziót adja meg.
Az alapértelmezett verziótól eltérő verziót is megadhat.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hely
Az erőforráscsoport helyét adja meg. Adjon meg egy Azure Data Center helyet, például Nyugat-amerikai vagy Délkelet-ázsiai. Az erőforráscsoportok tetszőleges helyre helyezhetők. Az erőforráscsoport nem kell ugyanazon a helyen lennie az Azure-előfizetésben vagy ugyanazon a helyen, mint az erőforrás.
Ha meg szeretné állapítani, hogy melyik hely támogatja az egyes erőforrás-típusokat, használja az Get-AzResourceProvider parancsmagot a *ProviderNamespace* paraméterrel.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
Az erőforráscsoport nevét adja meg. Az erőforrás nevének egyedinek kell lennie az előfizetésben. Ha az adott nevű erőforráscsoport már létezik, a parancs a meglévő erőforráscsoport cseréje előtt kéri a megerősítést.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Címke
A kulcs-érték párok a hash-táblázatok formájában. Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"} a címke hozzáadásához vagy módosításához az erőforráscsoport címkéjének gyűjteményét kell lecserélnie.
Miután címkéket rendelt az erőforrásokhoz és csoportokhoz, a *címke* paramétert használhatja Get-AzResource és az Get-AzResourceGroup az erőforrások és a csoportok megkereséséhez a címke neve vagy név és érték alapján. Címkéket használhat az erőforrások (például részleg vagy költséghely) kategorizálásához, illetve az erőforrásokkal kapcsolatos megjegyzések és megjegyzések nyomon követéséhez.
Az előre definiált címkék megtekintéséhez használja az Get-AzTag parancsmagot.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Command. ResourceManagement. models. PSResourceGroup

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzResourceProvider](./Get-AzResourceProvider.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[Új – AzResource](./New-AzResource.md)

[Új – AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)
