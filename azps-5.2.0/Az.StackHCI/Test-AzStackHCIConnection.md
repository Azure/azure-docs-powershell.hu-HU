---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 1183a2aa6bf452d77ebe3975024067244075e5fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349925"
---
# Test-AzStackHCIConnection

## SYNOPSIS
Test-AzStackHCIConnection helyszíni csoportosított csomópontok és az Azure Stack HCI által megkövetelt Azure-szolgáltatások csatlakozását ellenőrzi.

## SZINTAXIS

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## LEÍRÁS
Test-AzStackHCIConnection helyszíni csoportosított csomópontok és az Azure Stack HCI által megkövetelt Azure-szolgáltatások csatlakozását ellenőrzi.

## PÉLDÁK

### 1. PÉLDA
```
Invoking on one of the cluster node. Success case.
```

C:\PS \> Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Succeedd

### 2. PÉLDA
```
Invoking on one of the cluster node. Failed case.
```

C:\PS \> Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Failed FailedNodes: Node1inClus2, Node2inClus3

## PARAMETERS

### -ComputerName
Az Azure-ba regisztrált, a környezetben található fürtben található egyik fürtcsomópontot adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hitelesítő adatok
A Számítógépnév hitelesítő adatait adja meg.
Az alapértelmezett érték az a felhasználó, aki végrehajtja a parancsmagot.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnvironmentName
Az Azure-környezetet határozza meg.
Az alapértelmezett érték az AzureCloud.
Érvényes értékek: AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### -Régió
Azt a régiót adja meg, amelyhez csatlakozni szeretne.
Nem használjuk, hacsak nem Canary régió.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

## KIMENETEK

### PSCustomObject. A PSCustomObject tulajdonságot követő tulajdonságokat adja eredményül.
### Teszt: Az elvégzett teszt neve.
### EndpointTested: Endpoint used in the test.
### IsRequired: True vagy False
### Eredmény: Sikeres vagy Sikertelen
### FailedNodes: Azon csomópontok listája, amelyeken a teszt sikertelen volt.
## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
