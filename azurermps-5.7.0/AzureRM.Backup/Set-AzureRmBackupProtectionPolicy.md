---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 7d41abd1d56bab4df0d716c3a9d11ea14140b784
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501487"
---
# <span data-ttu-id="aba15-101">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="aba15-101">Set-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="aba15-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aba15-102">SYNOPSIS</span></span>
<span data-ttu-id="aba15-103">Módosított egy meglévő védelmi házirendet.</span><span class="sxs-lookup"><span data-stu-id="aba15-103">Modifies an existing protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aba15-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aba15-104">SYNTAX</span></span>

### <span data-ttu-id="aba15-105">NoScheduleParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aba15-105">NoScheduleParamSet (Default)</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aba15-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="aba15-106">DailyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aba15-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="aba15-107">WeeklyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aba15-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="aba15-108">DESCRIPTION</span></span>
<span data-ttu-id="aba15-109">A **set-AzureRmBackupProtectionPolicy** parancsmag módosította az Azure biztonsági másolatban meglévő védelmi házirendet.</span><span class="sxs-lookup"><span data-stu-id="aba15-109">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing protection policy in Azure Backup.</span></span>
<span data-ttu-id="aba15-110">A következő védelmi házirend-összetevők módosíthatók:</span><span class="sxs-lookup"><span data-stu-id="aba15-110">You can modify the following protection policy components:</span></span> 

- <span data-ttu-id="aba15-111">név</span><span class="sxs-lookup"><span data-stu-id="aba15-111">Name</span></span>
- <span data-ttu-id="aba15-112">Biztonságimásolat-ütemezés</span><span class="sxs-lookup"><span data-stu-id="aba15-112">Backup schedule</span></span>
- <span data-ttu-id="aba15-113">Adatmegőrzési házirendek</span><span class="sxs-lookup"><span data-stu-id="aba15-113">Retention policies</span></span>

<span data-ttu-id="aba15-114">Bármely módosítás hatással lehet a házirendhez társított elemek biztonsági mentésére és megtartására.</span><span class="sxs-lookup"><span data-stu-id="aba15-114">Any change might affect the backup and retention of the items associated with the policy.</span></span>

## <span data-ttu-id="aba15-115">Példák</span><span class="sxs-lookup"><span data-stu-id="aba15-115">EXAMPLES</span></span>

## <span data-ttu-id="aba15-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aba15-116">PARAMETERS</span></span>

### <span data-ttu-id="aba15-117">-BackupTime</span><span class="sxs-lookup"><span data-stu-id="aba15-117">-BackupTime</span></span>
<span data-ttu-id="aba15-118">A házirendben a nap új biztonsági időpontját **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="aba15-118">Specifies the new backup time of day, as a **DateTime** object, for the policy.</span></span>
<span data-ttu-id="aba15-119">Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="aba15-119">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="aba15-120">A **datetime** -objektumokkal kapcsolatos további tudnivalókért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="aba15-120">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba15-121">-Napi</span><span class="sxs-lookup"><span data-stu-id="aba15-121">-Daily</span></span>
<span data-ttu-id="aba15-122">Azt jelzi, hogy a biztonsági mentési művelet napi ütemterven fut.</span><span class="sxs-lookup"><span data-stu-id="aba15-122">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba15-123">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="aba15-123">-DaysOfWeek</span></span>
<span data-ttu-id="aba15-124">A hét napjainak tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aba15-124">Specifies an array of days of the week.</span></span>
<span data-ttu-id="aba15-125">Ez a házirend a paraméter által meghatározott napokon futtatja a biztonsági mentéseket.</span><span class="sxs-lookup"><span data-stu-id="aba15-125">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="aba15-126">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="aba15-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aba15-127">Hétfő</span><span class="sxs-lookup"><span data-stu-id="aba15-127">Monday</span></span> 
- <span data-ttu-id="aba15-128">Kedd</span><span class="sxs-lookup"><span data-stu-id="aba15-128">Tuesday</span></span> 
- <span data-ttu-id="aba15-129">Szerda</span><span class="sxs-lookup"><span data-stu-id="aba15-129">Wednesday</span></span> 
- <span data-ttu-id="aba15-130">Csütörtök</span><span class="sxs-lookup"><span data-stu-id="aba15-130">Thursday</span></span> 
- <span data-ttu-id="aba15-131">Péntek</span><span class="sxs-lookup"><span data-stu-id="aba15-131">Friday</span></span> 
- <span data-ttu-id="aba15-132">Szombat</span><span class="sxs-lookup"><span data-stu-id="aba15-132">Saturday</span></span> 
- <span data-ttu-id="aba15-133">Vasárnap</span><span class="sxs-lookup"><span data-stu-id="aba15-133">Sunday</span></span>

```yaml
Type: String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba15-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aba15-134">-DefaultProfile</span></span>
<span data-ttu-id="aba15-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="aba15-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aba15-136">-NewName</span><span class="sxs-lookup"><span data-stu-id="aba15-136">-NewName</span></span>
<span data-ttu-id="aba15-137">A házirend új nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aba15-137">Specifies the new name for the policy.</span></span>
<span data-ttu-id="aba15-138">A névnek egyedinek kell lennie a boltozatban.</span><span class="sxs-lookup"><span data-stu-id="aba15-138">This name must be unique in a vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba15-139">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="aba15-139">-ProtectionPolicy</span></span>
<span data-ttu-id="aba15-140">A parancsmag által módosított védelmi házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="aba15-140">Specifies protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="aba15-141">**AzureRmBackupProtectionPolicy** objektum beolvasásához használja az Get-AzureRmBackupProtectionPolicy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="aba15-141">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aba15-142">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="aba15-142">-RetentionPolicy</span></span>
<span data-ttu-id="aba15-143">A biztonságimásolat-házirend adatmegőrzési házirendjeinek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aba15-143">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="aba15-144">A **AzureRmBackupRetentionPolicy** -objektumok beolvasásához használja az New-AzureRmBackupRetentionPolicyObject parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="aba15-144">To obtain **AzureRmBackupRetentionPolicy** objects, use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba15-145">-Heti</span><span class="sxs-lookup"><span data-stu-id="aba15-145">-Weekly</span></span>
<span data-ttu-id="aba15-146">Azt jelzi, hogy a biztonsági mentési művelet heti ütemterven fut.</span><span class="sxs-lookup"><span data-stu-id="aba15-146">Indicates that the backup operation runs on a Weekly schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba15-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aba15-147">CommonParameters</span></span>
<span data-ttu-id="aba15-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aba15-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aba15-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aba15-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aba15-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aba15-150">INPUTS</span></span>

### <span data-ttu-id="aba15-151">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="aba15-151">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="aba15-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aba15-152">OUTPUTS</span></span>

### <span data-ttu-id="aba15-153">Nincs</span><span class="sxs-lookup"><span data-stu-id="aba15-153">None</span></span>

## <span data-ttu-id="aba15-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aba15-154">NOTES</span></span>

## <span data-ttu-id="aba15-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aba15-155">RELATED LINKS</span></span>

[<span data-ttu-id="aba15-156">Új – AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="aba15-156">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


