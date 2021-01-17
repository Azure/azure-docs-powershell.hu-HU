---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: dad4af4f954fae03a68728de928614a81eed5e5a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466849"
---
# <span data-ttu-id="e6f12-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e6f12-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="e6f12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6f12-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f12-103">Ez a parancs törli a megadott szinkronizálási csoportot.</span><span class="sxs-lookup"><span data-stu-id="e6f12-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="e6f12-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e6f12-104">SYNTAX</span></span>

### <span data-ttu-id="e6f12-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e6f12-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6f12-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6f12-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6f12-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6f12-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6f12-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e6f12-108">DESCRIPTION</span></span>
<span data-ttu-id="e6f12-109">Ez a parancs törli a megadott szinkronizálási csoportot.</span><span class="sxs-lookup"><span data-stu-id="e6f12-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="e6f12-110">A szinkronizálási csoport csak akkor távolítható el, ha először az összes benne lévő végpontot törli.</span><span class="sxs-lookup"><span data-stu-id="e6f12-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="e6f12-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e6f12-111">EXAMPLES</span></span>

### <span data-ttu-id="e6f12-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="e6f12-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="e6f12-113">Ez a parancs eltávolítja a szinkronizálási csoportot.</span><span class="sxs-lookup"><span data-stu-id="e6f12-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="e6f12-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6f12-114">PARAMETERS</span></span>

### <span data-ttu-id="e6f12-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6f12-115">-AsJob</span></span>
<span data-ttu-id="e6f12-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e6f12-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6f12-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6f12-117">-DefaultProfile</span></span>
<span data-ttu-id="e6f12-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6f12-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6f12-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e6f12-119">-Force</span></span>
<span data-ttu-id="e6f12-120">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="e6f12-120">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6f12-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6f12-121">-InputObject</span></span>
<span data-ttu-id="e6f12-122">SyncGroup bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="e6f12-122">SyncGroup Input Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6f12-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e6f12-123">-Name</span></span>
<span data-ttu-id="e6f12-124">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="e6f12-124">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: SyncGroupName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f12-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6f12-125">-PassThru</span></span>
<span data-ttu-id="e6f12-126">Normál végrehajtáskor ez a parancsmag nem ad vissza értéket a sikerhez.</span><span class="sxs-lookup"><span data-stu-id="e6f12-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="e6f12-127">Ha a PassThru paramétert adja meg, akkor a parancsmag a sikeres végrehajtás után értéket ír a folyamatba.</span><span class="sxs-lookup"><span data-stu-id="e6f12-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="e6f12-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6f12-128">-ResourceGroupName</span></span>
<span data-ttu-id="e6f12-129">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e6f12-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f12-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6f12-130">-ResourceId</span></span>
<span data-ttu-id="e6f12-131">SyncGroup Resource Id</span><span class="sxs-lookup"><span data-stu-id="e6f12-131">SyncGroup Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6f12-132">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="e6f12-132">-StorageSyncServiceName</span></span>
<span data-ttu-id="e6f12-133">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="e6f12-133">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f12-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6f12-134">-Confirm</span></span>
<span data-ttu-id="e6f12-135">A parancsmag futtatása előtt megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e6f12-135">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6f12-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6f12-136">-WhatIf</span></span>
<span data-ttu-id="e6f12-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e6f12-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6f12-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e6f12-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6f12-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f12-139">CommonParameters</span></span>
<span data-ttu-id="e6f12-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6f12-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f12-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6f12-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f12-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6f12-142">INPUTS</span></span>

### <span data-ttu-id="e6f12-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e6f12-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="e6f12-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e6f12-144">System.String</span></span>

### <span data-ttu-id="e6f12-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e6f12-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e6f12-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6f12-146">OUTPUTS</span></span>

### <span data-ttu-id="e6f12-147">System.Object</span><span class="sxs-lookup"><span data-stu-id="e6f12-147">System.Object</span></span>
## <span data-ttu-id="e6f12-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e6f12-148">NOTES</span></span>

## <span data-ttu-id="e6f12-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6f12-149">RELATED LINKS</span></span>
