---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: e5864271e96add95624f857357defdea3039c7a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327987"
---
# Start-AzRecoveryServicesAsrPlannedFailoverJob

## SYNOPSIS
Tervezett feladatátvételi műveletet kezd.

## SZINTAXIS

### ByRPIObject (alapértelmezett)
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByRPObject
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## LEÍRÁS
A **Start-AzRecoveryServicesAsrPlannedFailoverService parancsmag** elindít egy tervezett feladatátvételt az Azure-webhely-helyreállítási replikációval védett elemhez vagy helyreállítási tervhez.
A feladat sikeres voltának ellenőrzéséhez használja a Get-AzRecoveryServicesAsrJob parancsmagot.

## PÉLDÁK

### 1. példa
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

Elindítja a tervezett feladatátvételt a megadott ASR helyreállítási tervhez, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.

## PARAMETERS

### -CreateVmIfNotFound
Hozza létre a virtuális gépet, ha nem található, miközben nem áll vissza az elsődleges régióba (alternatív hely-helyreállításban használva).) A paraméter elfogadható értékei a következőek:

- igen
- nem

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataEncryptionPrimaryCertFile
Az elsődleges tanúsítványfájlt adja meg.

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

### -DataEncryptionSecondaryCertFile
A másodlagos tanúsítványfájlt adja meg.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Irány
A feladatátvétel irányát határozza meg.
A paraméter elfogadható értékei a következőek:

- PrimaryToRecovery
- RecoveryToPrimary

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - Optimalizálás
Meghatározza, hogy mire optimalizálható.
Ez a paraméter akkor érvényes, ha egy Azure-webhelyről egy helyszíni webhelyre történik feladatátvétel, amely jelentős adatszinkronizálást igényel.
Érvényes értékek:

- ForDowntime
- ForSynchronization

Ha **a ForDowntime** meg van adva, az azt jelenti, hogy a rendszer a feladatátvétel előtt szinkronizálja az adatokat, hogy minimalizálja a leállást.
A szinkronizálás a virtuális gép leállítása nélkül történik.
A szinkronizálás befejezése után a feladat fel van függesztve.
Folytassa a feladatot egy további szinkronizálási művelettel, amely leállíthatja a virtuális gépet.

Ha meg van adva a **ForSynchronization** tulajdonság, az azt jelenti, hogy az adatok szinkronizálása csak feladatátvételkor történik meg, így az adatszinkronizálás kis méretűre van adva.
Ha ez a beállítás engedélyezve van, a virtuális gép azonnal leáll.
A szinkronizálás a leállítás után elindul a feladatátvételi művelet befejezéséhez.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPlan
Azt az ASR helyreállítási tervobjektumot adja meg, amely megfelel a helyreállítási terv meghiúsulási tervének.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ReplicationProtectedItem
A replikálás által védett elem asR-rel védett objektumának megadása, amely megfelel annak a replikációval védett elemnek, amelyről sikertelenül kell leírni a elemet.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ServicesProvider
Azonosítja azt az állomást, amelyen létre kell hoznia a virtuális gépet, miközben másik helyre kell átesni, az adott állomáson futó ASR-szolgáltatóhoz tartozó ASR-szolgáltató objektum megadásával.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases:

Required: False
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
A parancsmag futtatásakor a program megjeleníti, hogy mi történik. A parancsmag nem fut.

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

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem

## KIMENETEK

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
