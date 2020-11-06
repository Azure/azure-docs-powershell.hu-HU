---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: 694ac928d78cf64f500730c57e394a8e3a425456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504903"
---
# Get-AzureRmMlWebServiceKeys

## Áttekintés
Lekéri a webszolgáltatás kulcsait.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Az Azure ML webszolgáltatás elérési kulcsait a neve és az erőforráscsoport adja meg.
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### A megadott webszolgáltatás-példány elérési kesy beszerzése
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
Az Azure Machine learning webszolgáltatás futásidejű API-k elérési kulcsait kapja meg.

## Példák

### --------------------------Példa 1 – az erőforráscsoport által megadott webszolgáltatás kulcsai és a név--------------------------
@ {bekezdés = PS C: \\ \> }





```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### --------------------------Example 2 – webszolgáltatási példány kulcsának beszerzése--------------------------
@ {bekezdés = PS C: \\ \> }





```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

a $mlService a Microsoft. Azure. Management. MachineLearning. webszolgáltatás. models. webszolgáltatás parancsot adja meg.

## PARAMÉTEREK

### -MlWebService
Annak a webszolgáltatásnak a neve, amelyhez a hozzáférési kulcsokat lekérdezi.

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Get the access kesy for the given web service instance.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
Annak a webszolgáltatásnak a neve, amelyhez a hozzáférési kulcsokat lekérdezi.

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
A webszolgáltatás erőforráscsoport.

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### WebService
A ' MlWebService ' paraméter a "webszolgáltatás" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### Nincs

## MEGJEGYZI
Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml

## KAPCSOLÓDÓ HIVATKOZÁSOK

