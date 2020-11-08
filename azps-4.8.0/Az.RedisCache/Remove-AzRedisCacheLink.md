---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
ms.openlocfilehash: 38c72a19e73d87272fb91fb6472a41496658e7d6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181460"
---
# <span data-ttu-id="02c4f-101">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="02c4f-101">Remove-AzRedisCacheLink</span></span>

## <span data-ttu-id="02c4f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="02c4f-103">Geo-replikációs hivatkozás eltávolítása két Redis-gyorsítótár között</span><span class="sxs-lookup"><span data-stu-id="02c4f-103">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="02c4f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02c4f-104">SYNTAX</span></span>

```
Remove-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02c4f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="02c4f-105">DESCRIPTION</span></span>
<span data-ttu-id="02c4f-106">Geo-replikációs hivatkozás eltávolítása két Redis-gyorsítótár között</span><span class="sxs-lookup"><span data-stu-id="02c4f-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="02c4f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="02c4f-107">EXAMPLES</span></span>

### <span data-ttu-id="02c4f-108">Példa 1: Geo-replikációs hivatkozás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="02c4f-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="02c4f-109">Ez a parancs eltávolítja a Geo-replikációs hivatkozásokat, amelyekben az mycache1 nevű Redis-gyorsítótár az elsődleges, a Redis gyorsítótára pedig másodlagos.</span><span class="sxs-lookup"><span data-stu-id="02c4f-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="02c4f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02c4f-110">PARAMETERS</span></span>

### <span data-ttu-id="02c4f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c4f-111">-DefaultProfile</span></span>
<span data-ttu-id="02c4f-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02c4f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02c4f-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02c4f-113">-PassThru</span></span>
<span data-ttu-id="02c4f-114">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="02c4f-114">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="02c4f-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="02c4f-115">-PrimaryServerName</span></span>
<span data-ttu-id="02c4f-116">Az elsődleges Redis-gyorsítótár neve hivatkozásban.</span><span class="sxs-lookup"><span data-stu-id="02c4f-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="02c4f-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="02c4f-117">-SecondaryServerName</span></span>
<span data-ttu-id="02c4f-118">A másodlagos Redis-gyorsítótár neve hivatkozásban.</span><span class="sxs-lookup"><span data-stu-id="02c4f-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="02c4f-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="02c4f-119">-Confirm</span></span>
<span data-ttu-id="02c4f-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="02c4f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02c4f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02c4f-121">-WhatIf</span></span>
<span data-ttu-id="02c4f-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="02c4f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02c4f-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="02c4f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02c4f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c4f-124">CommonParameters</span></span>
<span data-ttu-id="02c4f-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02c4f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c4f-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02c4f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c4f-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02c4f-127">INPUTS</span></span>

### <span data-ttu-id="02c4f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="02c4f-128">System.String</span></span>

## <span data-ttu-id="02c4f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02c4f-129">OUTPUTS</span></span>

### <span data-ttu-id="02c4f-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="02c4f-130">System.Boolean</span></span>

## <span data-ttu-id="02c4f-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02c4f-131">NOTES</span></span>

## <span data-ttu-id="02c4f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02c4f-132">RELATED LINKS</span></span>

[<span data-ttu-id="02c4f-133">Új – AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="02c4f-133">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="02c4f-134">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="02c4f-134">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="02c4f-135">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="02c4f-135">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="02c4f-136">Új – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="02c4f-136">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="02c4f-137">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="02c4f-137">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="02c4f-138">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="02c4f-138">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)