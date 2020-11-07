---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
ms.openlocfilehash: 7264733055322c3d5886ff57f50d22e23f932a7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672288"
---
# New-AzureRmResourceGroup

## Áttekintés
Azure-erőforráscsoportot hoz létre.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **New-AzureRmResourceGroup** parancsmag létrehoz egy Azure erőforrás-csoportot.
Erőforráscsoport létrehozásához csak egy nevet és egy helyet kell használnia, majd az New-AzureRmResource parancsmaggal hozhat létre erőforrásokat az erőforráscsoport hozzáadásához.
Ha egy meglévő erőforrás-csoporthoz szeretne bevezetést hozzáadni, használja az New-AzureRmResourceGroupDeployment parancsmagot. Ha egy erőforrást meglévő erőforráscsoporthoz szeretne hozzáadni, használja a **New-AzureRmResource** parancsmagot. Az Azure-erőforrás egy felhasználó által felügyelt Azure-entitás, például egy adatbázis-kiszolgáló, adatbázis vagy webhely. Az Azure-erőforráscsoport olyan Azure-erőforrások gyűjteménye, amelyek egységként települnek.

## Példák

### Példa 1: üres erőforráscsoport létrehozása
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US"
```

Ez a parancs olyan erőforráscsoportot hoz létre, amelynek nincs erőforrásai. A **New-AzureRmResource** és a **New-AzureRmResourceGroupDeployment** parancsmagok segítségével erőforrásokat és üzembe helyezheti az erőforrás-csoporthoz.

### 2. példa: üres erőforráscsoport létrehozása a pozicionális paraméterekkel
```
PS> New-AzureRmResourceGroup RG01 "South Central US"
```

Ez a parancs olyan erőforráscsoportot hoz létre, amelynek nincs erőforrásai.

### 3. példa: erőforráscsoport létrehozása címkékkel
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
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
Aliases: AzureRmContext, AzureCredential

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
Ha meg szeretné állapítani, hogy melyik hely támogatja az egyes erőforrás-típusokat, használja az Get-AzureRmResourceProvider parancsmagot a *ProviderNamespace* paraméterrel.

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
Miután címkéket rendelt az erőforrásokhoz és csoportokhoz, a *címke* paramétert használhatja Get-AzureRmResource és az Get-AzureRmResourceGroup az erőforrások és a csoportok megkereséséhez a címke neve vagy név és érték alapján. Címkéket használhat az erőforrások (például részleg vagy költséghely) kategorizálásához, illetve az erőforrásokkal kapcsolatos megjegyzések és megjegyzések nyomon követéséhez.
Az előre definiált címkék megtekintéséhez használja az Get-AzureRMTag parancsmagot.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Command. ResourceManagement. models. PSResourceGroup

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmResourceProvider](./Get-AzureRmResourceProvider.md)

[Get-AzureRmResourceGroup](./Get-AzureRmResourceGroup.md)

[Új – AzureRmResource](./New-AzureRmResource.md)

[Új – AzureRmResourceGroupDeployment](./New-AzureRmResourceGroupDeployment.md)

[Remove-AzureRmResourceGroup](./Remove-AzureRmResourceGroup.md)

[Set-AzureRmResourceGroup](./Set-AzureRmResourceGroup.md)
