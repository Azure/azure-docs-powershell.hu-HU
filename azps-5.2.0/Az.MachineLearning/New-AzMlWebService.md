---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 5988aed4ca0560daedc1470198e0b02975f18196
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331853"
---
# New-AzMlWebService

## SYNOPSIS
Létrehoz egy új webszolgáltatást.

## SZINTAXIS

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

## LEÍRÁS
Azure Machine Learning webszolgáltatást hoz létre egy meglévő erőforráscsoportban.
Ha az erőforráscsoportban létezik azonos nevű webszolgáltatás, a hívás frissítési műveletként működik, és a meglévő webszolgáltatás felülíródik.

## PÉLDÁK

### 1. példa: Új szolgáltatás létrehozása Json-fájlalapú definícióból
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

Létrehozza a "myresourcegroup" csoportban és az Egyesült Államok déli részén található "myresourcegroup" nevű új Azure Machine Learning webszolgáltatást a hivatkozott json-fájlban található definíció alapján.

### 2. példa: Új szolgáltatás létrehozása objektumpéldányból
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

A webszolgáltatás-objektumpéldányt az erőforrásként való közzététel előtt testre szabhatja a Import-AzMlWebService parancsmag használatával.

## PARAMETERS

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

### -DefinitionFile
A webszolgáltatás JSON formátumdefinícióját tartalmazó fájl elérési útját adja meg.
A webszolgáltatás-definíció legújabb specifikációját a swagger specifikáció alatt https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning találja.

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

### -Location
A webszolgáltatás régiója.
Adjon meg egy Azure-adatközpont régiót, például "Nyugat-Usa" vagy "Délkelet-Ázsia".
A webszolgáltatás bármely olyan régióban elhelyelhet, amely támogatja az adott típusú erőforrásokat.
A webszolgáltatásnak nem kell ugyanabban a régióban lennie, mint az Azure-előfizetésének, vagy ugyanabban a régióban, ahol az erőforráscsoportja található.
Az erőforráscsoportok különböző régiókból származó webes szolgáltatásokat tartalmazhatnak.
Ha meg szeretné állapítani, hogy mely régiók támogatják az egyes erőforrástípusokat, használja a Get-AzResourceProvider ProviderNamespace paraméter parancsmaggal.

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

### -Name
A webszolgáltatás neve.
A névnek egyedinek kell lennie az erőforráscsoportban.

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
Az új webszolgáltatás definíciója, amely a szolgáltatást tartalmazó összes tulajdonságot tartalmazza.
Ez a paraméter kötelező, és a Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService osztály egy példányát képviseli.
A webszolgáltatás-definíció legújabb specifikációját a swagger specifikáció alatt https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json találja.

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
Az az erőforráscsoport, amelyben el kell helyezze a webszolgáltatást.
Adjon meg egy Azure-adatközpont régiót, például "Nyugat-Usa" vagy "Délkelet-Ázsia".
A webszolgáltatás bármely olyan régióban elhelyelhet, amely támogatja az adott típusú erőforrásokat.
A webszolgáltatásnak nem kell ugyanabban a régióban lennie, mint az Azure-előfizetésének, vagy ugyanabban a régióban, ahol az erőforráscsoportja található.
Az erőforráscsoportok különböző régiókból származó webes szolgáltatásokat tartalmazhatnak.
Ha meg szeretné állapítani, hogy mely régiók támogatják az egyes erőforrástípusokat, használja a Get-AzResourceProvider ProviderNamespace paraméter parancsmaggal.

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

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

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
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService

## KIMENETEK

### Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService

## MEGJEGYZÉSEK
Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, gépi, gépi tanulás, azureml

## KAPCSOLÓDÓ HIVATKOZÁSOK
