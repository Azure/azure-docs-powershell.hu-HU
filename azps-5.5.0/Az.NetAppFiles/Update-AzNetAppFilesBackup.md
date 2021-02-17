---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
ms.openlocfilehash: a2cab03bb88d5b642a95142030eb646b2a5abef4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147195"
---
# <span data-ttu-id="d1e23-101">Update-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="d1e23-101">Update-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="d1e23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1e23-102">SYNOPSIS</span></span>
<span data-ttu-id="d1e23-103">Frissíti az Azure NetApp-fájlok (ANF) biztonsági másolatát a megadott opcionális módosítókkal.</span><span class="sxs-lookup"><span data-stu-id="d1e23-103">Updates an Azure NetApp Files (ANF) backup to the optional modifiers provided.</span></span>

## <span data-ttu-id="d1e23-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d1e23-104">SYNTAX</span></span>

### <span data-ttu-id="d1e23-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d1e23-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolName <String> -VolumeName <String> [-Label <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1e23-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1e23-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup -Name <String> [-Label <String>] [-Tag <Hashtable>]
 -VolumeObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1e23-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1e23-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1e23-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1e23-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesBackup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1e23-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d1e23-109">DESCRIPTION</span></span>
<span data-ttu-id="d1e23-110">Az **Update-AzNetAppFilesBackup** parancsmag módosítja az ANF-biztonsági mentést.</span><span class="sxs-lookup"><span data-stu-id="d1e23-110">The **Update-AzNetAppFilesBackup** cmdlet modifies an ANF backup.</span></span>

## <span data-ttu-id="d1e23-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d1e23-111">EXAMPLES</span></span>

### <span data-ttu-id="d1e23-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="d1e23-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName $accName1 -Name $backupPolicyObject -Label "updatedLabel"
```

<span data-ttu-id="d1e23-113">Ez a parancs frissítést hajt végre a megadott biztonsági másolaton, és módosítja a megadott felhasználónevet.</span><span class="sxs-lookup"><span data-stu-id="d1e23-113">This command performs an update on the given backup modifying the username to that provided.</span></span>

## <span data-ttu-id="d1e23-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1e23-114">PARAMETERS</span></span>

### <span data-ttu-id="d1e23-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d1e23-115">-AccountName</span></span>
<span data-ttu-id="d1e23-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="d1e23-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="d1e23-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1e23-117">-DefaultProfile</span></span>
<span data-ttu-id="d1e23-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d1e23-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1e23-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1e23-119">-InputObject</span></span>
<span data-ttu-id="d1e23-120">Az eltávolítható pillanatkép-objektum</span><span class="sxs-lookup"><span data-stu-id="d1e23-120">The snapshot object to remove</span></span>

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

### <span data-ttu-id="d1e23-121">-Label</span><span class="sxs-lookup"><span data-stu-id="d1e23-121">-Label</span></span>
<span data-ttu-id="d1e23-122">Címke a biztonsági mentéshez</span><span class="sxs-lookup"><span data-stu-id="d1e23-122">Label for backup</span></span>

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

### <span data-ttu-id="d1e23-123">-Location</span><span class="sxs-lookup"><span data-stu-id="d1e23-123">-Location</span></span>
<span data-ttu-id="d1e23-124">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="d1e23-124">The location of the resource</span></span>

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

### <span data-ttu-id="d1e23-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d1e23-125">-Name</span></span>
<span data-ttu-id="d1e23-126">Az ANF biztonsági mentési házirend neve</span><span class="sxs-lookup"><span data-stu-id="d1e23-126">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="d1e23-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="d1e23-127">-PoolName</span></span>
<span data-ttu-id="d1e23-128">Az ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="d1e23-128">The name of the ANF pool</span></span>

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

### <span data-ttu-id="d1e23-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1e23-129">-ResourceGroupName</span></span>
<span data-ttu-id="d1e23-130">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="d1e23-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="d1e23-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1e23-131">-ResourceId</span></span>
<span data-ttu-id="d1e23-132">Az ANF biztonsági másolat erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="d1e23-132">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="d1e23-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="d1e23-133">-Tag</span></span>
<span data-ttu-id="d1e23-134">Erőforráscímkéket képviselő hashtable</span><span class="sxs-lookup"><span data-stu-id="d1e23-134">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="d1e23-135">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="d1e23-135">-VolumeName</span></span>
<span data-ttu-id="d1e23-136">Az ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="d1e23-136">The name of the ANF volume</span></span>

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

### <span data-ttu-id="d1e23-137">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="d1e23-137">-VolumeObject</span></span>
<span data-ttu-id="d1e23-138">A vissza nem térő biztonsági másolatot tartalmazó kötetobjektum</span><span class="sxs-lookup"><span data-stu-id="d1e23-138">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="d1e23-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1e23-139">-Confirm</span></span>
<span data-ttu-id="d1e23-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d1e23-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1e23-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1e23-141">-WhatIf</span></span>
<span data-ttu-id="d1e23-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d1e23-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1e23-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d1e23-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1e23-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1e23-144">CommonParameters</span></span>
<span data-ttu-id="d1e23-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1e23-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1e23-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1e23-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1e23-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d1e23-147">INPUTS</span></span>

### <span data-ttu-id="d1e23-148">System.String</span><span class="sxs-lookup"><span data-stu-id="d1e23-148">System.String</span></span>

### <span data-ttu-id="d1e23-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d1e23-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="d1e23-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="d1e23-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="d1e23-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1e23-151">OUTPUTS</span></span>

### <span data-ttu-id="d1e23-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d1e23-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="d1e23-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d1e23-153">NOTES</span></span>

## <span data-ttu-id="d1e23-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1e23-154">RELATED LINKS</span></span>
