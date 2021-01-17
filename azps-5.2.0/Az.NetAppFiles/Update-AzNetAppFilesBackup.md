---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
ms.openlocfilehash: a2cab03bb88d5b642a95142030eb646b2a5abef4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335298"
---
# <span data-ttu-id="1ada9-101">Update-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="1ada9-101">Update-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="1ada9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ada9-102">SYNOPSIS</span></span>
<span data-ttu-id="1ada9-103">Frissíti az Azure NetApp-fájlok (ANF) biztonsági másolatát a megadott opcionális módosítókkal.</span><span class="sxs-lookup"><span data-stu-id="1ada9-103">Updates an Azure NetApp Files (ANF) backup to the optional modifiers provided.</span></span>

## <span data-ttu-id="1ada9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1ada9-104">SYNTAX</span></span>

### <span data-ttu-id="1ada9-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ada9-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolName <String> -VolumeName <String> [-Label <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ada9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ada9-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup -Name <String> [-Label <String>] [-Tag <Hashtable>]
 -VolumeObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1ada9-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ada9-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ada9-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ada9-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesBackup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ada9-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1ada9-109">DESCRIPTION</span></span>
<span data-ttu-id="1ada9-110">Az **Update-AzNetAppFilesBackup** parancsmag módosítja az ANF-biztonsági mentést.</span><span class="sxs-lookup"><span data-stu-id="1ada9-110">The **Update-AzNetAppFilesBackup** cmdlet modifies an ANF backup.</span></span>

## <span data-ttu-id="1ada9-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1ada9-111">EXAMPLES</span></span>

### <span data-ttu-id="1ada9-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="1ada9-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName $accName1 -Name $backupPolicyObject -Label "updatedLabel"
```

<span data-ttu-id="1ada9-113">Ez a parancs frissítést hajt végre a megadott biztonsági másolaton, és módosítja a megadott felhasználónevet.</span><span class="sxs-lookup"><span data-stu-id="1ada9-113">This command performs an update on the given backup modifying the username to that provided.</span></span>

## <span data-ttu-id="1ada9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ada9-114">PARAMETERS</span></span>

### <span data-ttu-id="1ada9-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1ada9-115">-AccountName</span></span>
<span data-ttu-id="1ada9-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="1ada9-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="1ada9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ada9-117">-DefaultProfile</span></span>
<span data-ttu-id="1ada9-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ada9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ada9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ada9-119">-InputObject</span></span>
<span data-ttu-id="1ada9-120">Az eltávolítható pillanatkép-objektum</span><span class="sxs-lookup"><span data-stu-id="1ada9-120">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ada9-121">-Label</span><span class="sxs-lookup"><span data-stu-id="1ada9-121">-Label</span></span>
<span data-ttu-id="1ada9-122">Címke a biztonsági mentéshez</span><span class="sxs-lookup"><span data-stu-id="1ada9-122">Label for backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ada9-123">-Location</span><span class="sxs-lookup"><span data-stu-id="1ada9-123">-Location</span></span>
<span data-ttu-id="1ada9-124">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="1ada9-124">The location of the resource</span></span>

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

### <span data-ttu-id="1ada9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1ada9-125">-Name</span></span>
<span data-ttu-id="1ada9-126">Az ANF biztonsági mentési házirend neve</span><span class="sxs-lookup"><span data-stu-id="1ada9-126">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="1ada9-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="1ada9-127">-PoolName</span></span>
<span data-ttu-id="1ada9-128">Az ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="1ada9-128">The name of the ANF pool</span></span>

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

### <span data-ttu-id="1ada9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ada9-129">-ResourceGroupName</span></span>
<span data-ttu-id="1ada9-130">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="1ada9-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="1ada9-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ada9-131">-ResourceId</span></span>
<span data-ttu-id="1ada9-132">Az ANF biztonsági másolat erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="1ada9-132">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="1ada9-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="1ada9-133">-Tag</span></span>
<span data-ttu-id="1ada9-134">Erőforráscímkéket képviselő hashtable</span><span class="sxs-lookup"><span data-stu-id="1ada9-134">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="1ada9-135">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="1ada9-135">-VolumeName</span></span>
<span data-ttu-id="1ada9-136">Az ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="1ada9-136">The name of the ANF volume</span></span>

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

### <span data-ttu-id="1ada9-137">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="1ada9-137">-VolumeObject</span></span>
<span data-ttu-id="1ada9-138">A vissza nem térő biztonsági másolatot tartalmazó kötetobjektum</span><span class="sxs-lookup"><span data-stu-id="1ada9-138">The volume object containing the backup to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ada9-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ada9-139">-Confirm</span></span>
<span data-ttu-id="1ada9-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1ada9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ada9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ada9-141">-WhatIf</span></span>
<span data-ttu-id="1ada9-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1ada9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ada9-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1ada9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ada9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ada9-144">CommonParameters</span></span>
<span data-ttu-id="1ada9-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ada9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ada9-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ada9-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ada9-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ada9-147">INPUTS</span></span>

### <span data-ttu-id="1ada9-148">System.String</span><span class="sxs-lookup"><span data-stu-id="1ada9-148">System.String</span></span>

### <span data-ttu-id="1ada9-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="1ada9-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="1ada9-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="1ada9-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="1ada9-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ada9-151">OUTPUTS</span></span>

### <span data-ttu-id="1ada9-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="1ada9-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="1ada9-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1ada9-153">NOTES</span></span>

## <span data-ttu-id="1ada9-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ada9-154">RELATED LINKS</span></span>
