---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3A7B0280-CE6E-4374-87AF-4C1015EB88FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 4ea286ae6e3aec7f3eca961b5dc1452c717f3c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501515"
---
# New-AzureRmBackupProtectionPolicy

## Áttekintés
Biztonsági házirendet hoz létre.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### NoScheduleParamSet (alapértelmezett)
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-BackupTime] <DateTime>
 [[-DaysOfWeek] <String[]>] [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DailyScheduleParamSet
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Daily] [-BackupTime] <DateTime>
 [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WeeklyScheduleParamSet
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Weekly] [-BackupTime] <DateTime>
 [-DaysOfWeek] <String[]> [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzureRmBackupProtectionPolicy** parancsmag Azure PowerShell-objektumként hoz létre Azure Backup-házirendet.

A biztonsági házirend azt határozza meg, hogy mikor és milyen gyakran biztonsági másolatot készít az elemekről.
A Enable-AzureRmBackupProtection parancsmag biztonsági házirendet használ.

## Példák

### 1. példa: napi és havi adatmegőrzési házirend létrehozása napi és havi adatmegőrzéssel
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $ProtectionPolicy = New-AzureRmBackupProtectionPolicy -Name DailyBackup01 -Type AzureVM -Daily -BackupTime ([datetime]"3:30 PM") -RetentionPolicy ($Daily,$Monthly) -Vault $Vault
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
```

Az első parancs a Vault03 nevű boltozatot az Get-AzureRmBackupVault parancsmag segítségével kapja meg.
A parancs az objektumot a $Vault változóban tárolja.

A második parancs adatmegőrzési házirendet hoz létre a napi adatmegőrzést követő 30 napra, majd a $Daily változóban tárolja.

A harmadik parancs olyan adatmegőrzési házirendet hoz létre, amely minden hónap tizedik és huszadik részéről 12 hónapig őrzi meg a biztonsági másolatot.
A parancs az adatmegőrzési házirendet a $Monthly változóban tárolja.

A végleges parancs létrehoz egy biztonsági házirendet a 3:00 $Vault-as, napi biztonsági mentési időpontot tartalmazó boltozathoz.
A parancs kiosztja az $Daily és a $Monthlyban tárolt adatmegőrzési házirendeket.
A parancs az eredményt a $ProtectionPolicy változóban tárolja.

## PARAMÉTEREK

### -BackupTime
A nap időpontját adja meg **datetime** -objektumként a biztonsági mentési művelethez.
A **datetime** érték beolvasásához használja az Get-Date parancsmagot.
A **datetime** -objektumokkal kapcsolatos további tudnivalókért írja be a következőt: `Get-Help Get-Date` .

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Napi
Azt jelzi, hogy a biztonsági mentési művelet napi ütemterven fut.

```yaml
Type: SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysOfWeek
A hét napjainak tömbjét adja meg.
Ez a házirend a paraméter által meghatározott napokon futtatja a biztonsági mentéseket.
A paraméter elfogadható értékei a következők:

- Hétfő 
- Kedd 
- Szerda 
- Csütörtök 
- Péntek 
- Szombat 
- Vasárnap

Ha a *heti* paramétert adja meg, adja meg ezt a paramétert.

```yaml
Type: String[]
Parameter Sets: NoScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A biztonságimásolat-házirend nevét adja meg.
Jelöljön ki egy egyedi nevet a boltozatban.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetentionPolicy
A biztonságimásolat-házirend adatmegőrzési házirendjeinek tömbjét adja meg.
Ha **AzureRmBackupRetentionPolicy** szeretne beolvasni, használja az New-AzureRmBackupRetentionPolicyObject parancsmagot.

```yaml
Type: AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Type (típus)
Annak a biztonsági mentési elemnek a típusa, amelyre a házirend vonatkozik.
Jelenleg az egyetlen támogatott érték a AzureVM.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Boltozat
Itt adhatja meg azt az Azure Backup Vault-tárolót, amelyhez a biztonsági házirend tartozik.
**AzureRmBackupVault** objektum beolvasásához használja az Get-AzureRmBackupVault parancsmagot.

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Heti
Azt jelzi, hogy a biztonságimásolat-házirendet a hét egy vagy több napján indítják el hetente.

```yaml
Type: SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### AzureRmBackupProtectionPolicy

## MEGJEGYZI
* Nincs

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Enable-AzureRmBackupProtection](./Enable-AzureRmBackupProtection.md)

[Get-AzureRmBackupProtectionPolicy](./Get-AzureRmBackupProtectionPolicy.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Új – AzureRmBackupRetentionPolicyObject](./New-AzureRmBackupRetentionPolicyObject.md)

[Remove-AzureRmBackupProtectionPolicy](./Remove-AzureRmBackupProtectionPolicy.md)

[Set-AzureRmBackupProtectionPolicy](./Set-AzureRmBackupProtectionPolicy.md)


