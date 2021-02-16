---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
ms.openlocfilehash: fa799a05b76f9f6941b19bf171beb77318b77d39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163506"
---
# <span data-ttu-id="7519f-101">Set-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="7519f-101">Set-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="7519f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7519f-102">SYNOPSIS</span></span>
<span data-ttu-id="7519f-103">Frissíti a tárterület célhelyét.</span><span class="sxs-lookup"><span data-stu-id="7519f-103">Updates a Storage Target.</span></span>

## <span data-ttu-id="7519f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7519f-104">SYNTAX</span></span>

### <span data-ttu-id="7519f-105">ClfsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7519f-105">ClfsParameterSet (Default)</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7519f-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="7519f-106">NfsParameterSet</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7519f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7519f-107">DESCRIPTION</span></span>
<span data-ttu-id="7519f-108">A **Set-AzHpcCacheStorageTarget** parancsmag frissíti az Azure HPC-gyorsítótárhoz csatlakoztatott tárolóhelyet.</span><span class="sxs-lookup"><span data-stu-id="7519f-108">The **Set-AzHpcCacheStorageTarget** cmdlet updates a Storage Target attached to Azure HPC cache.</span></span>

## <span data-ttu-id="7519f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7519f-109">EXAMPLES</span></span>

### <span data-ttu-id="7519f-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="7519f-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="7519f-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="7519f-111">Example 2</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/export"})
```

## <span data-ttu-id="7519f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7519f-112">PARAMETERS</span></span>

### <span data-ttu-id="7519f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7519f-113">-AsJob</span></span>
<span data-ttu-id="7519f-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7519f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7519f-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="7519f-115">-CacheName</span></span>
<span data-ttu-id="7519f-116">A gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="7519f-116">Name of cache.</span></span>

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

### <span data-ttu-id="7519f-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="7519f-117">-CLFS</span></span>
<span data-ttu-id="7519f-118">Frissítse a CLFS-tároló céltípusát.</span><span class="sxs-lookup"><span data-stu-id="7519f-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="7519f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7519f-119">-DefaultProfile</span></span>
<span data-ttu-id="7519f-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7519f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7519f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7519f-121">-Force</span></span>
<span data-ttu-id="7519f-122">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7519f-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="7519f-123">Ez a parancsmag alapértelmezés szerint megkérdezi, hogy szeretné-e kiüríteni a gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="7519f-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="7519f-124">-Junction</span><span class="sxs-lookup"><span data-stu-id="7519f-124">-Junction</span></span>
<span data-ttu-id="7519f-125">Junction.</span><span class="sxs-lookup"><span data-stu-id="7519f-125">Junction.</span></span>

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

### <span data-ttu-id="7519f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="7519f-126">-Name</span></span>
<span data-ttu-id="7519f-127">A tárolási cél neve.</span><span class="sxs-lookup"><span data-stu-id="7519f-127">Name of storage target.</span></span>

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

### <span data-ttu-id="7519f-128">-NFS</span><span class="sxs-lookup"><span data-stu-id="7519f-128">-NFS</span></span>
<span data-ttu-id="7519f-129">Frissítse az NFS-tároló céltípusát.</span><span class="sxs-lookup"><span data-stu-id="7519f-129">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="7519f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7519f-130">-ResourceGroupName</span></span>
<span data-ttu-id="7519f-131">Annak az erőforráscsoportnak a neve, amely alatt frissíteni szeretné a tárterület célhelyét.</span><span class="sxs-lookup"><span data-stu-id="7519f-131">Name of resource group under which you want to update storage target.</span></span>

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

### <span data-ttu-id="7519f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7519f-132">-Confirm</span></span>
<span data-ttu-id="7519f-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7519f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7519f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7519f-134">-WhatIf</span></span>
<span data-ttu-id="7519f-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7519f-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7519f-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7519f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7519f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7519f-137">CommonParameters</span></span>
<span data-ttu-id="7519f-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7519f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7519f-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7519f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7519f-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7519f-140">INPUTS</span></span>

### <span data-ttu-id="7519f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="7519f-141">System.String</span></span>

## <span data-ttu-id="7519f-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7519f-142">OUTPUTS</span></span>

### <span data-ttu-id="7519f-143">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="7519f-143">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="7519f-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7519f-144">NOTES</span></span>

## <span data-ttu-id="7519f-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7519f-145">RELATED LINKS</span></span>
