---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2575F5C4-A276-49CE-AB0C-726F359DA6F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f71138e47c851097fe36ca294784fc571b6369f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015751"
---
# Start-AzureSiteRecoveryPlannedFailoverJob

## Áttekintés
A webhely-helyreállítási tervezett feladatátvételi művelet elindítása

## SZINTAXISA

### ByRPId (alapértelmezett)
```
Start-AzureSiteRecoveryPlannedFailoverJob -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByPEId
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRPObject
```
Start-AzureSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByPEObject
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Start-AzureSiteRecoveryPlannedFailoverJob** parancsmag tervezett feladatátvételt indít az Azure webhely-helyreállítási védelmi entitások vagy helyreállítási tervek számára.
Ellenőrizheti, hogy a feladat sikeres volt-e a **Get-AzureSiteRecoveryJob** parancsmag használatával.

## Példák

### 1. példa: tervezett feladatátvételi feladat indítása
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryPlannedFailoverJob -Direction PrimaryToRecovery -ProtectionEntity $Protected -Optimize ForDowntime
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

Az első parancs a **Get-AzureSiteRecoveryProtectionContainer** parancsmag segítségével az aktuális Azure-webhely helyreállítási tárolójában minden védett tárolót megkapja, majd a $Container változóban tárolja az eredményeket.
Ebben a példában egyetlen tároló található.

A második parancs a **Get-AzureSiteRecoveryProtectionEntity** parancsmaggal a $Container tárolt tárolóhoz tartozó védett virtuális gépeket kapja.
A parancs az eredményt a $Protected változóban tárolja.

A végleges parancs elindítja a feladatátvételi feladatot az $Protected-ban tárolt védett virtuális gépek iránya PrimaryToRecovery.

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

### -Optimalizálás
Itt adhatja meg, hogy mit szeretne optimalizálni.
Ez a paraméter egy Azure-webhelyről a helyszíni webhelyre való feladatátvételre vonatkozik, amely jelentős adatszinkronizálást követel meg.
A paraméter elfogadható értékei a következők:

- ForDowntime
- ForSynchronization

Ha a **ForDowntime** meg van adva, ez azt jelzi, hogy az adatokat a program szinkronizálja a feladatátvétel minimalizálása előtt.
A szinkronizálás a virtuális gép leállítása nélkül végezhető el.
Miután befejeződött a szinkronizálás, a program felfüggeszti a feladatot.
Folytassa a feladatot, és végezze el a szinkronizálási műveletet, amely leállítja a virtuális gépet.

Ha a **ForSynchronization** meg van adva, ez azt jelzi, hogy az adatok szinkronizálása a feladatátvétel során történik, így az adatok szinkronizálása kisméretű.
Mivel ez a beállítás engedélyezve van, a virtuális gép azonnal leállt.
A szinkronizálás a leállítást követően kezdődik a feladatátvételi művelet befejezéséhez.

```yaml
Type: String
Parameter Sets: (All)
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
Annak a védett tárolónak az AZONOSÍTÓját adja meg, amelybe a feladatot el szeretné indítani.

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
Azt a **ASRProtectionEntity** -objektumot adja meg, amelybe a feladatot el szeretné kezdeni.
Ha **ASRProtectionEntity** objektumot szeretne beolvasni, használja a **Get-AzureSiteRecoveryProtectionEntity** parancsmagot.

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

[Get-AzureSiteRecoveryProtectionContainer](./Get-AzureSiteRecoveryProtectionContainer.md)

[Get-AzureSiteRecoveryProtectionEntity](./Get-AzureSiteRecoveryProtectionEntity.md)


