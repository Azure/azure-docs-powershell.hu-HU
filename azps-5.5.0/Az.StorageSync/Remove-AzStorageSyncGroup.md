---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: dad4af4f954fae03a68728de928614a81eed5e5a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156059"
---
# <span data-ttu-id="0a607-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0a607-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="0a607-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a607-102">SYNOPSIS</span></span>
<span data-ttu-id="0a607-103">Ez a parancs törli a megadott szinkronizálási csoportot.</span><span class="sxs-lookup"><span data-stu-id="0a607-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="0a607-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0a607-104">SYNTAX</span></span>

### <span data-ttu-id="0a607-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0a607-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a607-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a607-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a607-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a607-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a607-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0a607-108">DESCRIPTION</span></span>
<span data-ttu-id="0a607-109">Ez a parancs törli a megadott szinkronizálási csoportot.</span><span class="sxs-lookup"><span data-stu-id="0a607-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="0a607-110">A szinkronizálási csoport csak akkor távolítható el, ha először az összes benne lévő végpontot törli.</span><span class="sxs-lookup"><span data-stu-id="0a607-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="0a607-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0a607-111">EXAMPLES</span></span>

### <span data-ttu-id="0a607-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="0a607-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="0a607-113">Ez a parancs eltávolítja a szinkronizálási csoportot.</span><span class="sxs-lookup"><span data-stu-id="0a607-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="0a607-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a607-114">PARAMETERS</span></span>

### <span data-ttu-id="0a607-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a607-115">-AsJob</span></span>
<span data-ttu-id="0a607-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0a607-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a607-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a607-117">-DefaultProfile</span></span>
<span data-ttu-id="0a607-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a607-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a607-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0a607-119">-Force</span></span>
<span data-ttu-id="0a607-120">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="0a607-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="0a607-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a607-121">-InputObject</span></span>
<span data-ttu-id="0a607-122">SyncGroup bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="0a607-122">SyncGroup Input Object</span></span>

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

### <span data-ttu-id="0a607-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0a607-123">-Name</span></span>
<span data-ttu-id="0a607-124">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="0a607-124">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="0a607-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a607-125">-PassThru</span></span>
<span data-ttu-id="0a607-126">Normál végrehajtáskor ez a parancsmag nem ad vissza értéket a sikerhez.</span><span class="sxs-lookup"><span data-stu-id="0a607-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="0a607-127">Ha a PassThru paramétert adja meg, akkor a parancsmag a sikeres végrehajtás után értéket ír a folyamatba.</span><span class="sxs-lookup"><span data-stu-id="0a607-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="0a607-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a607-128">-ResourceGroupName</span></span>
<span data-ttu-id="0a607-129">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0a607-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="0a607-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a607-130">-ResourceId</span></span>
<span data-ttu-id="0a607-131">SyncGroup erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="0a607-131">SyncGroup Resource Id</span></span>

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

### <span data-ttu-id="0a607-132">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="0a607-132">-StorageSyncServiceName</span></span>
<span data-ttu-id="0a607-133">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="0a607-133">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="0a607-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a607-134">-Confirm</span></span>
<span data-ttu-id="0a607-135">A parancsmag futtatása előtt megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0a607-135">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a607-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a607-136">-WhatIf</span></span>
<span data-ttu-id="0a607-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0a607-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a607-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0a607-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a607-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a607-139">CommonParameters</span></span>
<span data-ttu-id="0a607-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a607-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a607-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a607-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a607-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a607-142">INPUTS</span></span>

### <span data-ttu-id="0a607-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0a607-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="0a607-144">System.String</span><span class="sxs-lookup"><span data-stu-id="0a607-144">System.String</span></span>

### <span data-ttu-id="0a607-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0a607-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0a607-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a607-146">OUTPUTS</span></span>

### <span data-ttu-id="0a607-147">System.Object</span><span class="sxs-lookup"><span data-stu-id="0a607-147">System.Object</span></span>
## <span data-ttu-id="0a607-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0a607-148">NOTES</span></span>

## <span data-ttu-id="0a607-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a607-149">RELATED LINKS</span></span>
