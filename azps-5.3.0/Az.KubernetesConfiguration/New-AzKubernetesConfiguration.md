---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 70ff3c636f6c88ac89e53a5c2b1acb209aad274a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469502"
---
# New-AzKubernetesConfiguration

## SYNOPSIS
Hozzon létre egy új Kubanetes-forrásvezérlő-konfigurációt.

## SZINTAXIS

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## LEÍRÁS
Hozzon létre egy új Kubanetes-forrásvezérlő-konfigurációt.

## PÉLDÁK

### 1. példa: Konfigurációs konfiguráció létrehozása a kubernetes fürthöz
```powershell
PS C:\> New-AzKubernetesConfiguration -Name conf-test01 -ClusterName connaks-d983yc -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

Ezzel a paranccsal konkguguációt hoz létre a rendszer a parancssori hálózatok fürtjéhez.

## PARAMETERS

### -ClusterName
A kubernetes fürt neve.

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

### -ClusterScoped
Ha a beállításnak megfelelő tartományt ad meg, a konfiguráció hatókörét fürtre állíthatja (az alapértelmezett névTér.

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

### -ClusterType
A Kubarenetes-fürterőforrás neve – vagy managedClusters (AKS-fürtök esetén) vagy connectedClusters (OnPrem K8S-fürtök esetén).

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

### -EnableHelmOperator
Option to enable Fogék operátor for this git configuration.

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

### -MerteOperatorChartValues
Values override for the operator Chart.

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

### -ÉkOperatorChartVersion
A Chart operátor verziója.

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

### -Name
A forrásvezérlő-konfiguráció neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatorInstanceName
Az operátor példányneve – az adott konfiguráció azonosítása.

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

### -OperatorNamespace
Az a névtér, amelyre az operátor telepítve van.
Legfeljebb 253 kisbetűs alfanumerikus karakter, kötőjel és pont.

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

### -OperatorParameters
Az Operátor példány bármely paramétere karakterlánc formátumban.

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

### -RepositoryUrl
A SourceControl adattár URL-címe.

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

### -ResourceGroupName
Az erőforráscsoport neve.

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

### -SubscriptionId
Az Azure-előfizetés azonosítója.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

## KIMENETEK

### Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration

## MEGJEGYZÉSEK

ALIASOK

## KAPCSOLÓDÓ HIVATKOZÁSOK

