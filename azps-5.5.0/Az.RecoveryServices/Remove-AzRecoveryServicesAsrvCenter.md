---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 69146f9ff6cc3897d304c6ce816ae35cb5113181
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156498"
---
# Remove-AzRecoveryServicesAsrvCenter

## SYNOPSIS
Eltávolítja a vCenter-kiszolgálót az ASR-anyagból, és leállítja a virtuális gépek felderítését a vCenter-kiszolgálóról.

## SZINTAXIS

### Alapértelmezett (alapértelmezett)
```
Remove-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByResourceId
```
Remove-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByName
```
Remove-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Remove-AzRecoveryServicesAsrvCenter** parancsmag eltávolítja a vCenter-kiszolgálót az ASR-anyagból, és leállítja a virtuális gépek felderítését a vCenter-kiszolgálóról.

## PÉLDÁK

### 1. példa
```powershell
PS C:\> Remove-AzRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

Eltávolítja a vCenter-kiszolgálót az ASR-anyagból.

### 2. példa

Eltávolítja a vCenter-kiszolgálót az ASR-anyagból, és leállítja a virtuális gépek felderítését a vCenter-kiszolgálóról. (automatikusan generált)

```powershell <!-- Aladdin Generated Example --> 
Remove-AzRecoveryServicesAsrvCenter -Fabric $Fabric -Name 'V2VM'
```

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

### -Fabric
A Configuration Servert képviselő ASR-anyagobjektum.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InputObject
Az eltávolítható vCenter-kiszolgálót képviselő ASR vCenter-objektum.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
A vCenter-kiszolgáló neve.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
A vCenter eltávolítható erőforrásazonosítóját adja meg.

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System.String

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric

## KIMENETEK

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
