---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
ms.openlocfilehash: 38c72a19e73d87272fb91fb6472a41496658e7d6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846926"
---
# <span data-ttu-id="ded46-101">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="ded46-101">Remove-AzRedisCacheLink</span></span>

## <span data-ttu-id="ded46-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ded46-102">SYNOPSIS</span></span>
<span data-ttu-id="ded46-103">Geo-replikációs hivatkozás eltávolítása két Redis-gyorsítótár között</span><span class="sxs-lookup"><span data-stu-id="ded46-103">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="ded46-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ded46-104">SYNTAX</span></span>

```
Remove-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ded46-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ded46-105">DESCRIPTION</span></span>
<span data-ttu-id="ded46-106">Geo-replikációs hivatkozás eltávolítása két Redis-gyorsítótár között</span><span class="sxs-lookup"><span data-stu-id="ded46-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="ded46-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ded46-107">EXAMPLES</span></span>

### <span data-ttu-id="ded46-108">Példa 1: Geo-replikációs hivatkozás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ded46-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="ded46-109">Ez a parancs eltávolítja a Geo-replikációs hivatkozásokat, amelyekben az mycache1 nevű Redis-gyorsítótár az elsődleges, a Redis gyorsítótára pedig másodlagos.</span><span class="sxs-lookup"><span data-stu-id="ded46-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="ded46-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ded46-110">PARAMETERS</span></span>

### <span data-ttu-id="ded46-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ded46-111">-DefaultProfile</span></span>
<span data-ttu-id="ded46-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ded46-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ded46-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ded46-113">-PassThru</span></span>
<span data-ttu-id="ded46-114">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ded46-114">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ded46-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="ded46-115">-PrimaryServerName</span></span>
<span data-ttu-id="ded46-116">Az elsődleges Redis-gyorsítótár neve hivatkozásban.</span><span class="sxs-lookup"><span data-stu-id="ded46-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="ded46-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="ded46-117">-SecondaryServerName</span></span>
<span data-ttu-id="ded46-118">A másodlagos Redis-gyorsítótár neve hivatkozásban.</span><span class="sxs-lookup"><span data-stu-id="ded46-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="ded46-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ded46-119">-Confirm</span></span>
<span data-ttu-id="ded46-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ded46-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ded46-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ded46-121">-WhatIf</span></span>
<span data-ttu-id="ded46-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ded46-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ded46-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ded46-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ded46-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ded46-124">CommonParameters</span></span>
<span data-ttu-id="ded46-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ded46-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ded46-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ded46-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ded46-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ded46-127">INPUTS</span></span>

### <span data-ttu-id="ded46-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ded46-128">System.String</span></span>

## <span data-ttu-id="ded46-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ded46-129">OUTPUTS</span></span>

### <span data-ttu-id="ded46-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ded46-130">System.Boolean</span></span>

## <span data-ttu-id="ded46-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ded46-131">NOTES</span></span>

## <span data-ttu-id="ded46-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ded46-132">RELATED LINKS</span></span>

[<span data-ttu-id="ded46-133">Új – AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="ded46-133">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="ded46-134">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="ded46-134">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="ded46-135">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ded46-135">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="ded46-136">Új – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ded46-136">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="ded46-137">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ded46-137">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="ded46-138">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ded46-138">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)