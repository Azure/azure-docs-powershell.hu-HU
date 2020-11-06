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
# <span data-ttu-id="aed20-101">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="aed20-101">New-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="aed20-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aed20-102">SYNOPSIS</span></span>
<span data-ttu-id="aed20-103">Biztonsági házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="aed20-103">Creates a Backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aed20-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aed20-104">SYNTAX</span></span>

### <span data-ttu-id="aed20-105">NoScheduleParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aed20-105">NoScheduleParamSet (Default)</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-BackupTime] <DateTime>
 [[-DaysOfWeek] <String[]>] [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aed20-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="aed20-106">DailyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Daily] [-BackupTime] <DateTime>
 [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aed20-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="aed20-107">WeeklyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Weekly] [-BackupTime] <DateTime>
 [-DaysOfWeek] <String[]> [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aed20-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="aed20-108">DESCRIPTION</span></span>
<span data-ttu-id="aed20-109">A **New-AzureRmBackupProtectionPolicy** parancsmag Azure PowerShell-objektumként hoz létre Azure Backup-házirendet.</span><span class="sxs-lookup"><span data-stu-id="aed20-109">The **New-AzureRmBackupProtectionPolicy** cmdlet creates an Azure Backup policy as an Azure PowerShell object.</span></span>

<span data-ttu-id="aed20-110">A biztonsági házirend azt határozza meg, hogy mikor és milyen gyakran biztonsági másolatot készít az elemekről.</span><span class="sxs-lookup"><span data-stu-id="aed20-110">A backup policy defines when and how often Backup backs up an item.</span></span>
<span data-ttu-id="aed20-111">A Enable-AzureRmBackupProtection parancsmag biztonsági házirendet használ.</span><span class="sxs-lookup"><span data-stu-id="aed20-111">The Enable-AzureRmBackupProtection cmdlet uses a backup policy.</span></span>

## <span data-ttu-id="aed20-112">Példák</span><span class="sxs-lookup"><span data-stu-id="aed20-112">EXAMPLES</span></span>

### <span data-ttu-id="aed20-113">1. példa: napi és havi adatmegőrzési házirend létrehozása napi és havi adatmegőrzéssel</span><span class="sxs-lookup"><span data-stu-id="aed20-113">Example 1: Create a daily backup policy with daily and monthly retention</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $ProtectionPolicy = New-AzureRmBackupProtectionPolicy -Name DailyBackup01 -Type AzureVM -Daily -BackupTime ([datetime]"3:30 PM") -RetentionPolicy ($Daily,$Monthly) -Vault $Vault
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
```

<span data-ttu-id="aed20-114">Az első parancs a Vault03 nevű boltozatot az Get-AzureRmBackupVault parancsmag segítségével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aed20-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="aed20-115">A parancs az objektumot a $Vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="aed20-115">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="aed20-116">A második parancs adatmegőrzési házirendet hoz létre a napi adatmegőrzést követő 30 napra, majd a $Daily változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="aed20-116">The second command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="aed20-117">A harmadik parancs olyan adatmegőrzési házirendet hoz létre, amely minden hónap tizedik és huszadik részéről 12 hónapig őrzi meg a biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="aed20-117">The third command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="aed20-118">A parancs az adatmegőrzési házirendet a $Monthly változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="aed20-118">The command stores the retention policy in the $Monthly variable.</span></span>

<span data-ttu-id="aed20-119">A végleges parancs létrehoz egy biztonsági házirendet a 3:00 $Vault-as, napi biztonsági mentési időpontot tartalmazó boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="aed20-119">The final command creates a backup policy for the vault in $Vault that has a daily backup time of 3:00 PM.</span></span>
<span data-ttu-id="aed20-120">A parancs kiosztja az $Daily és a $Monthlyban tárolt adatmegőrzési házirendeket.</span><span class="sxs-lookup"><span data-stu-id="aed20-120">The command assigns the retention policies stored in $Daily and $Monthly.</span></span>
<span data-ttu-id="aed20-121">A parancs az eredményt a $ProtectionPolicy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="aed20-121">The command stores the result in the $ProtectionPolicy variable.</span></span>

## <span data-ttu-id="aed20-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aed20-122">PARAMETERS</span></span>

### <span data-ttu-id="aed20-123">-BackupTime</span><span class="sxs-lookup"><span data-stu-id="aed20-123">-BackupTime</span></span>
<span data-ttu-id="aed20-124">A nap időpontját adja meg **datetime** -objektumként a biztonsági mentési művelethez.</span><span class="sxs-lookup"><span data-stu-id="aed20-124">Specifies the time of day, as a **DateTime** object, for the backup operation.</span></span>
<span data-ttu-id="aed20-125">A **datetime** érték beolvasásához használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="aed20-125">To obtain a **DateTime** , use the Get-Date cmdlet.</span></span>
<span data-ttu-id="aed20-126">A **datetime** -objektumokkal kapcsolatos további tudnivalókért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="aed20-126">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="aed20-127">-Napi</span><span class="sxs-lookup"><span data-stu-id="aed20-127">-Daily</span></span>
<span data-ttu-id="aed20-128">Azt jelzi, hogy a biztonsági mentési művelet napi ütemterven fut.</span><span class="sxs-lookup"><span data-stu-id="aed20-128">Indicates that the backup operation runs on a Daily schedule.</span></span>

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

### <span data-ttu-id="aed20-129">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="aed20-129">-DaysOfWeek</span></span>
<span data-ttu-id="aed20-130">A hét napjainak tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aed20-130">Specifies an array of days of the week.</span></span>
<span data-ttu-id="aed20-131">Ez a házirend a paraméter által meghatározott napokon futtatja a biztonsági mentéseket.</span><span class="sxs-lookup"><span data-stu-id="aed20-131">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="aed20-132">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="aed20-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aed20-133">Hétfő</span><span class="sxs-lookup"><span data-stu-id="aed20-133">Monday</span></span> 
- <span data-ttu-id="aed20-134">Kedd</span><span class="sxs-lookup"><span data-stu-id="aed20-134">Tuesday</span></span> 
- <span data-ttu-id="aed20-135">Szerda</span><span class="sxs-lookup"><span data-stu-id="aed20-135">Wednesday</span></span> 
- <span data-ttu-id="aed20-136">Csütörtök</span><span class="sxs-lookup"><span data-stu-id="aed20-136">Thursday</span></span> 
- <span data-ttu-id="aed20-137">Péntek</span><span class="sxs-lookup"><span data-stu-id="aed20-137">Friday</span></span> 
- <span data-ttu-id="aed20-138">Szombat</span><span class="sxs-lookup"><span data-stu-id="aed20-138">Saturday</span></span> 
- <span data-ttu-id="aed20-139">Vasárnap</span><span class="sxs-lookup"><span data-stu-id="aed20-139">Sunday</span></span>

<span data-ttu-id="aed20-140">Ha a *heti* paramétert adja meg, adja meg ezt a paramétert.</span><span class="sxs-lookup"><span data-stu-id="aed20-140">If you specify the *Weekly* parameter, specify this parameter.</span></span>

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

### <span data-ttu-id="aed20-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aed20-141">-DefaultProfile</span></span>
<span data-ttu-id="aed20-142">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="aed20-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aed20-143">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aed20-143">-Name</span></span>
<span data-ttu-id="aed20-144">A biztonságimásolat-házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aed20-144">Specifies a name for the backup policy.</span></span>
<span data-ttu-id="aed20-145">Jelöljön ki egy egyedi nevet a boltozatban.</span><span class="sxs-lookup"><span data-stu-id="aed20-145">Select a name that is unique in the vault.</span></span>

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

### <span data-ttu-id="aed20-146">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="aed20-146">-RetentionPolicy</span></span>
<span data-ttu-id="aed20-147">A biztonságimásolat-házirend adatmegőrzési házirendjeinek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aed20-147">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="aed20-148">Ha **AzureRmBackupRetentionPolicy** szeretne beolvasni, használja az New-AzureRmBackupRetentionPolicyObject parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="aed20-148">To obtain an **AzureRmBackupRetentionPolicy** , use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

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

### <span data-ttu-id="aed20-149">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="aed20-149">-Type</span></span>
<span data-ttu-id="aed20-150">Annak a biztonsági mentési elemnek a típusa, amelyre a házirend vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="aed20-150">Specifies the type of backup item to which the policy applies.</span></span>
<span data-ttu-id="aed20-151">Jelenleg az egyetlen támogatott érték a AzureVM.</span><span class="sxs-lookup"><span data-stu-id="aed20-151">Currently, the only supported value is AzureVM.</span></span>

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

### <span data-ttu-id="aed20-152">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="aed20-152">-Vault</span></span>
<span data-ttu-id="aed20-153">Itt adhatja meg azt az Azure Backup Vault-tárolót, amelyhez a biztonsági házirend tartozik.</span><span class="sxs-lookup"><span data-stu-id="aed20-153">Specifies the Azure Backup vault to which the backup policy belongs.</span></span>
<span data-ttu-id="aed20-154">**AzureRmBackupVault** objektum beolvasásához használja az Get-AzureRmBackupVault parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="aed20-154">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="aed20-155">-Heti</span><span class="sxs-lookup"><span data-stu-id="aed20-155">-Weekly</span></span>
<span data-ttu-id="aed20-156">Azt jelzi, hogy a biztonságimásolat-házirendet a hét egy vagy több napján indítják el hetente.</span><span class="sxs-lookup"><span data-stu-id="aed20-156">Indicates that the backup policy is triggered weekly on one or more days of the week.</span></span>

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

### <span data-ttu-id="aed20-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aed20-157">CommonParameters</span></span>
<span data-ttu-id="aed20-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aed20-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aed20-159">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aed20-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aed20-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aed20-160">INPUTS</span></span>

### <span data-ttu-id="aed20-161">Nincs</span><span class="sxs-lookup"><span data-stu-id="aed20-161">None</span></span>

## <span data-ttu-id="aed20-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aed20-162">OUTPUTS</span></span>

### <span data-ttu-id="aed20-163">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="aed20-163">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="aed20-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aed20-164">NOTES</span></span>
* <span data-ttu-id="aed20-165">Nincs</span><span class="sxs-lookup"><span data-stu-id="aed20-165">None</span></span>

## <span data-ttu-id="aed20-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aed20-166">RELATED LINKS</span></span>

[<span data-ttu-id="aed20-167">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="aed20-167">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="aed20-168">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="aed20-168">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="aed20-169">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="aed20-169">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="aed20-170">Új – AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="aed20-170">New-AzureRmBackupRetentionPolicyObject</span></span>](./New-AzureRmBackupRetentionPolicyObject.md)

[<span data-ttu-id="aed20-171">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="aed20-171">Remove-AzureRmBackupProtectionPolicy</span></span>](./Remove-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="aed20-172">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="aed20-172">Set-AzureRmBackupProtectionPolicy</span></span>](./Set-AzureRmBackupProtectionPolicy.md)


