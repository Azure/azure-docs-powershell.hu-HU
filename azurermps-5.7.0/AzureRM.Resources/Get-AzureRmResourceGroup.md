---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
ms.openlocfilehash: f3924115d68d7e844503e076a214c95bf3d2239d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502487"
---
# Get-AzureRmResourceGroup

## Áttekintés
Erőforrás-csoportok beolvasása

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### GetByResourceGroupName (alapértelmezett)
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupId
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmResourceGroup** parancsmag Azure-erőforráscsoportokat kap az aktuális előfizetésben.
Az összes erőforráscsoport beolvasható, vagy megadhat egy erőforráscsoportot név vagy egyéb tulajdonság alapján.
Alapértelmezés szerint ez a parancsmag a jelenlegi előfizetésben az összes erőforráscsoport számára elérhető lesz.

Az Azure-erőforrásokról és az Azure-erőforráscsoportok használatáról az New-AzureRmResourceGroup parancsmag című témakörben olvashat bővebben.

## Példák

### Példa 1: erőforráscsoport beszerzése név alapján
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

Ez a parancs a EngineerBlog nevű előfizetésben az Azure Resource Group nevet kapja.

### 2. példa: erőforráscsoport összes címkéjának beolvasása
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

Ez a parancs beolvassa a ContosoRG nevű erőforráscsoportot, és megjeleníti a csoporthoz társított címkéket.

### 3. példa: erőforráscsoportok megjelenítése hely szerint
```
PS C:\> Get-AzureRmResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### Példa 4: egy adott helyen található összes erőforráscsoport nevének megjelenítése
```
PS C:\> Get-AzureRmResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### Példa 5: azoknak az erőforrás-csoportoknak a megjelenítése, amelyek nevei a webkiszolgálóval kezdődnek
```
PS C:\> Get-AzureRmResourceGroup | Where ResourceGroupName -like WebServer*
```

## PARAMÉTEREK

### -ApiVersion
Az erőforrás-szolgáltató által támogatott API-verziót adja meg.
Az alapértelmezett verziótól eltérő verziót is megadhat.

```yaml
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Azonosító
A beolvasott erőforráscsoport AZONOSÍTÓját adja meg.
A helyettesítő karakterek nem engedélyezettek.

```yaml
Type: String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hely
A beolvasott erőforráscsoport helyét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A beolvasott erőforráscsoport nevét adja meg.
A helyettesítő karakterek nem engedélyezettek.

```yaml
Type: String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Karakterlánc
A parancsmagot tulajdonság neve szerint, de nem érték szerint is beírhatja.

## KIMENETEK

### Microsoft. Azure. Command. ResourceManagement. PSResourceGroup
Ez a parancsmag erőforrás-csoportokat ad eredményül.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[Remove-AzureRmResourceGroup](./Remove-AzureRmResourceGroup.md)

[Set-AzureRmResourceGroup](./Set-AzureRmResourceGroup.md)


