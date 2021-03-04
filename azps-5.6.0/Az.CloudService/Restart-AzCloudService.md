---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/restart-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudService.md
ms.openlocfilehash: e61eea1d00468937a46f90fdd6a995f5f53ff468
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920834"
---
# Restart-AzCloudService

## SYNOPSIS
Egy vagy több szerepkörpéldány újraindítása egy felhőszolgáltatásban.

## SZINTAXIS

### RestartExpanded (alapértelmezett)
```
Restart-AzCloudService -Name <String> -ResourceGroupName <String> -RoleInstance <String[]>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### RestartViaIdentityExpanded
```
Restart-AzCloudService -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## LEÍRÁS
Egy vagy több szerepkörpéldány újraindítása egy felhőszolgáltatásban.

## PÉLDÁK

### 1. példa: A felhőszolgáltatás szerepkörpéldányainak újraindítása
```powershell
PS C:\> $roleInstances = @("ContosoFrontEnd_IN_0", "ContosoBackEnd_IN_1")
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance $roleInstances
```

Ez a parancs 2 szerepkörpéldányt ContosoFrontEnd_IN_0 és ContosoBackEnd_IN_1 ContosoCS nevű felhőszolgáltatást, amely a ContosOrg nevű erőforráscsoporthoz tartozik.

### 2. példa: A felhőszolgáltatás összes szerepkörének újraindítása
```powershell
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "*"
```

Ez a parancs újraindítja a ContosoCS nevű felhőszolgáltatás összes olyan szerepkörpéldányát, amely a ContosOrg nevű erőforráscsoporthoz tartozik.

## PARAMETERS

### -AsJob
A parancs futtatása feladatként

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
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RestartViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
A felhőszolgáltatás neve.

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
A parancs futtatása aszinkron módon

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

### -PassThru
Igaz értéket ad vissza, ha a parancs sikeres

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

### -ResourceGroupName
Az erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleInstance
A felhőbeli szolgáltatási szerepkör példánynevének listája.
A "*" érték a felhőszolgáltatás összes szerepkörpéldányát alá fogja írni.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.
Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.

```yaml
Type: System.String
Parameter Sets: RestartExpanded
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

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity

## KIMENETEK

### System.Boolean

## MEGJEGYZÉSEK

ALIASOK

COMPLEX PARAMETER PROPERTIES

Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat. A kivonattáblákról további információt a Get-Help about_Hash_Tables.


INPUTOBJECT: <ICloudServiceIdentity> Identity Parameter
  - `[CloudServiceName <String>]`: 
  - `[Id <String>]`: Erőforrás-identitás elérési útja
  - `[ResourceGroupName <String>]`: 
  - `[RoleInstanceName <String>]`: A szerepkörpéldány neve.
  - `[RoleName <String>]`: A szerepkör neve.
  - `[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést. Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.
  - `[UpdateDomain <Int32?>]`: A frissítő tartományt azonosító egész értéket ad meg. A frissítési tartományokat nulla alapú index azonosítja: az első frissítési tartomány azonosítója 0, a második 1 és így tovább.

## KAPCSOLÓDÓ HIVATKOZÁSOK

