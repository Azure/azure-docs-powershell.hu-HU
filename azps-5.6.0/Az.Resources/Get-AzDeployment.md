---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: 92a0aac5043be520f6a7ed7afc2066e0532b79ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922674"
---
# Get-AzDeployment

## SYNOPSIS
Üzembe helyezés

## SZINTAXIS

### GetByDeploymentName (alapértelmezett)
```
Get-AzDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByDeploymentId
```
Get-AzDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzDeployment** parancsmag az aktuális előfizetési hatókörű telepítéseket kapja meg.
Adja meg *a Név* vagy *az Azonosító* paramétert az eredmények szűréséhez.
Alapértelmezés szerint a **Get-AzDeployment** az összes telepítést az aktuális előfizetési hatókörben kapja meg.

## PÉLDÁK

### 1. példa: Az összes telepítés lekérte az előfizetés hatókörét
```
PS C:\>Get-AzDeployment
```

Ez a parancs az összes telepítést az aktuális előfizetési hatókörben kapja meg.

### 2. példa: Telepítés lekérte név szerint
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

Ez a parancs a DeployRoles01 telepítést az aktuális előfizetési hatókörben kapja meg.
A **New-AzDeployment parancsmagok** használatával nevet rendelhet a telepítéshez, amikor létrehozza.
Ha nem rendel nevet, a parancsmagok az üzembe helyezés létrehozásához használt sablon alapján alapértelmezett nevet biztosítanak.

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

### -Id
A telepítés teljes erőforrás-azonosítója.
példa: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Az üzembe helyezés neve.

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
