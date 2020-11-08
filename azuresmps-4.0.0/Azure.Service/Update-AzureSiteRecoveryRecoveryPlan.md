---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 5625ED47-BD85-4BF5-9044-2012E5A67BA4
online version: ''
schema: 2.0.0
ms.openlocfilehash: d1c680adf1d9d850f89cb81e1525a0e0e06eb6c9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016014"
---
# Update-AzureSiteRecoveryRecoveryPlan

## Áttekintés
Helyreállítási terv frissítése a webhely-helyreállításban.

## SZINTAXISA

```
Update-AzureSiteRecoveryRecoveryPlan -File <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
Az **Update-AzureSiteRecoveryRecoveryPlan** parancsmag az Azure-webhely helyreállításakor frissíti a helyreállítási tervet, majd közzéteszi azt.

## Példák

### Példa 1: helyreállítási terv frissítése
```
PS C:\> Update-AzureSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

Ez a parancs frissíti a megadott helyreállítási csomagot, majd közzéteszi azt.

## PARAMÉTEREK

### -Fájl
A parancsmag által frissített helyreállítási terv helyreállítási tervének fájlját adja meg.

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

[Get-AzureSiteRecoveryRecoveryPlan](./Get-AzureSiteRecoveryRecoveryPlan.md)

[Új – AzureSiteRecoveryRecoveryPlan](./New-AzureSiteRecoveryRecoveryPlan.md)

[Remove-AzureSiteRecoveryRecoveryPlan](./Remove-AzureSiteRecoveryRecoveryPlan.md)


