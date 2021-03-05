---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: e32d5f53b13b26a93f23e4e557c6bad20911a776
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008613"
---
# New-AzResourceGroup

## SYNOPSIS
Létrehoz egy Azure-erőforráscsoportot.

## SZINTAXIS

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzResourceGroup** parancsmag létrehoz egy Azure-erőforráscsoportot.
Létrehozhat egy erőforráscsoportot úgy, hogy csak egy nevet és egy helyet használ, majd a New-AzResource parancsmag használatával erőforrásokat hozhat létre az erőforráscsoporthoz való hozzáadáshoz.
Ha egy meglévő erőforráscsoporthoz szeretne központi telepítést hozzáadni, használja a New-AzResourceGroupDeployment parancsmagot. Ha erőforrást szeretne hozzáadni egy meglévő erőforráscsoporthoz, használja a **New-AzResource** parancsmagot. Az Azure-erőforrás egy felhasználó által felügyelt Azure-entitás, például egy adatbázis-kiszolgáló, adatbázis vagy webhely. Az Azure-erőforráscsoportok egy egységként üzembe helyezett Azure-erőforrások gyűjteményei.

## PÉLDÁK

### 1. példa: Üres erőforráscsoport létrehozása
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

Ez a parancs olyan erőforráscsoportot hoz létre, amely nem rendelkezik erőforrásokkal. A **New-AzResource** vagy **a New-AzResourceGroupDeployment** parancsmagokkal erőforrásokat és telepítéseket adhat ehhez az erőforráscsoporthoz.

### 2. példa: Üres erőforráscsoport létrehozása pozícióparaméterek használatával
```
PS> New-AzResourceGroup RG01 "South Central US"
```

Ez a parancs olyan erőforráscsoportot hoz létre, amely nem rendelkezik erőforrásokkal.

### 3. példa: Erőforráscsoport létrehozása címkékkel
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

Ez a parancs egy üres erőforráscsoportot hoz létre. Ez a parancs ugyanaz, mint az 1. példa parancsa, azzal a kivételvel, hogy címkéket rendel az erőforráscsoporthoz. Az első üres címke segítségével azonosíthatók az erőforrásokkal nem kapcsolatos erőforráscsoportok. A második címke neve Részleg, értéke Marketing. Az ehhez hasonló címkék segítségével kategorizálhatja az erőforráscsoportokat felügyelet vagy költségvetés-elosztás érdekében.

## PARAMETERS

### -ApiVersion
Az erőforrásszolgáltató által támogatott API-verziót adja meg.
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
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.

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

### -Location
Az erőforráscsoport helyét határozza meg. Adja meg az Azure-adatközpont helyét, például Nyugat-Egyesült Államok vagy Délkelet-Ázsia. Az erőforráscsoportokat bármilyen helyen el lehet helyezése. Az erőforráscsoportnak nem kell az Azure-előfizetésével azonos helyen lennie, és nem is kell ugyanazon a helyen lennie, mint az erőforrásainak.
Ha meg szeretné állapítani, hogy melyik hely támogatja az egyes erőforrástípusokat, használja a Get-AzResourceProvider Parancsmagot *a ProviderNamespace* paraméterrel.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Az erőforráscsoport nevét adja meg. Az erőforrás nevének egyedinek kell lennie az előfizetésben. Ha már létezik ilyen nevű erőforráscsoport, a parancs megerősítést kér, mielőtt lecseréli a meglévő erőforráscsoportot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.

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

### -Tag
Kulcsérték-párok kivonattábla formájában. Például: @{key0="érték0";key1=$null;key2="érték2"} Címke hozzáadásához vagy cseréjéhez le kell cserélnie az erőforráscsoport címkéinek gyűjteményét.
Miután címkéket hozzárendelt az erőforrásokhoz  és a csoportokhoz, a Get-AzResource és a Get-AzResourceGroup címke paraméterével kereshet erőforrásokat és csoportokat címkenév, illetve név és érték szerint. Címkékkel kategorizálhatja az erőforrásokat, például részlegek vagy költségközpontok szerint, illetve nyomon követheti az erőforrásokkal kapcsolatos jegyzeteket vagy megjegyzéseket.
Az előre definiált címkéket a Get-AzTag használhatja.

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

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

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
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.Collections.Hashtable

## KIMENETEK

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzResourceProvider](./Get-AzResourceProvider.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResource](./New-AzResource.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)
