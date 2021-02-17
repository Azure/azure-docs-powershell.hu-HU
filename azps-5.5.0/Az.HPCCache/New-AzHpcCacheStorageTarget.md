---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
ms.openlocfilehash: eee07c01b0c9e0e2b072787d0d37a6a868fbf150
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209375"
---
# <span data-ttu-id="d7d29-101">New-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="d7d29-101">New-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="d7d29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7d29-102">SYNOPSIS</span></span>
<span data-ttu-id="d7d29-103">Tárterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d7d29-103">Creates a Storage Target.</span></span>

## <span data-ttu-id="d7d29-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d7d29-104">SYNTAX</span></span>

### <span data-ttu-id="d7d29-105">ClfsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d7d29-105">ClfsParameterSet (Default)</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-StorageContainerID <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7d29-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7d29-106">NfsParameterSet</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-HostName <String>] [-UsageModel <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7d29-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d7d29-107">DESCRIPTION</span></span>
<span data-ttu-id="d7d29-108">A **New-AzHpcCacheStorageTarget** parancsmag hozzáad egy tárolóhelyet az Azure HPC-gyorsítótárhoz.</span><span class="sxs-lookup"><span data-stu-id="d7d29-108">The **New-AzHpcCacheStorageTarget** cmdlet adds a Storage Target to Azure HPC Cache.</span></span>

## <span data-ttu-id="d7d29-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d7d29-109">EXAMPLES</span></span>

### <span data-ttu-id="d7d29-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="d7d29-110">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -StorageContainerID "/subscriptions/testsub/resourceGroups/testRG/providers/Microsoft.Storage/storageAccounts/testdstorageaccount/blobServices/default/containers/testcontainer" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="d7d29-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="d7d29-111">Example 2</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -UsageModel "READ_HEAVY_INFREQ" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

## <span data-ttu-id="d7d29-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7d29-112">PARAMETERS</span></span>

### <span data-ttu-id="d7d29-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7d29-113">-AsJob</span></span>
<span data-ttu-id="d7d29-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d7d29-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7d29-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="d7d29-115">-CacheName</span></span>
<span data-ttu-id="d7d29-116">A gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="d7d29-116">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d29-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="d7d29-117">-CLFS</span></span>
<span data-ttu-id="d7d29-118">Frissítse a CLFS-tároló céltípusát.</span><span class="sxs-lookup"><span data-stu-id="d7d29-118">Update CLFS Storage Target type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ClfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7d29-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7d29-119">-DefaultProfile</span></span>
<span data-ttu-id="d7d29-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7d29-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7d29-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d7d29-121">-Force</span></span>
<span data-ttu-id="d7d29-122">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d7d29-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="d7d29-123">Ez a parancsmag alapértelmezés szerint megkérdezi, hogy szeretné-e kiüríteni a gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="d7d29-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="d7d29-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="d7d29-124">-HostName</span></span>
<span data-ttu-id="d7d29-125">NFS-állomásnév.</span><span class="sxs-lookup"><span data-stu-id="d7d29-125">NFS host name.</span></span>

```yaml
Type: System.String
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7d29-126">-Junction</span><span class="sxs-lookup"><span data-stu-id="d7d29-126">-Junction</span></span>
<span data-ttu-id="d7d29-127">Junction.</span><span class="sxs-lookup"><span data-stu-id="d7d29-127">Junction.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7d29-128">-Name</span><span class="sxs-lookup"><span data-stu-id="d7d29-128">-Name</span></span>
<span data-ttu-id="d7d29-129">A tárolási cél neve.</span><span class="sxs-lookup"><span data-stu-id="d7d29-129">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageTargetName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d29-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="d7d29-130">-NFS</span></span>
<span data-ttu-id="d7d29-131">Frissítse az NFS-tároló céltípusát.</span><span class="sxs-lookup"><span data-stu-id="d7d29-131">Update NFS Storage Target type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7d29-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7d29-132">-ResourceGroupName</span></span>
<span data-ttu-id="d7d29-133">"Annak az erőforráscsoportnak a neve, amely alatt tárterületet szeretne létrehozni az adott gyorsítótárhoz.</span><span class="sxs-lookup"><span data-stu-id="d7d29-133">"Name of resource group under which you want to create storage target for given cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d29-134">-StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="d7d29-134">-StorageContainerID</span></span>
<span data-ttu-id="d7d29-135">StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="d7d29-135">StorageContainerID</span></span>

```yaml
Type: System.String
Parameter Sets: ClfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7d29-136">-UsageModel</span><span class="sxs-lookup"><span data-stu-id="d7d29-136">-UsageModel</span></span>
<span data-ttu-id="d7d29-137">NFS használati modell.</span><span class="sxs-lookup"><span data-stu-id="d7d29-137">NFS usage model.</span></span>

```yaml
Type: System.String
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7d29-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7d29-138">-Confirm</span></span>
<span data-ttu-id="d7d29-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d7d29-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7d29-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7d29-140">-WhatIf</span></span>
<span data-ttu-id="d7d29-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d7d29-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7d29-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d7d29-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7d29-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7d29-143">CommonParameters</span></span>
<span data-ttu-id="d7d29-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7d29-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7d29-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7d29-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7d29-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7d29-146">INPUTS</span></span>

### <span data-ttu-id="d7d29-147">System.String</span><span class="sxs-lookup"><span data-stu-id="d7d29-147">System.String</span></span>

## <span data-ttu-id="d7d29-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7d29-148">OUTPUTS</span></span>

### <span data-ttu-id="d7d29-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="d7d29-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="d7d29-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d7d29-150">NOTES</span></span>

## <span data-ttu-id="d7d29-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7d29-151">RELATED LINKS</span></span>
