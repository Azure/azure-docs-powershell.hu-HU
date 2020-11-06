---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
ms.openlocfilehash: 4cdd81b0cf9f83482192fbe6f484fb0b0d1beaf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503968"
---
# <span data-ttu-id="f3229-101">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f3229-101">Get-AzureRmRedisCache</span></span>

## <span data-ttu-id="f3229-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3229-102">SYNOPSIS</span></span>
<span data-ttu-id="f3229-103">Redis-gyorsítótárat kap.</span><span class="sxs-lookup"><span data-stu-id="f3229-103">Gets a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3229-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3229-104">SYNTAX</span></span>

### <span data-ttu-id="f3229-105">All in előfizetés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f3229-105">All In Subscription (Default)</span></span>
```
Get-AzureRmRedisCache [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3229-106">Minden az erőforrás csoportban</span><span class="sxs-lookup"><span data-stu-id="f3229-106">All In Resource Group</span></span>
```
Get-AzureRmRedisCache -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3229-107">Adott Redis-gyorsítótár</span><span class="sxs-lookup"><span data-stu-id="f3229-107">Specific Redis Cache</span></span>
```
Get-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3229-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3229-108">DESCRIPTION</span></span>
<span data-ttu-id="f3229-109">A **Get-AzureRmRedisCache** parancsmag a megadott Azure Redis-gyorsítótárat kapja.</span><span class="sxs-lookup"><span data-stu-id="f3229-109">The **Get-AzureRmRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="f3229-110">Ha nem ad meg paramétereket, ez a művelet minden Redis-gyorsítótárban megkapja az aktuális előfizetést.</span><span class="sxs-lookup"><span data-stu-id="f3229-110">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="f3229-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f3229-111">EXAMPLES</span></span>

### <span data-ttu-id="f3229-112">Példa 1: Redis-gyorsítótár beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="f3229-112">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzureRmRedisCache -ResourceGroupName "myGroup" -Name "myexists"

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
```

<span data-ttu-id="f3229-113">Ez a parancs a myexists nevű Redis-gyorsítótárat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f3229-113">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="f3229-114">2. példa: az erőforráscsoport minden Redis-gyorsítótárának beolvasása</span><span class="sxs-lookup"><span data-stu-id="f3229-114">Example 2: Get every Redis Cache in a resource group</span></span>
```
PS C:\>Get-AzureRmRedisCache -ResourceGroupName "myGroup"


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
```

<span data-ttu-id="f3229-115">Ez a parancs a megadott erőforráscsoport minden Redis-gyorsítótárát beolvassa.</span><span class="sxs-lookup"><span data-stu-id="f3229-115">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="f3229-116">3. példa: a jelenlegi előfizetés minden Redis-gyorsítótárának beszerzése</span><span class="sxs-lookup"><span data-stu-id="f3229-116">Example 3: Get every Redis Cache in the current subscription</span></span>
```
PS C:\>Get-AzureRmRedisCache


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
```

<span data-ttu-id="f3229-117">Ez a parancs minden Redis-gyorsítótárba bekerül az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="f3229-117">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="f3229-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3229-118">PARAMETERS</span></span>

### <span data-ttu-id="f3229-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f3229-119">-Name</span></span>
<span data-ttu-id="f3229-120">A beolvasott Redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3229-120">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="f3229-121">Használja a *ResourceGroupName* paramétert.</span><span class="sxs-lookup"><span data-stu-id="f3229-121">Use with the *ResourceGroupName* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Redis Cache
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3229-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3229-122">-ResourceGroupName</span></span>
<span data-ttu-id="f3229-123">Annak a csoportnak a neve, amely a Redis-gyorsítótárat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f3229-123">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>

<span data-ttu-id="f3229-124">Ha csak a *ResourceGroupName* paramétert adja meg, ez a művelet a megadott erőforráscsoport minden Redis-gyorsítótárát megkapja.</span><span class="sxs-lookup"><span data-stu-id="f3229-124">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group, Specific Redis Cache
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3229-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3229-125">-DefaultProfile</span></span>
<span data-ttu-id="f3229-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3229-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3229-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3229-127">CommonParameters</span></span>
<span data-ttu-id="f3229-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3229-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3229-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3229-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3229-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3229-130">INPUTS</span></span>

### <span data-ttu-id="f3229-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="f3229-131">None</span></span>
<span data-ttu-id="f3229-132">A parancsmagot név szerint, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="f3229-132">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="f3229-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3229-133">OUTPUTS</span></span>

### <span data-ttu-id="f3229-134">Microsoft. Azure. Command. RedisCache. models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="f3229-134">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>
<span data-ttu-id="f3229-135">**RedisCacheAttributes** -objektumok tömbjét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="f3229-135">Returns an array of **RedisCacheAttributes** objects.</span></span>

## <span data-ttu-id="f3229-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3229-136">NOTES</span></span>

## <span data-ttu-id="f3229-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3229-137">RELATED LINKS</span></span>

[<span data-ttu-id="f3229-138">Új – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f3229-138">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="f3229-139">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f3229-139">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="f3229-140">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f3229-140">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


