---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: edb22cc9945ca665b2e24a4488bf3335faac4f50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161258"
---
# <span data-ttu-id="219d4-101">Update-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="219d4-101">Update-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="219d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="219d4-102">SYNOPSIS</span></span>
<span data-ttu-id="219d4-103">Frissíti az Azure NetApp-fájlok (ANF) pillanatkép-házirendet a megadott opcionális módosítókra.</span><span class="sxs-lookup"><span data-stu-id="219d4-103">Updates an Azure NetApp Files (ANF) snapshot policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="219d4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="219d4-104">SYNTAX</span></span>

### <span data-ttu-id="219d4-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="219d4-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="219d4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="219d4-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled <Boolean>]
 [-HourlySchedule <PSNetAppFilesHourlySchedule>] [-DailySchedule <PSNetAppFilesDailySchedule>]
 [-WeeklySchedule <PSNetAppFilesWeeklySchedule>] [-MonthlySchedule <PSNetAppFilesMonthlySchedule>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="219d4-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="219d4-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="219d4-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="219d4-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesSnapshotPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="219d4-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="219d4-109">DESCRIPTION</span></span>
<span data-ttu-id="219d4-110">Az **Update-AzNetAppFilesSnapshotPolicy** parancsmag módosítja az ANF pillanatkép-házirendet.</span><span class="sxs-lookup"><span data-stu-id="219d4-110">The **Update-AzNetAppFilesSnapshotPolicy** cmdlet modifies an ANF snapshot policy.</span></span>

## <span data-ttu-id="219d4-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="219d4-111">EXAMPLES</span></span>

### <span data-ttu-id="219d4-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="219d4-112">Example 1</span></span>
```powershell
$hourlySchedule = @{
        Minute = 1
        SnapshotsToKeep = 3
    }
PS C:\> Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy" -HourlySchedule $hourlySchedule
```

<span data-ttu-id="219d4-113">Ez a parancs módosítja a "MySnapshotPolicy" ANF biztonsági mentési házirendet úgy, hogy az adott Órai ütemezést kapják.</span><span class="sxs-lookup"><span data-stu-id="219d4-113">This command changes the ANF backup policy "MySnapshotPolicy" to have the given HourlySchedule.</span></span>

## <span data-ttu-id="219d4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="219d4-114">PARAMETERS</span></span>

### <span data-ttu-id="219d4-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="219d4-115">-AccountName</span></span>
<span data-ttu-id="219d4-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="219d4-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="219d4-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="219d4-117">-AccountObject</span></span>
<span data-ttu-id="219d4-118">The Account for the new Snapshot Policy object</span><span class="sxs-lookup"><span data-stu-id="219d4-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="219d4-119">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="219d4-119">-DailySchedule</span></span>
<span data-ttu-id="219d4-120">A napi ütemezést képviselő hashtable array</span><span class="sxs-lookup"><span data-stu-id="219d4-120">A hashtable array which represents the daily Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesDailySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219d4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="219d4-121">-DefaultProfile</span></span>
<span data-ttu-id="219d4-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="219d4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="219d4-123">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="219d4-123">-Enabled</span></span>
<span data-ttu-id="219d4-124">A házirendet döntéshezó tulajdonság engedélyezve van-e vagy sem</span><span class="sxs-lookup"><span data-stu-id="219d4-124">The property to decide policy is enabled or not</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219d4-125">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="219d4-125">-HourlySchedule</span></span>
<span data-ttu-id="219d4-126">A hashtable array which represents the hourly Schedule</span><span class="sxs-lookup"><span data-stu-id="219d4-126">A hashtable array which represents the hourly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesHourlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219d4-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="219d4-127">-InputObject</span></span>
<span data-ttu-id="219d4-128">Az eltávolítható pillanatkép-objektum</span><span class="sxs-lookup"><span data-stu-id="219d4-128">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="219d4-129">-Location</span><span class="sxs-lookup"><span data-stu-id="219d4-129">-Location</span></span>
<span data-ttu-id="219d4-130">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="219d4-130">The location of the resource</span></span>

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

### <span data-ttu-id="219d4-131">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="219d4-131">-MonthlySchedule</span></span>
<span data-ttu-id="219d4-132">A montly Schedule tömböt képviselő hashtable array</span><span class="sxs-lookup"><span data-stu-id="219d4-132">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesMonthlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219d4-133">-Name</span><span class="sxs-lookup"><span data-stu-id="219d4-133">-Name</span></span>
<span data-ttu-id="219d4-134">Az ANF pillanatkép-házirend neve</span><span class="sxs-lookup"><span data-stu-id="219d4-134">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219d4-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="219d4-135">-ResourceGroupName</span></span>
<span data-ttu-id="219d4-136">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="219d4-136">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="219d4-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="219d4-137">-ResourceId</span></span>
<span data-ttu-id="219d4-138">Az ANF pillanatkép-házirend erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="219d4-138">The resource id of the ANF Snapshot Policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="219d4-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="219d4-139">-Tag</span></span>
<span data-ttu-id="219d4-140">A hashtable array which represents resource tags</span><span class="sxs-lookup"><span data-stu-id="219d4-140">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="219d4-141">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="219d4-141">-WeeklySchedule</span></span>
<span data-ttu-id="219d4-142">A montly Schedule tömböt képviselő hashtable array</span><span class="sxs-lookup"><span data-stu-id="219d4-142">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesWeeklySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219d4-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="219d4-143">-Confirm</span></span>
<span data-ttu-id="219d4-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="219d4-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="219d4-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="219d4-145">-WhatIf</span></span>
<span data-ttu-id="219d4-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="219d4-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="219d4-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="219d4-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="219d4-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="219d4-148">CommonParameters</span></span>
<span data-ttu-id="219d4-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="219d4-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="219d4-150">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="219d4-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="219d4-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="219d4-151">INPUTS</span></span>

### <span data-ttu-id="219d4-152">System.String</span><span class="sxs-lookup"><span data-stu-id="219d4-152">System.String</span></span>

### <span data-ttu-id="219d4-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="219d4-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="219d4-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="219d4-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="219d4-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="219d4-155">OUTPUTS</span></span>

### <span data-ttu-id="219d4-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="219d4-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="219d4-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="219d4-157">NOTES</span></span>

## <span data-ttu-id="219d4-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="219d4-158">RELATED LINKS</span></span>
