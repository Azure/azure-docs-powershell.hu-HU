---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: 0523041357becb38475bb496c94ba1fd48c5acaf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465944"
---
# Set-AzResourceGroup

## SYNOPSIS
Módosít egy erőforráscsoportot.

## SZINTAXIS

### SetByResourceGroupName (alapértelmezett)
```
Set-AzResourceGroup -Name <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceGroupId
```
Set-AzResourceGroup [-Tag] <Hashtable> -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzResourceGroup** parancsmag módosítja egy erőforráscsoport tulajdonságait.
Ezzel a parancsmagtal hozzáadhatja, módosíthatja vagy törölheti az erőforráscsoportokra alkalmazott Azure-címkéket.
Adja meg *a Name paramétert* az erőforráscsoport azonosításához, a *Címke* paramétert pedig a címkék módosításához.
Ezzel a parancsmagtal nem módosíthatja egy erőforráscsoport nevét.

## PÉLDÁK

### 1. példa: Címke alkalmazása erőforráscsoportra
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

Ez a parancs egy it-értékkel megadott Részleg címkét alkalmaz egy olyan erőforráscsoportra, amely nem rendelkezik meglévő címkékkel.

### 2. példa: Címkék hozzáadása erőforráscsoporthoz
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

Ebben a példában egy "Jóváhagyva" értékkel és egy 2016-os FY2016-os címkével egy meglévő címkéket kezelő erőforráscsoporthoz ad hozzá egy állapotcímkét. Mivel a megadott címkék lecserélik a meglévő címkéket, a meglévő címkéket fel kell vesznie az új címkegyűjteménybe, különben elvesznek.
Az első parancs a ContosoRG erőforráscsoportot kapja meg, és a pont módszerrel be tudja szerezni a Címkék tulajdonság értékét. A parancs a címkéket a $Tags tárolja.
A második parancs megkapja a címkéket a $Tags változóban.
A harmadik parancs a += hozzárendelési operátorral adja hozzá az állapot- és 2016-os címkéket a címketömbhöz a $Tags változóban.
A negyedik parancs *a* **Set-AzResourceGroup** Címke paraméterével alkalmazza a $Tags címkéit a ContosoRG erőforráscsoportra.
Az ötödik parancs a ContosoRG erőforráscsoportra alkalmazott összes címkét begyakorlja. A kimenet azt mutatja, hogy az erőforráscsoport részlegcímkével és a két új címkével (Állapot és Y2015) rendelkezik.

### 3. példa: Erőforráscsoport összes címkéének törlése
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

Ez a parancs a *Címke* paramétert adja meg egy üres kivonattábla-értékkel, amely törli az összes címkét a ContosoRG erőforráscsoportból.

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

### -Id
A módosítani szükséges erőforráscsoport azonosítója.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
A módosítani szükséges erőforráscsoport nevét adja meg.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: Named
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
Kulcsérték-párok kivonattábla formájában. Például: @{key0="érték0";key1=$null;key2="érték2"} A címke egy névérték-pár, amely létrehozható és alkalmazható erőforrásokra és erőforráscsoportokra. Miután címkéket rendel erőforrásokhoz és csoportokhoz, a Get-AzResource és a Get-AzResourceGroup címke paraméterével kereshet erőforrásokat és csoportokat címkenév, név és érték alapján.  Címkékkel kategorizálhatja az erőforrásokat, például részlegek vagy költségközpontok szerint, illetve nyomon követheti az erőforrásokkal kapcsolatos jegyzeteket vagy megjegyzéseket.
Címke hozzáadásához vagy cseréjéhez le kell cserélnie az erőforráscsoport címkéinek gyűjteményét. Címke törléséhez írjon be egy olyan kivonattáblát, amely az erőforráscsoportra jelenleg alkalmazott összes címkét tartalmazza a **Get-AzResourceGroup** csoportból , kivéve a törölni kívánt címkét. Ha egy erőforráscsoport összes címkéét törölni szeretné, adjon meg egy üres kivonattáblát: `@{}` .

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

[Get-AzResource](./Get-AzResource.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)
