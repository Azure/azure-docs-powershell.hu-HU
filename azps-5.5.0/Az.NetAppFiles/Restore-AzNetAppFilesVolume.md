---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/restore-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
ms.openlocfilehash: 6606de1a5d4de6df6ecafa700ac1b93d31399b43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203293"
---
# <span data-ttu-id="c1f42-101">Restore-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c1f42-101">Restore-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="c1f42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1f42-102">SYNOPSIS</span></span>
<span data-ttu-id="c1f42-103">Hangerő visszaállítása/visszaállítása annak pillanatképei egyikére</span><span class="sxs-lookup"><span data-stu-id="c1f42-103">Restore/Revert a volume to one of its snapshots</span></span>

## <span data-ttu-id="c1f42-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c1f42-104">SYNTAX</span></span>

### <span data-ttu-id="c1f42-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c1f42-105">ByFieldsParameterSet (Default)</span></span>
```
Restore-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-SnapshotId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1f42-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1f42-106">ByParentObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1f42-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1f42-107">ByResourceIdParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1f42-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1f42-108">ByObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1f42-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c1f42-109">DESCRIPTION</span></span>
<span data-ttu-id="c1f42-110">Kötet visszaállítása/visszaállítása a SnapshotId paraméterben megadott pillanatképre</span><span class="sxs-lookup"><span data-stu-id="c1f42-110">Restore/Revert a volume to the snapshot specified in the SnapshotId paramter</span></span>

## <span data-ttu-id="c1f42-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c1f42-111">EXAMPLES</span></span>

### <span data-ttu-id="c1f42-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="c1f42-112">Example 1</span></span>
```powershell
PS C:\> Restore-AzNetAppFilesVolume -ResourceGroupName "MyRG" -Location "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -SnapshotId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="c1f42-113">Ez a parancs visszaállítja/visszaállítja a MyVolume kötetet annak egyik pillanatfelvételére a 7d6e4069-6c78-6c61-7bf6-c60968e45fbf pillanatkép-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="c1f42-113">This command Restores/Reverts the volume MyVolume to one of its snapshots with the snapshotId of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="c1f42-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1f42-114">PARAMETERS</span></span>

### <span data-ttu-id="c1f42-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c1f42-115">-AccountName</span></span>
<span data-ttu-id="c1f42-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="c1f42-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="c1f42-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1f42-117">-DefaultProfile</span></span>
<span data-ttu-id="c1f42-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1f42-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1f42-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1f42-119">-InputObject</span></span>
<span data-ttu-id="c1f42-120">Az eltávolítható kötetobjektum</span><span class="sxs-lookup"><span data-stu-id="c1f42-120">The volume object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1f42-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c1f42-121">-Name</span></span>
<span data-ttu-id="c1f42-122">Az ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="c1f42-122">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1f42-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1f42-123">-PassThru</span></span>
<span data-ttu-id="c1f42-124">Visszaadja, hogy a megadott kötet visszaállítása/visszaállítása sikeresen megtörtént-e</span><span class="sxs-lookup"><span data-stu-id="c1f42-124">Return whether the specified volume was successfully restored/reverted</span></span>

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

### <span data-ttu-id="c1f42-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="c1f42-125">-PoolName</span></span>
<span data-ttu-id="c1f42-126">Az ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="c1f42-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="c1f42-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="c1f42-127">-PoolObject</span></span>
<span data-ttu-id="c1f42-128">Az eltávolítható hangerőt tartalmazó készletobjektum</span><span class="sxs-lookup"><span data-stu-id="c1f42-128">The pool object containing the volume to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1f42-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1f42-129">-ResourceGroupName</span></span>
<span data-ttu-id="c1f42-130">Az ANF-mennyiség erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="c1f42-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="c1f42-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1f42-131">-ResourceId</span></span>
<span data-ttu-id="c1f42-132">Az ANF-mennyiség erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="c1f42-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="c1f42-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="c1f42-133">-SnapshotId</span></span>
<span data-ttu-id="c1f42-134">SnapshotId of the snapshot.</span><span class="sxs-lookup"><span data-stu-id="c1f42-134">SnapshotId of the snapshot.</span></span>
<span data-ttu-id="c1f42-135">A pillanatkép azonosítására használt UUID v4</span><span class="sxs-lookup"><span data-stu-id="c1f42-135">UUID v4 used to identify the Snapshot</span></span>

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

### <span data-ttu-id="c1f42-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1f42-136">-Confirm</span></span>
<span data-ttu-id="c1f42-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c1f42-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1f42-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1f42-138">-WhatIf</span></span>
<span data-ttu-id="c1f42-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c1f42-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1f42-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c1f42-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1f42-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1f42-141">CommonParameters</span></span>
<span data-ttu-id="c1f42-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1f42-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1f42-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1f42-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1f42-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1f42-144">INPUTS</span></span>

### <span data-ttu-id="c1f42-145">System.String</span><span class="sxs-lookup"><span data-stu-id="c1f42-145">System.String</span></span>

### <span data-ttu-id="c1f42-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="c1f42-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="c1f42-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c1f42-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="c1f42-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1f42-148">OUTPUTS</span></span>

### <span data-ttu-id="c1f42-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c1f42-149">System.Boolean</span></span>

## <span data-ttu-id="c1f42-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c1f42-150">NOTES</span></span>

## <span data-ttu-id="c1f42-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1f42-151">RELATED LINKS</span></span>
