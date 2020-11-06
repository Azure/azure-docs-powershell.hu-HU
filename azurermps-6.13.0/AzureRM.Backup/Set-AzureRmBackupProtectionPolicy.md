---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: caf6394ce84b18bd8e36b4504173fe7f7bb07fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494175"
---
# <span data-ttu-id="a02a6-101">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a02a6-101">Set-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="a02a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a02a6-102">SYNOPSIS</span></span>
<span data-ttu-id="a02a6-103">Módosított egy meglévő védelmi házirendet.</span><span class="sxs-lookup"><span data-stu-id="a02a6-103">Modifies an existing protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a02a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a02a6-104">SYNTAX</span></span>

### <span data-ttu-id="a02a6-105">NoScheduleParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a02a6-105">NoScheduleParamSet (Default)</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a02a6-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="a02a6-106">DailyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a02a6-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="a02a6-107">WeeklyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a02a6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a02a6-108">DESCRIPTION</span></span>
<span data-ttu-id="a02a6-109">A **set-AzureRmBackupProtectionPolicy** parancsmag módosította az Azure biztonsági másolatban meglévő védelmi házirendet.</span><span class="sxs-lookup"><span data-stu-id="a02a6-109">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing protection policy in Azure Backup.</span></span>
<span data-ttu-id="a02a6-110">A következő védelmi házirend-összetevők módosíthatók:</span><span class="sxs-lookup"><span data-stu-id="a02a6-110">You can modify the following protection policy components:</span></span> 
- <span data-ttu-id="a02a6-111">név</span><span class="sxs-lookup"><span data-stu-id="a02a6-111">Name</span></span>
- <span data-ttu-id="a02a6-112">Biztonságimásolat-ütemezés</span><span class="sxs-lookup"><span data-stu-id="a02a6-112">Backup schedule</span></span>
- <span data-ttu-id="a02a6-113">Adatmegőrzési szabályok: bármely módosítás hatással lehet a házirendhez társított elemek biztonsági mentésére és megtartására.</span><span class="sxs-lookup"><span data-stu-id="a02a6-113">Retention policies Any change might affect the backup and retention of the items associated with the policy.</span></span>

## <span data-ttu-id="a02a6-114">Példák</span><span class="sxs-lookup"><span data-stu-id="a02a6-114">EXAMPLES</span></span>

## <span data-ttu-id="a02a6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a02a6-115">PARAMETERS</span></span>

### <span data-ttu-id="a02a6-116">-BackupTime</span><span class="sxs-lookup"><span data-stu-id="a02a6-116">-BackupTime</span></span>
<span data-ttu-id="a02a6-117">A házirendben a nap új biztonsági időpontját **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="a02a6-117">Specifies the new backup time of day, as a **DateTime** object, for the policy.</span></span>
<span data-ttu-id="a02a6-118">Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a02a6-118">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="a02a6-119">A **datetime** -objektumokkal kapcsolatos további tudnivalókért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="a02a6-119">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a02a6-120">-Napi</span><span class="sxs-lookup"><span data-stu-id="a02a6-120">-Daily</span></span>
<span data-ttu-id="a02a6-121">Azt jelzi, hogy a biztonsági mentési művelet napi ütemterven fut.</span><span class="sxs-lookup"><span data-stu-id="a02a6-121">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a02a6-122">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="a02a6-122">-DaysOfWeek</span></span>
<span data-ttu-id="a02a6-123">A hét napjainak tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a02a6-123">Specifies an array of days of the week.</span></span>
<span data-ttu-id="a02a6-124">Ez a házirend a paraméter által meghatározott napokon futtatja a biztonsági mentéseket.</span><span class="sxs-lookup"><span data-stu-id="a02a6-124">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="a02a6-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a02a6-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a02a6-126">Hétfő</span><span class="sxs-lookup"><span data-stu-id="a02a6-126">Monday</span></span> 
- <span data-ttu-id="a02a6-127">Kedd</span><span class="sxs-lookup"><span data-stu-id="a02a6-127">Tuesday</span></span> 
- <span data-ttu-id="a02a6-128">Szerda</span><span class="sxs-lookup"><span data-stu-id="a02a6-128">Wednesday</span></span> 
- <span data-ttu-id="a02a6-129">Csütörtök</span><span class="sxs-lookup"><span data-stu-id="a02a6-129">Thursday</span></span> 
- <span data-ttu-id="a02a6-130">Péntek</span><span class="sxs-lookup"><span data-stu-id="a02a6-130">Friday</span></span> 
- <span data-ttu-id="a02a6-131">Szombat</span><span class="sxs-lookup"><span data-stu-id="a02a6-131">Saturday</span></span> 
- <span data-ttu-id="a02a6-132">Vasárnap</span><span class="sxs-lookup"><span data-stu-id="a02a6-132">Sunday</span></span>

```yaml
Type: System.String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a02a6-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a02a6-133">-DefaultProfile</span></span>
<span data-ttu-id="a02a6-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a02a6-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a02a6-135">-NewName</span><span class="sxs-lookup"><span data-stu-id="a02a6-135">-NewName</span></span>
<span data-ttu-id="a02a6-136">A házirend új nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a02a6-136">Specifies the new name for the policy.</span></span>
<span data-ttu-id="a02a6-137">A névnek egyedinek kell lennie a boltozatban.</span><span class="sxs-lookup"><span data-stu-id="a02a6-137">This name must be unique in a vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a02a6-138">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a02a6-138">-ProtectionPolicy</span></span>
<span data-ttu-id="a02a6-139">A parancsmag által módosított védelmi házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="a02a6-139">Specifies protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="a02a6-140">**AzureRmBackupProtectionPolicy** objektum beolvasásához használja az Get-AzureRmBackupProtectionPolicy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a02a6-140">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a02a6-141">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a02a6-141">-RetentionPolicy</span></span>
<span data-ttu-id="a02a6-142">A biztonságimásolat-házirend adatmegőrzési házirendjeinek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a02a6-142">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="a02a6-143">A **AzureRmBackupRetentionPolicy** -objektumok beolvasásához használja az New-AzureRmBackupRetentionPolicyObject parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a02a6-143">To obtain **AzureRmBackupRetentionPolicy** objects, use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a02a6-144">-Heti</span><span class="sxs-lookup"><span data-stu-id="a02a6-144">-Weekly</span></span>
<span data-ttu-id="a02a6-145">Azt jelzi, hogy a biztonsági mentési művelet heti ütemterven fut.</span><span class="sxs-lookup"><span data-stu-id="a02a6-145">Indicates that the backup operation runs on a Weekly schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a02a6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a02a6-146">CommonParameters</span></span>
<span data-ttu-id="a02a6-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a02a6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a02a6-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a02a6-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a02a6-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a02a6-149">INPUTS</span></span>

### <span data-ttu-id="a02a6-150">Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a02a6-150">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy</span></span>
<span data-ttu-id="a02a6-151">Paraméterek: ProtectionPolicy (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a02a6-151">Parameters: ProtectionPolicy (ByValue)</span></span>

## <span data-ttu-id="a02a6-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a02a6-152">OUTPUTS</span></span>

### <span data-ttu-id="a02a6-153">Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="a02a6-153">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="a02a6-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a02a6-154">NOTES</span></span>

## <span data-ttu-id="a02a6-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a02a6-155">RELATED LINKS</span></span>

[<span data-ttu-id="a02a6-156">Új – AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a02a6-156">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


