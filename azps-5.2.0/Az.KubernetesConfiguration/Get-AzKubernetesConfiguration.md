---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: 3fd93e42b8f38659f61fcbeb0f49040409f635a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367763"
---
# Get-AzKubernetesConfiguration

## SYNOPSIS
A forrásvezérlő konfigurációjának részletei.

## SZINTAXIS

### Lista (alapértelmezett)
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Bej.le
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## LEÍRÁS
A forrásvezérlő konfigurációjának részletei.

## PÉLDÁK

### 1. példa: A rendszer az összes beállítását beveszi a rendszercsoportban.
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

Ez a parancs a parancssori fürt összes konfigurációját beveszi.

### 2. példa: A rendszer név szerint konfigurálja a rendszer a többhálózatos fürtöt
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name conf-t02

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

Ez a parancs név szerint konfigurálja a kubernetes fürtöt.

### 3. példa: A rendszer objektum szerint csoportosítva konfigurálja a rendszer a többhálózati hálózatokat.
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name conf-test02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

Ez a parancs objektum szerint csoportosítva kapja meg a kubernetes fürt konfigurációját.

### 4. példa: A rendszer a többhálózati fürt konfigurációját prognózis szerint konfigurálja
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/conf-test01'} | Get-AzKubernetesConfiguration

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

Ez a parancs a parancssori fürt konfigurációját kapja meg folyamat szerint.

## PARAMETERS

### -ClusterName
A kubernetes fürt neve.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClusterRp
A Kubanetes-fürt RP- vagy Microsoft.ContainerService (AKS-fürtök esetén) vagy Microsoft.Kubernetes (OnPrem K8S-fürtök esetén).

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClusterType
A Kubarenetes-fürterőforrás neve – vagy managedClusters (AKS-fürtök esetén) vagy connectedClusters (OnPrem K8S-fürtök esetén).

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
A forrásvezérlő-konfiguráció neve.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Az Azure-előfizetés azonosítója.
Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-0000000000000000000)

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity

## KIMENETEK

### Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration

## MEGJEGYZÉSEK

ALIASOK

COMPLEX PARAMETER PROPERTIES

Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat. A kivonattáblákról további információt a Get-Help about_Hash_Tables.


INPUTOBJECT: <IKubernetesConfigurationIdentity> Identity Parameter
  - `[ClusterName <String>]`: Anetes fürt neve.
  - `[ClusterResourceName <String>]`: A Kubernetes-fürterőforrás neve – vagy managedClusters (AKS-fürtök esetén) vagy connectedClusters (OnPrem K8S-fürtök esetén).
  - `[ClusterRp <String>]`: A Kubanetes fürt RP - vagy Microsoft.ContainerService (AKS-fürtök esetén) vagy Microsoft.Kubernetes (OnPrem K8S-fürtök esetén).
  - `[Id <String>]`: Erőforrás-identitás elérési útja
  - `[ResourceGroupName <String>]`: Az erőforráscsoport neve.
  - `[SourceControlConfigurationName <String>]`: A forrásvezérlő-konfiguráció neve.
  - `[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója. Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-0000000000000000000)

## KAPCSOLÓDÓ HIVATKOZÁSOK

