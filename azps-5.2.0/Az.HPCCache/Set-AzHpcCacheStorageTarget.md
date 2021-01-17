---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
ms.openlocfilehash: fa799a05b76f9f6941b19bf171beb77318b77d39
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345965"
---
# <span data-ttu-id="43a33-101">Set-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="43a33-101">Set-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="43a33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43a33-102">SYNOPSIS</span></span>
<span data-ttu-id="43a33-103">Frissíti a tárterület célhelyét.</span><span class="sxs-lookup"><span data-stu-id="43a33-103">Updates a Storage Target.</span></span>

## <span data-ttu-id="43a33-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="43a33-104">SYNTAX</span></span>

### <span data-ttu-id="43a33-105">ClfsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="43a33-105">ClfsParameterSet (Default)</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43a33-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="43a33-106">NfsParameterSet</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43a33-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="43a33-107">DESCRIPTION</span></span>
<span data-ttu-id="43a33-108">A **Set-AzHpcCacheStorageTarget** parancsmag frissíti az Azure HPC-gyorsítótárhoz csatlakoztatott tárolóhelyet.</span><span class="sxs-lookup"><span data-stu-id="43a33-108">The **Set-AzHpcCacheStorageTarget** cmdlet updates a Storage Target attached to Azure HPC cache.</span></span>

## <span data-ttu-id="43a33-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="43a33-109">EXAMPLES</span></span>

### <span data-ttu-id="43a33-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="43a33-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="43a33-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="43a33-111">Example 2</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/export"})
```

## <span data-ttu-id="43a33-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43a33-112">PARAMETERS</span></span>

### <span data-ttu-id="43a33-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43a33-113">-AsJob</span></span>
<span data-ttu-id="43a33-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="43a33-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43a33-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="43a33-115">-CacheName</span></span>
<span data-ttu-id="43a33-116">A gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="43a33-116">Name of cache.</span></span>

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

### <span data-ttu-id="43a33-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="43a33-117">-CLFS</span></span>
<span data-ttu-id="43a33-118">Frissítse a CLFS-tároló céltípusát.</span><span class="sxs-lookup"><span data-stu-id="43a33-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="43a33-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43a33-119">-DefaultProfile</span></span>
<span data-ttu-id="43a33-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43a33-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43a33-121">-Force</span><span class="sxs-lookup"><span data-stu-id="43a33-121">-Force</span></span>
<span data-ttu-id="43a33-122">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="43a33-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="43a33-123">Ez a parancsmag alapértelmezés szerint megkérdezi, hogy szeretné-e kiüríteni a gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="43a33-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="43a33-124">-Junction</span><span class="sxs-lookup"><span data-stu-id="43a33-124">-Junction</span></span>
<span data-ttu-id="43a33-125">Junction.</span><span class="sxs-lookup"><span data-stu-id="43a33-125">Junction.</span></span>

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

### <span data-ttu-id="43a33-126">-Name</span><span class="sxs-lookup"><span data-stu-id="43a33-126">-Name</span></span>
<span data-ttu-id="43a33-127">A tárolási cél neve.</span><span class="sxs-lookup"><span data-stu-id="43a33-127">Name of storage target.</span></span>

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

### <span data-ttu-id="43a33-128">-NFS</span><span class="sxs-lookup"><span data-stu-id="43a33-128">-NFS</span></span>
<span data-ttu-id="43a33-129">Frissítse az NFS-tároló céltípusát.</span><span class="sxs-lookup"><span data-stu-id="43a33-129">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="43a33-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43a33-130">-ResourceGroupName</span></span>
<span data-ttu-id="43a33-131">Annak az erőforráscsoportnak a neve, amely alatt frissíteni szeretné a tárterület célhelyét.</span><span class="sxs-lookup"><span data-stu-id="43a33-131">Name of resource group under which you want to update storage target.</span></span>

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

### <span data-ttu-id="43a33-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43a33-132">-Confirm</span></span>
<span data-ttu-id="43a33-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="43a33-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43a33-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43a33-134">-WhatIf</span></span>
<span data-ttu-id="43a33-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="43a33-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43a33-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43a33-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43a33-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43a33-137">CommonParameters</span></span>
<span data-ttu-id="43a33-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43a33-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43a33-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43a33-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43a33-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43a33-140">INPUTS</span></span>

### <span data-ttu-id="43a33-141">System.String</span><span class="sxs-lookup"><span data-stu-id="43a33-141">System.String</span></span>

## <span data-ttu-id="43a33-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43a33-142">OUTPUTS</span></span>

### <span data-ttu-id="43a33-143">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="43a33-143">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="43a33-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="43a33-144">NOTES</span></span>

## <span data-ttu-id="43a33-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43a33-145">RELATED LINKS</span></span>
