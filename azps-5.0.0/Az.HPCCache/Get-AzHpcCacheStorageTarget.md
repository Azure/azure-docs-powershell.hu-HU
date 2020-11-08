---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
ms.openlocfilehash: c32b47b7300c7da0a6517ca5e3802af60bd0f571
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187815"
---
# <span data-ttu-id="278c6-101">Get-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="278c6-101">Get-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="278c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="278c6-102">SYNOPSIS</span></span>
<span data-ttu-id="278c6-103">A HPC-gyorsítótár tárolási célja (i)</span><span class="sxs-lookup"><span data-stu-id="278c6-103">Get HPC cache storage target(s).</span></span>

## <span data-ttu-id="278c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="278c6-104">SYNTAX</span></span>

### <span data-ttu-id="278c6-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="278c6-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="278c6-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="278c6-106">ByResourceIdParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="278c6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="278c6-107">ByObjectParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheObject <PSHPCCache> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="278c6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="278c6-108">DESCRIPTION</span></span>
<span data-ttu-id="278c6-109">A **Get-AzHpcCacheStorageTarget** parancsmag a gyorsítótárban lévő tárterület-tárolókat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="278c6-109">The **Get-AzHpcCacheStorageTarget** cmdlet gets storage target(s) that exist on cache.</span></span>

## <span data-ttu-id="278c6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="278c6-110">EXAMPLES</span></span>

### <span data-ttu-id="278c6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="278c6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest
```

### <span data-ttu-id="278c6-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="278c6-112">Example 2</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest -StorageTargetName stTest
```

## <span data-ttu-id="278c6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="278c6-113">PARAMETERS</span></span>

### <span data-ttu-id="278c6-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="278c6-114">-CacheId</span></span>
<span data-ttu-id="278c6-115">A gyorsítótár erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="278c6-115">The resource id of the Cache</span></span>

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

### <span data-ttu-id="278c6-116">-CacheName</span><span class="sxs-lookup"><span data-stu-id="278c6-116">-CacheName</span></span>
<span data-ttu-id="278c6-117">A gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="278c6-117">Name of cache.</span></span>

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

### <span data-ttu-id="278c6-118">-CacheObject</span><span class="sxs-lookup"><span data-stu-id="278c6-118">-CacheObject</span></span>
<span data-ttu-id="278c6-119">Az elindítani kívánt gyorsítótár-objektum.</span><span class="sxs-lookup"><span data-stu-id="278c6-119">The cache object to start.</span></span>

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

### <span data-ttu-id="278c6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="278c6-120">-DefaultProfile</span></span>
<span data-ttu-id="278c6-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="278c6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="278c6-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="278c6-122">-Name</span></span>
<span data-ttu-id="278c6-123">A tárolási cél neve</span><span class="sxs-lookup"><span data-stu-id="278c6-123">Name of storage target.</span></span>

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

### <span data-ttu-id="278c6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="278c6-124">-ResourceGroupName</span></span>
<span data-ttu-id="278c6-125">Az erőforráscsoport-gyorsítótár neve be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="278c6-125">Name of resource group cache is in.</span></span>


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

### <span data-ttu-id="278c6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="278c6-126">CommonParameters</span></span>
<span data-ttu-id="278c6-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="278c6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="278c6-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="278c6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="278c6-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="278c6-129">INPUTS</span></span>

### <span data-ttu-id="278c6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="278c6-130">System.String</span></span>

## <span data-ttu-id="278c6-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="278c6-131">OUTPUTS</span></span>

### <span data-ttu-id="278c6-132">Microsoft. Azure. PowerShell. parancsmagok. HPCCache. models. PSHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="278c6-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span></span>

## <span data-ttu-id="278c6-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="278c6-133">NOTES</span></span>

## <span data-ttu-id="278c6-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="278c6-134">RELATED LINKS</span></span>
