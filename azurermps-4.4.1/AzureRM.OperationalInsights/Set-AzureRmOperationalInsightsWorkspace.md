---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: e24597d25fffdc1b516c5a18cf011f7222d288c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493393"
---
# Set-AzureRmOperationalInsightsWorkspace

## Áttekintés
Munkaterületet frissít.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByName (alapértelmezett)
```
Set-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tags] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByObject
```
Set-AzureRmOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tags] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **set-AzureRmOperationalInsightsWorkspace** parancsmag a munkaterület konfigurációját módosítja.

## Példák

### Példa 1: munkaterület módosítása név szerint
```
PS C:\>Set-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

Ez a parancs módosítja a MyWorkspace nevű munkaterület SKU-és címkéket a ContosoResourceGroup nevű erőforráscsoport nevében.

### 2. példa: munkaterület frissítése a csővezeték használatával
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzureRmOperationalInsightsWorkspace -Sku "Premium"
```

Ez a parancs a Get-AzureRmOperationalInsightsWorkspace parancsmagot használja a MyWorkSpace nevű munkaterület beolvasásához, majd átadja azt a **set-AzureRmOperationalInsightsWorkspace** parancsmagnak a pipeline operátorral az SKU prémium értékre való beállításához.

## PARAMÉTEREK

### -Name (név)
A munkaterület nevét adja meg.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Az Azure Resource Group nevet adja meg.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
A munkaterület szolgáltatási rétegét adja meg.
Az érvényes értékek a következők: 

- ingyenes
- Standard
- prémium verzió

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: free, standard, premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Címkék
A munkaterület erőforrás-címkéit adja meg.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Munkaterület
A frissítendő munkaterületet adja meg.

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -RetentionInDays
Munkaterület-adatmegőrzés napokban. a 730 napok az összes többi SKU számára megengedett maximális érték.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### PSWorkspace
A "Munkaterület" paraméter elfogadja a "PSWorkspace" típusú értéket a csővezetékről

## KIMENETEK

### Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure hadműveleti parancsmagok](./AzureRM.OperationalInsights.md)

[Get-AzureRmOperationalInsightsWorkspace](./Get-AzureRmOperationalInsightsWorkspace.md)


