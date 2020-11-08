---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
ms.openlocfilehash: fa799a05b76f9f6941b19bf171beb77318b77d39
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017733"
---
# <span data-ttu-id="a312f-101">Set-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="a312f-101">Set-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="a312f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a312f-102">SYNOPSIS</span></span>
<span data-ttu-id="a312f-103">Tárterület-tároló frissítése</span><span class="sxs-lookup"><span data-stu-id="a312f-103">Updates a Storage Target.</span></span>

## <span data-ttu-id="a312f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a312f-104">SYNTAX</span></span>

### <span data-ttu-id="a312f-105">ClfsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a312f-105">ClfsParameterSet (Default)</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a312f-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="a312f-106">NfsParameterSet</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a312f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a312f-107">DESCRIPTION</span></span>
<span data-ttu-id="a312f-108">A **set-AzHpcCacheStorageTarget** parancsmag az Azure HPC-gyorsítótárhoz csatolt tárterület-tárolóra frissít.</span><span class="sxs-lookup"><span data-stu-id="a312f-108">The **Set-AzHpcCacheStorageTarget** cmdlet updates a Storage Target attached to Azure HPC cache.</span></span>

## <span data-ttu-id="a312f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a312f-109">EXAMPLES</span></span>

### <span data-ttu-id="a312f-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a312f-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="a312f-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="a312f-111">Example 2</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/export"})
```

## <span data-ttu-id="a312f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a312f-112">PARAMETERS</span></span>

### <span data-ttu-id="a312f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a312f-113">-AsJob</span></span>
<span data-ttu-id="a312f-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a312f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a312f-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="a312f-115">-CacheName</span></span>
<span data-ttu-id="a312f-116">A gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="a312f-116">Name of cache.</span></span>

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

### <span data-ttu-id="a312f-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="a312f-117">-CLFS</span></span>
<span data-ttu-id="a312f-118">Frissítse a CLFS-tárterület típusát.</span><span class="sxs-lookup"><span data-stu-id="a312f-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="a312f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a312f-119">-DefaultProfile</span></span>
<span data-ttu-id="a312f-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a312f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a312f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a312f-121">-Force</span></span>
<span data-ttu-id="a312f-122">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a312f-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="a312f-123">Ez a parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, hogy szeretné-e kiüríteni a gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="a312f-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="a312f-124">-Elágazás</span><span class="sxs-lookup"><span data-stu-id="a312f-124">-Junction</span></span>
<span data-ttu-id="a312f-125">Junction.</span><span class="sxs-lookup"><span data-stu-id="a312f-125">Junction.</span></span>

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

### <span data-ttu-id="a312f-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a312f-126">-Name</span></span>
<span data-ttu-id="a312f-127">A tárolási cél neve</span><span class="sxs-lookup"><span data-stu-id="a312f-127">Name of storage target.</span></span>

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

### <span data-ttu-id="a312f-128">-NFS</span><span class="sxs-lookup"><span data-stu-id="a312f-128">-NFS</span></span>
<span data-ttu-id="a312f-129">Módosítsa az NFS-tárterület-tároló típusát.</span><span class="sxs-lookup"><span data-stu-id="a312f-129">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="a312f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a312f-130">-ResourceGroupName</span></span>
<span data-ttu-id="a312f-131">Annak az erőforráscsoport-csoportnak a neve, amely alatt frissíteni szeretné a tárterület-tárolót.</span><span class="sxs-lookup"><span data-stu-id="a312f-131">Name of resource group under which you want to update storage target.</span></span>

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

### <span data-ttu-id="a312f-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a312f-132">-Confirm</span></span>
<span data-ttu-id="a312f-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a312f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a312f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a312f-134">-WhatIf</span></span>
<span data-ttu-id="a312f-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a312f-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a312f-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a312f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a312f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a312f-137">CommonParameters</span></span>
<span data-ttu-id="a312f-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a312f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a312f-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a312f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a312f-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a312f-140">INPUTS</span></span>

### <span data-ttu-id="a312f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a312f-141">System.String</span></span>

## <span data-ttu-id="a312f-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a312f-142">OUTPUTS</span></span>

### <span data-ttu-id="a312f-143">Microsoft. Azure. PowerShell. parancsmagok. HPCCache. models. PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="a312f-143">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="a312f-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a312f-144">NOTES</span></span>

## <span data-ttu-id="a312f-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a312f-145">RELATED LINKS</span></span>
