---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: e6ac8c2a47f7a8d11eb4f82d46be2047fd5ff47d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835289"
---
# New-AzMlWebService

## Áttekintés
Új webszolgáltatás létrehozása.

## SZINTAXISA

### CreateFromFile
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateFromInstance
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
Azure Machine learning-webszolgáltatás létrehozása meglévő erőforráscsoport számára.
Ha egy azonos nevű webszolgáltatás megtalálható az erőforrás csoportban, a hívás frissítési műveletként működik, és a meglévő webszolgáltatás felülíródik.

## Példák

### Példa 1: új szolgáltatás létrehozása JSON-fájlon keresztüli definíció alapján
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

Létrehoz egy új Azure Machine learning webszolgáltatás "mywebservicename" nevű webszolgáltatását a "myresourcegroup" csoportban és a dél-közép-amerikai régióban, a hivatkozott JSON-fájlban szereplő definíciók alapján.

### 2. példa: új szolgáltatás létrehozása objektum-példányból
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

A Import-AzMlWebService parancsmag segítségével webszolgáltatási objektum példányát is testre szabhatja a közzététel előtt.

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

### -DefinitionFile
Specifes a webszolgáltatás JSON formátumú definícióját tartalmazó fájl elérési útját.
A webszolgáltatás definíciójának legújabb specifikációját a hencegés specifikáció csoportban találja https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .

```yaml
Type: System.String
Parameter Sets: CreateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Ne kérjen megerősítést.

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
A webszolgáltatás területe.
Írjon be egy Azure Data Center-régiót (például "Nyugat-amerikai" vagy "Délkelet-ázsiai").
A webszolgáltatásokat bármely olyan régióban elhelyezheti, amely támogatja az adott típusú erőforrásokat.
A webszolgáltatásnak nem kell ugyanazon a régión belül lennie az Azure-előfizetésben vagy ugyanabban a régióban, mint az erőforráscsoport.
Az erőforráscsoportok tartalmazhatnak olyan webszolgáltatásokat, amelyek különböző régiókban találhatók.
Ha meg szeretné állapítani, hogy mely régiók támogatják az egyes erőforrás-típusokat, használja a Get-AzResourceProvidert a ProviderNamespace paraméter parancsmaggal.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A webszolgáltatás neve.
A névnek egyedinek kell lennie az erőforrás csoportban.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewWebServiceDefinition
Az új webszolgáltatás definíciója, amely a szolgáltatást alkotó összes tulajdonságot tartalmazza.
Ez a paraméter kötelező, és a Microsoft. Azure. Management. MachineLearning. webszolgáltatás. models. webszolgáltatási osztály példányát jelöli.
A webszolgáltatás definíciójának legújabb specifikációját a hencegés specifikáció csoportban találja https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: CreateFromInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Az az erőforráscsoport, amelybe a webszolgáltatást helyezni szeretné.
Írjon be egy Azure Data Center-régiót (például "Nyugat-amerikai" vagy "Délkelet-ázsiai").
A webszolgáltatásokat bármely olyan régióban elhelyezheti, amely támogatja az adott típusú erőforrásokat.
A webszolgáltatásnak nem kell ugyanazon a régión belül lennie az Azure-előfizetésben vagy ugyanabban a régióban, mint az erőforráscsoport.
Az erőforráscsoportok tartalmazhatnak olyan webszolgáltatásokat, amelyek különböző régiókban találhatók.
Ha meg szeretné állapítani, hogy mely régiók támogatják az egyes erőforrás-típusokat, használja a Get-AzResourceProvidert a ProviderNamespace paraméter parancsmaggal.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás

## KIMENETEK

### Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás

## MEGJEGYZI
Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml

## KAPCSOLÓDÓ HIVATKOZÁSOK
