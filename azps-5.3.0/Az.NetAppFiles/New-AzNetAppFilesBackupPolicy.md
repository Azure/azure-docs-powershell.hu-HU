---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: ce49a011ba7e6c746c97e4b1aca6273d7d8b650d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466247"
---
# <span data-ttu-id="97c7a-101">New-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="97c7a-101">New-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="97c7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97c7a-102">SYNOPSIS</span></span>
<span data-ttu-id="97c7a-103">Új Azure NetApp-fájlok (ANF) biztonsági mentési házirendet hoz létre egy ANF-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="97c7a-103">Creates a new Azure NetApp Files (ANF) backup policy for an ANF account.</span></span>

## <span data-ttu-id="97c7a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="97c7a-104">SYNTAX</span></span>

### <span data-ttu-id="97c7a-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="97c7a-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97c7a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97c7a-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackupPolicy -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>]
 [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97c7a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="97c7a-107">DESCRIPTION</span></span>
<span data-ttu-id="97c7a-108">A **New-AzNetAppFilesActiveDirectory** parancsmag létrehoz egy új biztonságimásolat-házirendet egy ANF-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="97c7a-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new backup policy for an ANF account.</span></span>

## <span data-ttu-id="97c7a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="97c7a-109">EXAMPLES</span></span>

### <span data-ttu-id="97c7a-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="97c7a-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyBackupPolicy" -Tag @{"tag1" = "tagValue"} -Enabled -DailyBackupsToKeep 1 -WeeklyBackupsToKeep 2 -MonthlyBackupsToKeep 2 -YearlyBackupsToKeep 1
```

<span data-ttu-id="97c7a-111">Ez a parancs létrehozza az új ANF biztonsági mentési házirendet a "MyAccount" nevű ANF-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="97c7a-111">This command creates the new ANF backup policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="97c7a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97c7a-112">PARAMETERS</span></span>

### <span data-ttu-id="97c7a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="97c7a-113">-AccountName</span></span>
<span data-ttu-id="97c7a-114">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="97c7a-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="97c7a-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="97c7a-115">-AccountObject</span></span>
<span data-ttu-id="97c7a-116">Az új biztonsági mentési házirend Fiók objektuma</span><span class="sxs-lookup"><span data-stu-id="97c7a-116">The Account object for the new Backup Policy</span></span>

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

### <span data-ttu-id="97c7a-117">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="97c7a-117">-DailyBackupsToKeep</span></span>
<span data-ttu-id="97c7a-118">Napi biztonsági másolatok száma</span><span class="sxs-lookup"><span data-stu-id="97c7a-118">Daily backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97c7a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97c7a-119">-DefaultProfile</span></span>
<span data-ttu-id="97c7a-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="97c7a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97c7a-121">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="97c7a-121">-Enabled</span></span>
<span data-ttu-id="97c7a-122">A házirendet döntéshezó tulajdonság engedélyezve van-e vagy sem</span><span class="sxs-lookup"><span data-stu-id="97c7a-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="97c7a-123">-Location</span><span class="sxs-lookup"><span data-stu-id="97c7a-123">-Location</span></span>
<span data-ttu-id="97c7a-124">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="97c7a-124">The location of the resource</span></span>

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

### <span data-ttu-id="97c7a-125">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="97c7a-125">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="97c7a-126">A havi biztonsági másolatok számát meg kell tartani</span><span class="sxs-lookup"><span data-stu-id="97c7a-126">Monthly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97c7a-127">-Name</span><span class="sxs-lookup"><span data-stu-id="97c7a-127">-Name</span></span>
<span data-ttu-id="97c7a-128">Az ANF biztonsági mentési házirend neve</span><span class="sxs-lookup"><span data-stu-id="97c7a-128">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97c7a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97c7a-129">-ResourceGroupName</span></span>
<span data-ttu-id="97c7a-130">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="97c7a-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="97c7a-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="97c7a-131">-Tag</span></span>
<span data-ttu-id="97c7a-132">A hashtable array which represents resource tags</span><span class="sxs-lookup"><span data-stu-id="97c7a-132">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="97c7a-133">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="97c7a-133">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="97c7a-134">Heti biztonsági másolatok száma</span><span class="sxs-lookup"><span data-stu-id="97c7a-134">Weekly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97c7a-135">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="97c7a-135">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="97c7a-136">Meg kell tartani az éves biztonsági mentések számát</span><span class="sxs-lookup"><span data-stu-id="97c7a-136">Yearly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97c7a-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97c7a-137">-Confirm</span></span>
<span data-ttu-id="97c7a-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="97c7a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97c7a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97c7a-139">-WhatIf</span></span>
<span data-ttu-id="97c7a-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="97c7a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97c7a-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="97c7a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97c7a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97c7a-142">CommonParameters</span></span>
<span data-ttu-id="97c7a-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97c7a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97c7a-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97c7a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97c7a-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97c7a-145">INPUTS</span></span>

### <span data-ttu-id="97c7a-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="97c7a-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="97c7a-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97c7a-147">OUTPUTS</span></span>

### <span data-ttu-id="97c7a-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="97c7a-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="97c7a-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="97c7a-149">NOTES</span></span>

## <span data-ttu-id="97c7a-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97c7a-150">RELATED LINKS</span></span>
