---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
ms.openlocfilehash: c32b47b7300c7da0a6517ca5e3802af60bd0f571
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469633"
---
# <span data-ttu-id="23ad7-101">Get-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="23ad7-101">Get-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="23ad7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23ad7-102">SYNOPSIS</span></span>
<span data-ttu-id="23ad7-103">A HPC gyorsítótár-tároló célhelyének(i) lekérte.</span><span class="sxs-lookup"><span data-stu-id="23ad7-103">Get HPC cache storage target(s).</span></span>

## <span data-ttu-id="23ad7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="23ad7-104">SYNTAX</span></span>

### <span data-ttu-id="23ad7-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="23ad7-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23ad7-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23ad7-106">ByResourceIdParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23ad7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23ad7-107">ByObjectParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheObject <PSHPCCache> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23ad7-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="23ad7-108">DESCRIPTION</span></span>
<span data-ttu-id="23ad7-109">A **Get-AzHpcCacheStorageTarget** parancsmag a gyorsítótárban meglévő tároló cél(a)t kapja meg.</span><span class="sxs-lookup"><span data-stu-id="23ad7-109">The **Get-AzHpcCacheStorageTarget** cmdlet gets storage target(s) that exist on cache.</span></span>

## <span data-ttu-id="23ad7-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="23ad7-110">EXAMPLES</span></span>

### <span data-ttu-id="23ad7-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="23ad7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest
```

### <span data-ttu-id="23ad7-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="23ad7-112">Example 2</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest -StorageTargetName stTest
```

## <span data-ttu-id="23ad7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23ad7-113">PARAMETERS</span></span>

### <span data-ttu-id="23ad7-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="23ad7-114">-CacheId</span></span>
<span data-ttu-id="23ad7-115">A gyorsítótár erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="23ad7-115">The resource id of the Cache</span></span>

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

### <span data-ttu-id="23ad7-116">-CacheName</span><span class="sxs-lookup"><span data-stu-id="23ad7-116">-CacheName</span></span>
<span data-ttu-id="23ad7-117">A gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="23ad7-117">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23ad7-118">-CacheObject</span><span class="sxs-lookup"><span data-stu-id="23ad7-118">-CacheObject</span></span>
<span data-ttu-id="23ad7-119">A elindított gyorsítótárobjektum.</span><span class="sxs-lookup"><span data-stu-id="23ad7-119">The cache object to start.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23ad7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23ad7-120">-DefaultProfile</span></span>
<span data-ttu-id="23ad7-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23ad7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23ad7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="23ad7-122">-Name</span></span>
<span data-ttu-id="23ad7-123">A tárolási cél neve.</span><span class="sxs-lookup"><span data-stu-id="23ad7-123">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: StorageTargetName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23ad7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23ad7-124">-ResourceGroupName</span></span>
<span data-ttu-id="23ad7-125">Az erőforráscsoport-gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="23ad7-125">Name of resource group cache is in.</span></span>


```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23ad7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23ad7-126">CommonParameters</span></span>
<span data-ttu-id="23ad7-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23ad7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23ad7-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23ad7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23ad7-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23ad7-129">INPUTS</span></span>

### <span data-ttu-id="23ad7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="23ad7-130">System.String</span></span>

## <span data-ttu-id="23ad7-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23ad7-131">OUTPUTS</span></span>

### <span data-ttu-id="23ad7-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="23ad7-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span></span>

## <span data-ttu-id="23ad7-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="23ad7-133">NOTES</span></span>

## <span data-ttu-id="23ad7-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23ad7-134">RELATED LINKS</span></span>
