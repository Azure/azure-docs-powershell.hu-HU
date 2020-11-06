---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: 3402dc7018f094a5f95a967385d9bae8d70c68f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494564"
---
# Get-AzureRmBackupJob

## Áttekintés
Biztonsági mentési feladatokat kap.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### FiltersSet (alapértelmezett)
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### JobsListFilter
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmBackupJob** parancsmag Azure biztonságimásolat-készítési feladatokat kap egy adott boltozathoz.

## Példák

### Példa 1: a biztonságimásolat-tároló minden feladatának beszerzése
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

Az első parancs a Vault03 nevű boltozatot a **Get-AzureRmBackupVault** parancsmag használatával kapja.
A parancs az objektumot a $Vault változóban tárolja.

A második parancs a boltozat összes feladatát a $Vault-ban kapja meg.

### 2. példa: Befejezett feladatok beszerzése
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

Ennek a parancsnak a kitöltése a $Vault boltozatán keresztül végezhető el.

### 3. példa: Sikertelen feladatok beolvasása a múlt héten
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

Ez a parancs nem működik a múlt héten a $Vault a boltozatról.
A *from* paraméter a múltbeli hét napos időpontot adja meg.
A parancs nem adja meg *a paraméter értékét* .
Ennek megfelelően az aktuális idő alapértelmezett értékét használja.

### 4. példa: egy folyamatban lévő projekt szavazás biztonsági másolata, amely befejeződött
```
PS C:\>$Jobs = Get-AzureRmBackupJob -Vault $Vault -Status InProgress
$Job = $Jobs[0] 
while ( $Job.Status -ne Completed ) 
{
   Write-Host "Waiting for completion..." 
   Start-Sleep -Seconds 10
   $job = Get-AzureRmBackupJob -Vault $Vault -Job $Job
}
Write-Host "Done!"
Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

Ez a parancsfájl az első olyan feladatot kérdezi le, amely jelenleg folyamatban van addig, amíg a projekt be nem fejeződik.

A parancsfájl első sora megkapja a folyamatban lévő $Vault összes feladatát, majd a $Jobs tömbképlet tárolja ezeket a feladatokat.

A második sor az első feladatot az $Job változó $Jobs tömbből tárolja.

A harmadik sorba egy **while** ciklust indít, amely a feladat aktuális állapotát vizsgálja, amíg a feladat el nem készül.
A **while** kulcsszóval kapcsolatos további tudnivalókért írja be a következőt: `Get-Help about_While` .

A **while** ciklusban egy üzenet jelenik meg a konzolon, tíz másodpercig alszik, majd frissíti a $Job változót.
A parancsfájl a $Job meglévő értékével frissíti a $Job változót, és a jelenlegi parancsmagot használva beolvassa a feladat aktuális állapotát.
A Windows PowerShell-parancsmagokról a és a következő témakörben olvashat bővebben `Get-Help Write-Host` `Get-Help Start-Sleep` .

A parancsfájl utolsó sora közli, hogy a parancsfájl elkészült.

## PARAMÉTEREK

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

### -From
A parancsmag által beolvasott feladatok időtartományának kezdetét **datetime** -objektumként adja meg.
Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.
A **datetime** -objektumokkal kapcsolatos további tudnivalókért írja be a következőt: `Get-Help Get-Date` .

```yaml
Type: DateTime
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
A parancsmag által kapott feladatot adja meg.
**AzureRmBackupJob** objektum beolvasásához használja az Get-AzureRmBackupJob parancsmagot.

```yaml
Type: AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Annak a projektnek az AZONOSÍTÓját adja meg, amely a parancsmagot kapja.
Az azonosító egy **AzureRmBackupJob** objektum **InstanceId** tulajdonsága.
**AzureRmBackupJob** -objektum beszerzéséhez használja a Get-AzureRmBackupJob.

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Művelet
A parancsmag által kapott feladatok működését adja meg.
A paraméter elfogadható értékei a következők:

- Hát 
- ConfigureBackup 
- DeleteBackupData 
- Regisztráció 
- Visszaállítása 
- Védtelen 
- Regisztrációját

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Állapot
A parancsmag által kapott feladatok állapotát adja meg.
A paraméter elfogadható értékei a következők:

- Előrehaladás
- Sikertelen
- Lemondott
- Értekezletének lemondása
- Kész
- CompletedWithWarnings 

Ezt a paramétert akkor adhatja meg, ha az összes folyamatban lévő feladatban vagy az összes sikertelen munkahelyen keres.

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -To
Annak a projektnek az időtartományának a végét adja meg **datetime** -objektumként, amely a parancsmagot kapja.
Az alapértelmezett érték az aktuális rendszer idő.
Ha ezt a paramétert adja meg, a *from* paramétert is meg kell adnia.

```yaml
Type: DateTime
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type (típus)
Annak a tárolónak a típusa, amelyre a parancsmag biztonsági mentési feladatokat kap.
Jelenleg az egyetlen támogatott érték a AzureVM.

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Boltozat
Annak a biztonságimásolat-tárolónak a megadása, amelyhez ez a parancsmag feladatokat kap.
**AzureRmBackupVault** objektum beolvasásához használja az Get-AzureRmBackupVault parancsmagot.

```yaml
Type: AzureRMBackupVault
Parameter Sets: FiltersSet
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

### AzureRmBackupVault

## KIMENETEK

### AzureRmBackupJob[]
Ez a parancsmag egy vagy több biztonságimásolat-feladatot ad eredményül.

## MEGJEGYZI
* Nincs

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Stop-AzureRmBackupJob](./Stop-AzureRmBackupJob.md)

[Várjon-AzureRmBackupJob](./Wait-AzureRmBackupJob.md)


