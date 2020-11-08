---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
ms.openlocfilehash: cc8d6ff7e7fb55c5ee71c82a8eca4cc661b98b07
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194872"
---
# <span data-ttu-id="afa12-101">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="afa12-101">Get-AzRedisCache</span></span>

## <span data-ttu-id="afa12-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="afa12-102">SYNOPSIS</span></span>
<span data-ttu-id="afa12-103">Redis-gyorsítótárat kap.</span><span class="sxs-lookup"><span data-stu-id="afa12-103">Gets a Redis Cache.</span></span>

## <span data-ttu-id="afa12-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="afa12-104">SYNTAX</span></span>

```
Get-AzRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="afa12-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="afa12-105">DESCRIPTION</span></span>
<span data-ttu-id="afa12-106">A **Get-AzRedisCache** parancsmag a megadott Azure Redis-gyorsítótárat kapja.</span><span class="sxs-lookup"><span data-stu-id="afa12-106">The **Get-AzRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="afa12-107">Ha nem ad meg paramétereket, ez a művelet minden Redis-gyorsítótárban megkapja az aktuális előfizetést.</span><span class="sxs-lookup"><span data-stu-id="afa12-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="afa12-108">Példák</span><span class="sxs-lookup"><span data-stu-id="afa12-108">EXAMPLES</span></span>

### <span data-ttu-id="afa12-109">Példa 1: Redis-gyorsítótár beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="afa12-109">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzRedisCache -Name "myexists"

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="afa12-110">Ez a parancs a myexists nevű Redis-gyorsítótárat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="afa12-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="afa12-111">2. példa: az erőforráscsoport minden Redis-gyorsítótárának beolvasása</span><span class="sxs-lookup"><span data-stu-id="afa12-111">Example 2: Get every Redis Cache in a resource group</span></span>
```
PS C:\>Get-AzRedisCache -ResourceGroupName "myGroup"

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
        Location           : North Central US
        Name               : myearlier
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : True
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Standard
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="afa12-112">Ez a parancs a megadott erőforráscsoport minden Redis-gyorsítótárát beolvassa.</span><span class="sxs-lookup"><span data-stu-id="afa12-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="afa12-113">3. példa: a jelenlegi előfizetés minden Redis-gyorsítótárának beszerzése</span><span class="sxs-lookup"><span data-stu-id="afa12-113">Example 3: Get every Redis Cache in the current subscription</span></span>
```
PS C:\>Get-AzRedisCache

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
        Location           : North Central US
        Name               : myearlier
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : True
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Standard
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup2
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup2/providers/Microsoft.Cache/Redis/myearlier2
        Location           : North Central US
        Name               : myearlier2
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier2.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Basic
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="afa12-114">Ez a parancs minden Redis-gyorsítótárba bekerül az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="afa12-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="afa12-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="afa12-115">PARAMETERS</span></span>

### <span data-ttu-id="afa12-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afa12-116">-DefaultProfile</span></span>
<span data-ttu-id="afa12-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="afa12-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afa12-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="afa12-118">-Name</span></span>
<span data-ttu-id="afa12-119">A beolvasott Redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="afa12-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="afa12-120">Használja a *ResourceGroupName* paramétert.</span><span class="sxs-lookup"><span data-stu-id="afa12-120">Use with the *ResourceGroupName* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afa12-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afa12-121">-ResourceGroupName</span></span>
<span data-ttu-id="afa12-122">Annak a csoportnak a neve, amely a Redis-gyorsítótárat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="afa12-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>
<span data-ttu-id="afa12-123">Ha csak a *ResourceGroupName* paramétert adja meg, ez a művelet a megadott erőforráscsoport minden Redis-gyorsítótárát megkapja.</span><span class="sxs-lookup"><span data-stu-id="afa12-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afa12-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afa12-124">CommonParameters</span></span>
<span data-ttu-id="afa12-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="afa12-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afa12-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afa12-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afa12-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="afa12-127">INPUTS</span></span>

### <span data-ttu-id="afa12-128">System. String</span><span class="sxs-lookup"><span data-stu-id="afa12-128">System.String</span></span>

## <span data-ttu-id="afa12-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="afa12-129">OUTPUTS</span></span>

### <span data-ttu-id="afa12-130">Microsoft. Azure. Command. RedisCache. models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="afa12-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="afa12-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="afa12-131">NOTES</span></span>

## <span data-ttu-id="afa12-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="afa12-132">RELATED LINKS</span></span>

[<span data-ttu-id="afa12-133">Új – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="afa12-133">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="afa12-134">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="afa12-134">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="afa12-135">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="afa12-135">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


