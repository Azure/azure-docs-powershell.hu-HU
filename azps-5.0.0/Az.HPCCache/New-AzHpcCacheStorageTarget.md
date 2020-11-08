---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
ms.openlocfilehash: eee07c01b0c9e0e2b072787d0d37a6a868fbf150
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187810"
---
# <span data-ttu-id="36558-101">New-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="36558-101">New-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="36558-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36558-102">SYNOPSIS</span></span>
<span data-ttu-id="36558-103">Tároló tárolót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="36558-103">Creates a Storage Target.</span></span>

## <span data-ttu-id="36558-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36558-104">SYNTAX</span></span>

### <span data-ttu-id="36558-105">ClfsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="36558-105">ClfsParameterSet (Default)</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-StorageContainerID <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36558-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="36558-106">NfsParameterSet</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-HostName <String>] [-UsageModel <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36558-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="36558-107">DESCRIPTION</span></span>
<span data-ttu-id="36558-108">A **New-AzHpcCacheStorageTarget** parancsmag az Azure HPC-gyorsítótárba helyezi a tárterület-tárolót.</span><span class="sxs-lookup"><span data-stu-id="36558-108">The **New-AzHpcCacheStorageTarget** cmdlet adds a Storage Target to Azure HPC Cache.</span></span>

## <span data-ttu-id="36558-109">Példák</span><span class="sxs-lookup"><span data-stu-id="36558-109">EXAMPLES</span></span>

### <span data-ttu-id="36558-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="36558-110">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -StorageContainerID "/subscriptions/testsub/resourceGroups/testRG/providers/Microsoft.Storage/storageAccounts/testdstorageaccount/blobServices/default/containers/testcontainer" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="36558-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="36558-111">Example 2</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -UsageModel "READ_HEAVY_INFREQ" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

## <span data-ttu-id="36558-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36558-112">PARAMETERS</span></span>

### <span data-ttu-id="36558-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36558-113">-AsJob</span></span>
<span data-ttu-id="36558-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="36558-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36558-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="36558-115">-CacheName</span></span>
<span data-ttu-id="36558-116">A gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="36558-116">Name of cache.</span></span>

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

### <span data-ttu-id="36558-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="36558-117">-CLFS</span></span>
<span data-ttu-id="36558-118">Frissítse a CLFS-tárterület típusát.</span><span class="sxs-lookup"><span data-stu-id="36558-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="36558-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36558-119">-DefaultProfile</span></span>
<span data-ttu-id="36558-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36558-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36558-121">-Force</span><span class="sxs-lookup"><span data-stu-id="36558-121">-Force</span></span>
<span data-ttu-id="36558-122">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="36558-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="36558-123">Ez a parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, hogy szeretné-e kiüríteni a gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="36558-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="36558-124">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="36558-124">-HostName</span></span>
<span data-ttu-id="36558-125">Az NFS-állomás neve.</span><span class="sxs-lookup"><span data-stu-id="36558-125">NFS host name.</span></span>

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

### <span data-ttu-id="36558-126">-Elágazás</span><span class="sxs-lookup"><span data-stu-id="36558-126">-Junction</span></span>
<span data-ttu-id="36558-127">Junction.</span><span class="sxs-lookup"><span data-stu-id="36558-127">Junction.</span></span>

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

### <span data-ttu-id="36558-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="36558-128">-Name</span></span>
<span data-ttu-id="36558-129">A tárolási cél neve</span><span class="sxs-lookup"><span data-stu-id="36558-129">Name of storage target.</span></span>

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

### <span data-ttu-id="36558-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="36558-130">-NFS</span></span>
<span data-ttu-id="36558-131">Módosítsa az NFS-tárterület-tároló típusát.</span><span class="sxs-lookup"><span data-stu-id="36558-131">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="36558-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36558-132">-ResourceGroupName</span></span>
<span data-ttu-id="36558-133">"Az erőforráscsoport neve, amely alatt tárterületet szeretne létrehozni az adott gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="36558-133">"Name of resource group under which you want to create storage target for given cache.</span></span>

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

### <span data-ttu-id="36558-134">-StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="36558-134">-StorageContainerID</span></span>
<span data-ttu-id="36558-135">StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="36558-135">StorageContainerID</span></span>

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

### <span data-ttu-id="36558-136">-UsageModel</span><span class="sxs-lookup"><span data-stu-id="36558-136">-UsageModel</span></span>
<span data-ttu-id="36558-137">NFS-használati modell</span><span class="sxs-lookup"><span data-stu-id="36558-137">NFS usage model.</span></span>

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

### <span data-ttu-id="36558-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="36558-138">-Confirm</span></span>
<span data-ttu-id="36558-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="36558-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36558-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36558-140">-WhatIf</span></span>
<span data-ttu-id="36558-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="36558-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36558-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36558-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36558-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36558-143">CommonParameters</span></span>
<span data-ttu-id="36558-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36558-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36558-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="36558-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36558-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36558-146">INPUTS</span></span>

### <span data-ttu-id="36558-147">System. String</span><span class="sxs-lookup"><span data-stu-id="36558-147">System.String</span></span>

## <span data-ttu-id="36558-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36558-148">OUTPUTS</span></span>

### <span data-ttu-id="36558-149">Microsoft. Azure. PowerShell. parancsmagok. HPCCache. models. PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="36558-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="36558-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36558-150">NOTES</span></span>

## <span data-ttu-id="36558-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36558-151">RELATED LINKS</span></span>
