---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 5fcd81dcfc69f020a4e17e0858abfca0edaba405
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929129"
---
# Get-AzAccessToken

## SYNOPSIS
Nyers hozzáférési jogkivonat beszerzése. A -ResourceUrl használata esetén győződjön meg arról, hogy az érték megfelel az aktuális Azure-környezetnek. Hivatkozhat a `(Get-AzContext).Environment` .

## SZINTAXIS

### KnownResourceTypeName (alapértelmezett)
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceUrl
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
Hozzáférési jogkivonat beszerzése

## PÉLDÁK

### 1. példa: Nyers hozzáférési jogkivonat beszerzése ARM végponthoz
```powershell
PS C:\> Get-AzAccessToken
```

Az aktuális fiók ResourceManager-végpontjának hozzáférési jogkivonatának beszerzése

### 2. példa: Nyers hozzáférési jogkivonat beszerzése az AAD Graph-végponthoz
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

Az aktuális fiók AAD Graph-végpontjának hozzáférési jogkivonatának beszerzése

### 3. példa: Nyers hozzáférési jogkivonat beszerzése az AAD Graph-végponthoz
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

Az aktuális fiók AAD Graph-végpontjának hozzáférési jogkivonatának beszerzése

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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

### -ResourceTypeName
Nem kötelező megadni a típus nevét, támogatott értékek: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse. Az alapértelmezett érték az Arm, ha nincs megadva.

```yaml
Type: System.String
Parameter Sets: KnownResourceTypeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceUrl
Annak az erőforrásnak az URL-címe, amelyhez jogkivonatot kér, például ' http://graph.windows.net/ '.

```yaml
Type: System.String
Parameter Sets: ResourceUrl
Aliases: Resource, ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId
Nem kötelező bérlőazonosító. Ha nincs megadva, használja az alapértelmezett környezet bérlőazonosítóját.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Nincs

## KIMENETEK

### System.String

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
