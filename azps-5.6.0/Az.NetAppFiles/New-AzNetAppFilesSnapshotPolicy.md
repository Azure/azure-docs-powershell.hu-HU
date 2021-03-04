---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: 1f8b68ac04a563dbec44b0ed43bca0a54015154d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926833"
---
# <span data-ttu-id="4a196-101">New-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="4a196-101">New-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="4a196-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a196-102">SYNOPSIS</span></span>
<span data-ttu-id="4a196-103">Új Azure NetApp-fájlok (ANF) pillanatkép-házirendet hoz létre egy ANF-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="4a196-103">Creates a new Azure NetApp Files (ANF) snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="4a196-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4a196-104">SYNTAX</span></span>

### <span data-ttu-id="4a196-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4a196-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a196-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a196-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a196-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4a196-107">DESCRIPTION</span></span>
<span data-ttu-id="4a196-108">A **New-AzNetAppFilesActiveDirectory** parancsmag új pillanatkép-házirendet hoz létre egy ANF-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="4a196-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="4a196-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4a196-109">EXAMPLES</span></span>

### <span data-ttu-id="4a196-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="4a196-110">Example 1</span></span>
```powershell
$hourlySchedule = @{        
        Minute = 2
        SnapshotsToKeep = 6
    }
    $dailySchedule = @{
        Hour = 1
        Minute = 2
        SnapshotsToKeep = 6
    }
    $weeklySchedule = @{
        Minute = 2    
        Hour = 1                
        Day = "Sunday,Monday"
        SnapshotsToKeep = 6
    }
    $monthlySchedule = @{
        Minute = 2    
        Hour = 1        
        DaysOfMonth = "2,11,21"
        SnapshotsToKeep = 6
    }
PS C:\> New-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MySnapshotPolicy" -Enabled -HourlySchedule $hourlySchedule -DailySchedule $dailySchedule -WeeklySchedule $weeklySchedule -MonthlySchedule $monthlySchedule
```

<span data-ttu-id="4a196-111">Ez a parancs létrehozza az új ANF pillanatkép-házirendet a "MyAccount" nevű ANF-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="4a196-111">This command creates the new ANF snapshot policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="4a196-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a196-112">PARAMETERS</span></span>

### <span data-ttu-id="4a196-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4a196-113">-AccountName</span></span>
<span data-ttu-id="4a196-114">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="4a196-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a196-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="4a196-115">-AccountObject</span></span>
<span data-ttu-id="4a196-116">The Account for the new Snapshot Policy object</span><span class="sxs-lookup"><span data-stu-id="4a196-116">The Account for the new Snapshot Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a196-117">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="4a196-117">-DailySchedule</span></span>
<span data-ttu-id="4a196-118">A napi ütemezést képviselő hashtable array</span><span class="sxs-lookup"><span data-stu-id="4a196-118">A hashtable array which represents the daily Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesDailySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a196-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a196-119">-DefaultProfile</span></span>
<span data-ttu-id="4a196-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4a196-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a196-121">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="4a196-121">-Enabled</span></span>
<span data-ttu-id="4a196-122">A házirendet döntéshezó tulajdonság engedélyezve van-e vagy sem</span><span class="sxs-lookup"><span data-stu-id="4a196-122">The property to decide policy is enabled or not</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a196-123">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="4a196-123">-HourlySchedule</span></span>
<span data-ttu-id="4a196-124">A hashtable array which represents the hourly Schedule</span><span class="sxs-lookup"><span data-stu-id="4a196-124">A hashtable array which represents the hourly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesHourlySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a196-125">-Location</span><span class="sxs-lookup"><span data-stu-id="4a196-125">-Location</span></span>
<span data-ttu-id="4a196-126">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="4a196-126">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a196-127">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="4a196-127">-MonthlySchedule</span></span>
<span data-ttu-id="4a196-128">A montly Schedule táblázatot képviselő hashtable array</span><span class="sxs-lookup"><span data-stu-id="4a196-128">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesMonthlySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a196-129">-Name</span><span class="sxs-lookup"><span data-stu-id="4a196-129">-Name</span></span>
<span data-ttu-id="4a196-130">Az ANF pillanatkép-házirend neve</span><span class="sxs-lookup"><span data-stu-id="4a196-130">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a196-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a196-131">-ResourceGroupName</span></span>
<span data-ttu-id="4a196-132">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="4a196-132">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a196-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="4a196-133">-Tag</span></span>
<span data-ttu-id="4a196-134">A hashtable array which represents resource tags</span><span class="sxs-lookup"><span data-stu-id="4a196-134">A hashtable array which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a196-135">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="4a196-135">-WeeklySchedule</span></span>
<span data-ttu-id="4a196-136">A montly Schedule táblázatot képviselő hashtable array</span><span class="sxs-lookup"><span data-stu-id="4a196-136">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesWeeklySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a196-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a196-137">-Confirm</span></span>
<span data-ttu-id="4a196-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4a196-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a196-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a196-139">-WhatIf</span></span>
<span data-ttu-id="4a196-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4a196-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a196-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4a196-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a196-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a196-142">CommonParameters</span></span>
<span data-ttu-id="4a196-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a196-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a196-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a196-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a196-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a196-145">INPUTS</span></span>

### <span data-ttu-id="4a196-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="4a196-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="4a196-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a196-147">OUTPUTS</span></span>

### <span data-ttu-id="4a196-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="4a196-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="4a196-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4a196-149">NOTES</span></span>

## <span data-ttu-id="4a196-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a196-150">RELATED LINKS</span></span>
