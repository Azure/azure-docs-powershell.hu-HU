---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
ms.openlocfilehash: 14fbb8631a15321df9ae6834456649d00caae897
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504911"
---
# Get-AzureRmMlWebService

## Áttekintés
Lekérdezi egy vagy több webes szolgáltatás összefoglaló adatait.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A webszolgáltatás Defintion kapcsolatos adatok beolvasása
Az átadott paramenters függően a parancsmag egy adott webszolgáltatás Defintion ad eredményül, amely az aktuális előfizetésben lévő adott erőforráscsoport webszolgáltatásainak defintions, illetve az aktuális előfizetésben szereplő webes szolgáltatások defintions gyűjteménye.

## Példák

### --------------------------Példa 1: adott webszolgáltatás részleteinek beszerzése--------------------------
@ {bekezdés = PS C: \\ \> }





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### --------------------------Példa 2: az összes webszolgáltatás-erőforrás beolvasása a jelenlegi előfizetésben--------------------------
@ {bekezdés = PS C: \\ \> }





```
Get-AzureRmMlWebService
```

### --------------------------Example 3: az összes webes szolgáltatás beszerzése az aktuális előfizetésben és az adott erőforráscsoport--------------------------
@ {bekezdés = PS C: \\ \> }





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup"
```

## PARAMÉTEREK

### -Name (név)
Annak a webszolgáltatásnak a neve, amelybe a részleteket lekérdezi.

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

### -ResourceGroupName
Az az erőforráscsoport, amelyből a webszolgáltatás adatait beolvassák.

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

### -Region (régió)
A régió neve

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Nincs

## MEGJEGYZI
Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml

## KAPCSOLÓDÓ HIVATKOZÁSOK

