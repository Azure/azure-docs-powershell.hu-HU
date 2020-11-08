---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AC73119B-BB76-425B-AA44-44502028ECC4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a74a02f219b5bb64957ab919168cb79ccf681869
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015806"
---
# Start-AzureSiteRecoveryUnplannedFailoverJob

## Áttekintés
Elindítja a nem tervezett feladatátvételt egy webhely-helyreállítási jogalanynál vagy helyreállítási tervben.

## SZINTAXISA

### ByRPId (alapértelmezett)
```
Start-AzureSiteRecoveryUnplannedFailoverJob -RPId <String> -Direction <String> [-PrimaryAction <Boolean>]
 [-PerformSourceSideActions] [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByPEId
```
Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-PerformSourceSiteOperations <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRPObject
```
Start-AzureSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PrimaryAction <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByPEObject
```
Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSiteOperations <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Start-AzureSiteRecoveryUnplannedFailoverJob** parancsmag az Azure webhely-helyreállítási védelem vagy helyreállítási terv nem tervezett feladatátvételét indítja el.
Ellenőrizheti, hogy a feladat sikeres volt-e a **Get-AzureSiteRecoveryJob** parancsmag használatával.

## Példák

### Példa 1: nem tervezett feladatátvételi feladat indítása
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer 
PS C:\> Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntity $ProtectionEntity -Direction "PrimaryToRecovery"
ID               : c38eecdc-731c-405b-a61c-08db99aae2fe
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : {}
Name             : 
Tasks            : {}
Errors           : {}
```

Az első parancs a **Get-AzureSiteRecoveryProtectionContainer** parancsmag használatával kap védett tárolót, majd a $ProtectionContainer változóban tárolja.

A második parancs a **Get-AzureSiteRecoveryProtectionEntity** parancsmag segítségével a védett tárolóhoz tartozó védett entitásokat kapja meg $ProtectionContainer.
A parancs az eredményt a $ProtectionEntity változóban tárolja.

A végleges parancs elindítja a $ProtectionEntity tárolt védett entitások feladatátvételét, és a feladatátvétel irányát adja meg.

## PARAMÉTEREK

### -Irány
A feladatátvétel irányát adja meg.
A paraméter elfogadható értékei a következők:

- PrimaryToRecovery
- RecoveryToPrimary

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PerformSourceSideActions
Azt jelzi, hogy a művelet a forrásként használható műveleteket is elvégezheti.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PerformSourceSiteOperations
Azt jelzi, hogy a forrás-webhely műveletei végrehajthatók.

```yaml
Type: Boolean
Parameter Sets: ByPEId, ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimaryAction
Azt jelzi, hogy szükség van az elsődleges webhely műveleteire.

```yaml
Type: Boolean
Parameter Sets: ByRPId, ByRPObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionContainerId
Egy védett tároló AZONOSÍTÓját adja meg.
Ez a parancsmag elindítja a feladatot egy olyan védett virtuális géphez, amely a parancsmag által megadott tárolóhoz tartozik.

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionEntity
A webhely-helyreállítási védelem entitás objektumát adja meg.

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ProtectionEntityId
Annak a védett virtuális gépnek az AZONOSÍTÓját adja meg, amelyre a feladatot el szeretné indítani.

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPlan
A helyreállítási terv objektumát adja meg.

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RPId
Annak a helyreállítási tervnek az AZONOSÍTÓját adja meg, amelyre a feladatot el szeretné indítani.

```yaml
Type: String
Parameter Sets: ByRPId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForCompletion
Azt jelzi, hogy a parancsmag a művelet befejezéséhez vár, mielőtt a vezérlőt visszaadja a Windows PowerShell konzolnak.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureSiteRecoveryJob](./Get-AzureSiteRecoveryJob.md)

[Get-AzureSiteRecoveryProtectionContainer](./Get-AzureSiteRecoveryProtectionContainer.md)

[Get-AzureSiteRecoveryProtectionEntity](./Get-AzureSiteRecoveryProtectionEntity.md)

[Start-AzureSiteRecoveryTestFailoverJob](./Start-AzureSiteRecoveryTestFailoverJob.md)


