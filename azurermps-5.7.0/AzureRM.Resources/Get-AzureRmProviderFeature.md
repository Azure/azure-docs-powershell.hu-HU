---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
ms.openlocfilehash: d13eb98b01380fcb02392d1ac3f34c8d70c7f6dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679260"
---
# Get-AzureRmProviderFeature

## Áttekintés
Információkat kap az Azure Provider funkcióiról.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ListAvailableParameterSet (alapértelmezett)
```
Get-AzureRmProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetFeature
```
Get-AzureRmProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmProviderFeature** parancsmag a szolgáltatás nevét, a szolgáltató nevét és a regisztráció állapotát az Azure szolgáltató szolgáltatásaihoz kapja.

## Példák

### Példa 1: az összes elérhető funkció beszerzése
```
PS C:\>Get-AzureRmProviderFeature -ListAvailable
```

Ez a parancs elérhetővé válik az összes elérhető funkció.

### 2. példa: információk kérése egy adott funkcióról
```
PS C:\>Get-AzureRmProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

Ez a parancs információkat kap a megadott szolgáltató AllowPreReleaseRegions nevű funkcióról.

## PARAMÉTEREK

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

### -ÖsszetevőNeve
A beolvasott funkció nevét adja meg.

```yaml
Type: String
Parameter Sets: GetFeature
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ListAvailable
Azt jelzi, hogy ez a parancsmag minden szolgáltatást elérhető.

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailableParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProviderNamespace
Azt a névteret adja meg, amelynek a parancsmagja a szolgáltató funkcióit kapja.

```yaml
Type: String
Parameter Sets: ListAvailableParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetFeature
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. ResourceManager. Parancsmags. SdkModels. PSProviderFeature]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Register-AzureRmProviderFeature](./Register-AzureRmProviderFeature.md)


