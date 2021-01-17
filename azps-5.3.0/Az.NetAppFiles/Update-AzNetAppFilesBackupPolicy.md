---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 0cebe34948984e36c9ad2fbe30de8da3a0e0ca92
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380489"
---
# <span data-ttu-id="3e355-101">Update-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="3e355-101">Update-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="3e355-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e355-102">SYNOPSIS</span></span>
<span data-ttu-id="3e355-103">Frissíti az Azure NetApp-fájlok (ANF) biztonsági mentési házirendet a megadott opcionális módosítókra.</span><span class="sxs-lookup"><span data-stu-id="3e355-103">Updates an Azure NetApp Files (ANF) backup policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="3e355-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3e355-104">SYNTAX</span></span>

### <span data-ttu-id="3e355-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3e355-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>]
 [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e355-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e355-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e355-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e355-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e355-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e355-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesBackupPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e355-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3e355-109">DESCRIPTION</span></span>
<span data-ttu-id="3e355-110">Az **Update-AzNetAppFilesBackupPolicy** parancsmag módosítja az ANF biztonsági mentési házirendet.</span><span class="sxs-lookup"><span data-stu-id="3e355-110">The **Update-AzNetAppFilesBackupPolicy** cmdlet modifies an ANF backup policy .</span></span>

## <span data-ttu-id="3e355-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3e355-111">EXAMPLES</span></span>

### <span data-ttu-id="3e355-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="3e355-112">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy" -DailyBackupsToKeep 2
```

<span data-ttu-id="3e355-113">Ez a parancs módosítja a "MyBackupPolicy" ANF biztonsági mentési házirendet úgy, hogy az adott DailyBackupsToKeep legyen.</span><span class="sxs-lookup"><span data-stu-id="3e355-113">This command changes the ANF backup policy "MyBackupPolicy" to have the given DailyBackupsToKeep.</span></span>

## <span data-ttu-id="3e355-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e355-114">PARAMETERS</span></span>

### <span data-ttu-id="3e355-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3e355-115">-AccountName</span></span>
<span data-ttu-id="3e355-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="3e355-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="3e355-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="3e355-117">-AccountObject</span></span>
<span data-ttu-id="3e355-118">The Account object containing the Backup Policy to update</span><span class="sxs-lookup"><span data-stu-id="3e355-118">The Account object containing the Backup Policy to update</span></span>

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

### <span data-ttu-id="3e355-119">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="3e355-119">-DailyBackupsToKeep</span></span>
<span data-ttu-id="3e355-120">Napi biztonsági másolatok száma</span><span class="sxs-lookup"><span data-stu-id="3e355-120">Daily backups count to keep</span></span>

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

### <span data-ttu-id="3e355-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e355-121">-DefaultProfile</span></span>
<span data-ttu-id="3e355-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e355-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e355-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e355-123">-InputObject</span></span>
<span data-ttu-id="3e355-124">Az eltávolítható BackupPolicy objektum</span><span class="sxs-lookup"><span data-stu-id="3e355-124">The BackupPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e355-125">-Location</span><span class="sxs-lookup"><span data-stu-id="3e355-125">-Location</span></span>
<span data-ttu-id="3e355-126">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="3e355-126">The location of the resource</span></span>

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

### <span data-ttu-id="3e355-127">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="3e355-127">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="3e355-128">Meg kell tartani a havi biztonsági másolatok számát</span><span class="sxs-lookup"><span data-stu-id="3e355-128">Monthly backups count to keep</span></span>

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

### <span data-ttu-id="3e355-129">-Name</span><span class="sxs-lookup"><span data-stu-id="3e355-129">-Name</span></span>
<span data-ttu-id="3e355-130">Az ANF biztonsági mentési házirend neve</span><span class="sxs-lookup"><span data-stu-id="3e355-130">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e355-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e355-131">-ResourceGroupName</span></span>
<span data-ttu-id="3e355-132">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="3e355-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="3e355-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e355-133">-ResourceId</span></span>
<span data-ttu-id="3e355-134">Az ANF biztonsági mentési házirend erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="3e355-134">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="3e355-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="3e355-135">-Tag</span></span>
<span data-ttu-id="3e355-136">A hashtable array which represents resource tags</span><span class="sxs-lookup"><span data-stu-id="3e355-136">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="3e355-137">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="3e355-137">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="3e355-138">Heti biztonsági másolatok száma</span><span class="sxs-lookup"><span data-stu-id="3e355-138">Weekly backups count to keep</span></span>

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

### <span data-ttu-id="3e355-139">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="3e355-139">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="3e355-140">Meg kell tartani az éves biztonsági mentések számát</span><span class="sxs-lookup"><span data-stu-id="3e355-140">Yearly backups count to keep</span></span>

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

### <span data-ttu-id="3e355-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e355-141">-Confirm</span></span>
<span data-ttu-id="3e355-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3e355-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e355-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e355-143">-WhatIf</span></span>
<span data-ttu-id="3e355-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3e355-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e355-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3e355-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e355-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e355-146">CommonParameters</span></span>
<span data-ttu-id="3e355-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e355-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e355-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e355-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e355-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e355-149">INPUTS</span></span>

### <span data-ttu-id="3e355-150">System.String</span><span class="sxs-lookup"><span data-stu-id="3e355-150">System.String</span></span>

### <span data-ttu-id="3e355-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="3e355-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="3e355-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="3e355-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="3e355-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e355-153">OUTPUTS</span></span>

### <span data-ttu-id="3e355-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="3e355-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="3e355-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3e355-155">NOTES</span></span>

## <span data-ttu-id="3e355-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e355-156">RELATED LINKS</span></span>
