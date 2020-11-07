---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
ms.openlocfilehash: fe304408ee236312c2e6c71324d6a2a34157ff58
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835302"
---
# Get-AzMlWebService

## Áttekintés
Lekérdezi egy vagy több webes szolgáltatás összefoglaló adatait.

## SZINTAXISA

```
Get-AzMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A webszolgáltatás Defintion kapcsolatos adatok beolvasása
Az átadott paramenters függően a parancsmag egy adott webszolgáltatás Defintion ad eredményül, amely az aktuális előfizetésben lévő adott erőforráscsoport webszolgáltatásainak defintions, illetve az aktuális előfizetésben szereplő webes szolgáltatások defintions gyűjteménye.

## Példák

### Példa 1: adott webszolgáltatás részleteinek beolvasása
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### 2. példa: az összes webszolgáltatás-erőforrás beolvasása a jelenlegi előfizetésben
```
Get-AzMlWebService
```

### 3. példa: az aktuális előfizetés és a megadott erőforráscsoport összes webes szolgáltatásának beszerzése
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup"
```

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -Region (régió)
A Regio neve

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás

## MEGJEGYZI
Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml

## KAPCSOLÓDÓ HIVATKOZÁSOK
