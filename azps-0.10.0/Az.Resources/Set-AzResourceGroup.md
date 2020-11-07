---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: d645f430c21a1e9675a0f356cffacbad6a7b5740
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843182"
---
# Set-AzResourceGroup

## Áttekintés
Egy erőforráscsoport módosítása

## SZINTAXISA

### SetByResourceGroupName (alapértelmezett)
```
Set-AzResourceGroup [-Name] <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceGroupId
```
Set-AzResourceGroup [-Tag] <Hashtable> [-Id] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **set-AzResourceGroup** parancsmag egy erőforráscsoport tulajdonságait módosítja.
Ezzel a parancsmaggal megadhatja, módosíthatja vagy törölheti az erőforrás-csoportokra alkalmazott Azure-címkéket.
Adja meg a *Name (név* ) paramétert az erőforráscsoport meghatározásához, illetve a *címke* paramétert a címkék módosításához.
Ez a parancsmag nem használható az erőforráscsoport nevének módosítására.

## Példák

### 1. példa: címke alkalmazása erőforráscsoporthoz
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

Ez a parancs egy olyan részleg címkét alkalmaz, amelynek az értéke egy olyan erőforráscsoport, amely nem tartalmaz meglévő címkéket.

### 2. példa: Címkék hozzáadása erőforráscsoporthoz
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

Ebben a példában egy olyan állapotkódot ad meg, amely egy jóváhagyott értékkel rendelkezik, és egy FY2016 címkét tartalmaz egy meglévő címkéket tartalmazó erőforráscsoporthoz. Mivel a megadott címkék felülírják a meglévő címkéket, a meglévő címkéket meg kell jeleníteni az új címkét tartalmazó gyűjteményben, vagy elveszíti őket.
Az első parancs megkapja a ContosoRG erőforráscsoport értékét, és a dot metódus segítségével Kinyeri a címkék tulajdonság értékét. A parancs a címkéket a $Tags változóban tárolja.
A második parancs a címkéket a $Tags változóban kapja meg.
A harmadik parancs a + = hozzárendelés-operátor segítségével felveszi az állapotot és a FY2016 a címkék sorába a $Tags változóban.
A negyedik parancs a **set-AzResourceGroup** *címke* paraméterével alkalmazza a címkéket a $Tags változóban a ContosoRG-erőforrás csoportba.
Az ötödik parancs beilleszti az összes, a ContosoRG-erőforráscsoporthoz alkalmazott címkét. A kimenet azt mutatja, hogy az erőforráscsoport rendelkezik a részleg címkével, valamint a két új címkével, az állapottal és a FY2015.

### 3. példa: erőforráscsoport összes címkéjének törlése
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

Ez a parancs azt a *címkét* megadó paramétert adja meg, amely egy üres ujjlenyomat-tábla értékkel rendelkezik az összes címke törléséhez a ContosoRG-erőforráscsoport közül.

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

### -Azonosító
A módosítani kívánt erőforráscsoport AZONOSÍTÓját adja meg.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A módosítani kívánt erőforráscsoport nevét adja meg.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
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
A kulcs-érték párok a hash-táblázatok formájában. Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"} A címke egy olyan név-érték páros, amelyet létrehozhat, és alkalmazhat az erőforrásokra és az erőforrás-csoportokra. Miután címkéket rendelt az erőforrásokhoz és csoportokhoz, a *címke* paramétert használhatja Get-AzResource és a Get-AzResourceGroup segítségével az erőforrások és a csoportok címkét adhat a név vagy a név és az érték megadásával. Címkéket használhat az erőforrások (például részleg vagy költséghely) kategorizálásához, illetve az erőforrásokkal kapcsolatos megjegyzések és megjegyzések nyomon követéséhez.
Címke hozzáadásához vagy módosításához az erőforráscsoport címkéjének gyűjteményét kell lecserélnie. Ha törölni szeretne egy címkét, írja be az összes olyan címkét, amely az erőforráscsoport által használt összes címkét, a **Get-AzResourceGroup** , kivéve a törölni kívánt címkét tartalmazza. Ha az összes címkét törölni szeretné egy erőforráscsoport esetében, adjon meg egy üres kivonatoló táblát: `@{}` .

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Command. Resources. models. PSResourceGroup

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzResource](./Get-AzResource.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[Új – AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)
