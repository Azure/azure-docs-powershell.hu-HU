---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
ms.openlocfilehash: 34b4e43dcd09df600c73a6dd0a459a41b491da3d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385655"
---
# <span data-ttu-id="7465c-101">Remove-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="7465c-101">Remove-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="7465c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7465c-102">SYNOPSIS</span></span>
<span data-ttu-id="7465c-103">Egy Azure NetApp-fájl (ANF) biztonsági másolatának törlése.</span><span class="sxs-lookup"><span data-stu-id="7465c-103">Deletes an Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="7465c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7465c-104">SYNTAX</span></span>

### <span data-ttu-id="7465c-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7465c-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackup -ResourceGroupName <String> [-AccountName <String>] -PoolName <String>
 [-VolumeName <String>] -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7465c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7465c-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -Name <String> -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7465c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7465c-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7465c-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7465c-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -InputObject <PSNetAppFilesBackup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7465c-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7465c-109">DESCRIPTION</span></span>
<span data-ttu-id="7465c-110">A **Remove-AzNetAppFilesBackup** parancsmag töröl egy ANF-fiókot.</span><span class="sxs-lookup"><span data-stu-id="7465c-110">The **Remove-AzNetAppFilesBackup** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="7465c-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7465c-111">EXAMPLES</span></span>

### <span data-ttu-id="7465c-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="7465c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="7465c-113">Ez a parancs törli az új ANF biztonsági másolatot a MyVolume kötet "MyBackup" nevével.</span><span class="sxs-lookup"><span data-stu-id="7465c-113">This command deletes the new ANF backup with a the name "MyBackup" for volume "MyVolume".</span></span>

## <span data-ttu-id="7465c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7465c-114">PARAMETERS</span></span>

### <span data-ttu-id="7465c-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7465c-115">-AccountName</span></span>
<span data-ttu-id="7465c-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="7465c-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7465c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7465c-117">-DefaultProfile</span></span>
<span data-ttu-id="7465c-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7465c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7465c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7465c-119">-InputObject</span></span>
<span data-ttu-id="7465c-120">Az eltávolítható pillanatkép-objektum</span><span class="sxs-lookup"><span data-stu-id="7465c-120">The snapshot object to remove</span></span>

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

### <span data-ttu-id="7465c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7465c-121">-Name</span></span>
<span data-ttu-id="7465c-122">Az ANF biztonsági másolat neve</span><span class="sxs-lookup"><span data-stu-id="7465c-122">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7465c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7465c-123">-PassThru</span></span>
<span data-ttu-id="7465c-124">Annak visszaadése, hogy a megadott biztonsági mentés sikeresen el lett-e távolítva</span><span class="sxs-lookup"><span data-stu-id="7465c-124">Return whether the specified backup was successfully removed</span></span>

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

### <span data-ttu-id="7465c-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="7465c-125">-PoolName</span></span>
<span data-ttu-id="7465c-126">Az ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="7465c-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="7465c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7465c-127">-ResourceGroupName</span></span>
<span data-ttu-id="7465c-128">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="7465c-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="7465c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7465c-129">-ResourceId</span></span>
<span data-ttu-id="7465c-130">Az ANF biztonsági másolat erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="7465c-130">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="7465c-131">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="7465c-131">-VolumeName</span></span>
<span data-ttu-id="7465c-132">Az ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="7465c-132">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7465c-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="7465c-133">-VolumeObject</span></span>
<span data-ttu-id="7465c-134">A vissza nem térő biztonsági másolatot tartalmazó kötetobjektum</span><span class="sxs-lookup"><span data-stu-id="7465c-134">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="7465c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7465c-135">-Confirm</span></span>
<span data-ttu-id="7465c-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7465c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7465c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7465c-137">-WhatIf</span></span>
<span data-ttu-id="7465c-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7465c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7465c-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7465c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7465c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7465c-140">CommonParameters</span></span>
<span data-ttu-id="7465c-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7465c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7465c-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7465c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7465c-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7465c-143">INPUTS</span></span>

### <span data-ttu-id="7465c-144">System.String</span><span class="sxs-lookup"><span data-stu-id="7465c-144">System.String</span></span>

### <span data-ttu-id="7465c-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="7465c-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="7465c-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="7465c-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="7465c-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7465c-147">OUTPUTS</span></span>

### <span data-ttu-id="7465c-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="7465c-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="7465c-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7465c-149">NOTES</span></span>

## <span data-ttu-id="7465c-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7465c-150">RELATED LINKS</span></span>
