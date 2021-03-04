---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
ms.openlocfilehash: 8423c098542a621ec66a5de3255ccf62c3e8ec94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918106"
---
# <span data-ttu-id="4449e-101">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4449e-101">Get-AzRedisCache</span></span>

## <span data-ttu-id="4449e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4449e-102">SYNOPSIS</span></span>
<span data-ttu-id="4449e-103">Redis gyorsítótárat kap.</span><span class="sxs-lookup"><span data-stu-id="4449e-103">Gets a Redis Cache.</span></span>

## <span data-ttu-id="4449e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4449e-104">SYNTAX</span></span>

```
Get-AzRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4449e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4449e-105">DESCRIPTION</span></span>
<span data-ttu-id="4449e-106">A **Get-AzRedisCache** parancsmag megkapja a megadott Azure Redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="4449e-106">The **Get-AzRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="4449e-107">Ha nem ad meg paramétereket, ez a művelet az aktuális előfizetés összes redis-gyorsítótárát megkapja.</span><span class="sxs-lookup"><span data-stu-id="4449e-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="4449e-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4449e-108">EXAMPLES</span></span>

### <span data-ttu-id="4449e-109">1. példa: Redis Cache lekért név szerint</span><span class="sxs-lookup"><span data-stu-id="4449e-109">Example 1: Get a Redis Cache by name</span></span>
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

<span data-ttu-id="4449e-110">Ez a parancs a Myexists nevű Redis Cache-t kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4449e-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="4449e-111">2. példa: Erőforráscsoport minden redis-gyorsítótárának be szereznie</span><span class="sxs-lookup"><span data-stu-id="4449e-111">Example 2: Get every Redis Cache in a resource group</span></span>
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

<span data-ttu-id="4449e-112">Ez a parancs a megadott erőforráscsoport összes redis-gyorsítótárát beveszi.</span><span class="sxs-lookup"><span data-stu-id="4449e-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="4449e-113">3. példa: Az aktuális előfizetés összes redis-gyorsítótárának lekérte</span><span class="sxs-lookup"><span data-stu-id="4449e-113">Example 3: Get every Redis Cache in the current subscription</span></span>
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

<span data-ttu-id="4449e-114">Ez a parancs az aktuális előfizetés összes redis-gyorsítótárát megkapja.</span><span class="sxs-lookup"><span data-stu-id="4449e-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="4449e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4449e-115">PARAMETERS</span></span>

### <span data-ttu-id="4449e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4449e-116">-DefaultProfile</span></span>
<span data-ttu-id="4449e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4449e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4449e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4449e-118">-Name</span></span>
<span data-ttu-id="4449e-119">A lekért redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4449e-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="4449e-120">Használja a *ResourceGroupName paraméterrel.*</span><span class="sxs-lookup"><span data-stu-id="4449e-120">Use with the *ResourceGroupName* parameter.</span></span>

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

### <span data-ttu-id="4449e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4449e-121">-ResourceGroupName</span></span>
<span data-ttu-id="4449e-122">Annak az erőforráscsoportnak a neve, amely a lekért redis gyorsítótárat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4449e-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>
<span data-ttu-id="4449e-123">Ha csak az *ResourceGroupName* paramétert adja meg, ez a művelet a megadott erőforráscsoport összes redis-gyorsítótárát megkapja.</span><span class="sxs-lookup"><span data-stu-id="4449e-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

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

### <span data-ttu-id="4449e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4449e-124">CommonParameters</span></span>
<span data-ttu-id="4449e-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4449e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4449e-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4449e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4449e-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4449e-127">INPUTS</span></span>

### <span data-ttu-id="4449e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4449e-128">System.String</span></span>

## <span data-ttu-id="4449e-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4449e-129">OUTPUTS</span></span>

### <span data-ttu-id="4449e-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="4449e-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="4449e-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4449e-131">NOTES</span></span>

## <span data-ttu-id="4449e-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4449e-132">RELATED LINKS</span></span>

[<span data-ttu-id="4449e-133">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4449e-133">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="4449e-134">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4449e-134">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="4449e-135">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4449e-135">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


