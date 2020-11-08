---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 00B8AB6D-02E0-45B5-AB69-49FC69246A34
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb66f34cea13ac95cac47738e7cec214a6a10103
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015583"
---
# Get-AzureSiteRecoveryRecoveryPlanFile

## Áttekintés
Azure-webhely helyreállítási tervének letöltése XML formátumban

## SZINTAXISA

### ByRPObject (alapértelmezett)
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -RecoveryPlan <ASRRecoveryPlan>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ById
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -Id <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureSiteRecoveryRecoveryPlanFile** parancsmag XML-formátumban tölti le az Azure webhelyek helyreállítási csomagját.
Ezzel a fájllal frissítheti a helyreállítási tervet, és feltöltheti a webhely-helyreállítási kiszolgálóra.

A helyreállítási terv a virtuális gépeket egy csoportba gyűjti a feladatátvétel és helyreállítás céljából.

## Példák

### Példa 1: helyreállítási terv fájljának beszerzése
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Get-AzureSiteRecoveryRecoveryPlanFile -RecoveryPlan $RecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

Ez a parancs a **Get-AzureSiteRecoveryRecoveryPlan** parancsmagot használja a helyreállítási terv beszerzéséhez, majd a $RecoveryPlan változóban tárolja.

A második parancs a **GetAzureSiteRecoveryRecoveryPlanFile** parancsmagot használja a webhely-helyreállítási terv XML-fájljának beszerzéséhez a $RecoveryPlanban.
A parancs a megadott elérési úton tárolja az XML-fájlt.

## PARAMÉTEREK

### -Azonosító
A beszerzési terv AZONOSÍTÓját adja meg.

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path (elérési út)
A helyreállítási terv XML-fájljának tárolási teljes elérési útját adja meg.

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

### -RecoveryPlan
Azt a **ASRRecoveryPlan** -objektumot adja meg, amelyből a helyreállítási tervet be szeretné szerezni.
Ha **ASRRecoveryPlan** objektumot szeretne beolvasni, használja a **Get-AzureSiteRecoveryRecoveryPlan** parancsmagot.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureSiteRecoveryRecoveryPlan](./Get-AzureSiteRecoveryRecoveryPlan.md)


