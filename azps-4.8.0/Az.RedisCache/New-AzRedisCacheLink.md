---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
ms.openlocfilehash: d27f3ece14e18465fc534bff1a3451eaec2c40a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181005"
---
# <span data-ttu-id="426c5-101">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="426c5-101">New-AzRedisCacheLink</span></span>

## <span data-ttu-id="426c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="426c5-102">SYNOPSIS</span></span>
<span data-ttu-id="426c5-103">Geo-replikációs hivatkozás létrehozása két Redis-gyorsítótár között</span><span class="sxs-lookup"><span data-stu-id="426c5-103">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="426c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="426c5-104">SYNTAX</span></span>

```
New-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="426c5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="426c5-105">DESCRIPTION</span></span>
<span data-ttu-id="426c5-106">Geo-replikációs hivatkozás létrehozása két Redis-gyorsítótár között</span><span class="sxs-lookup"><span data-stu-id="426c5-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="426c5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="426c5-107">EXAMPLES</span></span>

### <span data-ttu-id="426c5-108">Példa 1: hivatkozás létrehozása két gyorsítótár között</span><span class="sxs-lookup"><span data-stu-id="426c5-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="426c5-109">Ez a parancs geo-replikációs kapcsolatot hoz létre a Redis-gyorsítótár mycache1 és a mycache2 között.</span><span class="sxs-lookup"><span data-stu-id="426c5-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="426c5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="426c5-110">PARAMETERS</span></span>

### <span data-ttu-id="426c5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="426c5-111">-DefaultProfile</span></span>
<span data-ttu-id="426c5-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="426c5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="426c5-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="426c5-113">-PrimaryServerName</span></span>
<span data-ttu-id="426c5-114">Az elsődleges Redis-gyorsítótár neve hivatkozásban.</span><span class="sxs-lookup"><span data-stu-id="426c5-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="426c5-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="426c5-115">-SecondaryServerName</span></span>
<span data-ttu-id="426c5-116">A másodlagos Redis-gyorsítótár neve hivatkozásban.</span><span class="sxs-lookup"><span data-stu-id="426c5-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="426c5-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="426c5-117">-Confirm</span></span>
<span data-ttu-id="426c5-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="426c5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="426c5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="426c5-119">-WhatIf</span></span>
<span data-ttu-id="426c5-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="426c5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="426c5-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="426c5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="426c5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="426c5-122">CommonParameters</span></span>
<span data-ttu-id="426c5-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="426c5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="426c5-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="426c5-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="426c5-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="426c5-125">INPUTS</span></span>

### <span data-ttu-id="426c5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="426c5-126">System.String</span></span>

## <span data-ttu-id="426c5-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="426c5-127">OUTPUTS</span></span>

### <span data-ttu-id="426c5-128">Microsoft. Azure. Command. RedisCache. models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="426c5-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="426c5-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="426c5-129">NOTES</span></span>

## <span data-ttu-id="426c5-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="426c5-130">RELATED LINKS</span></span>

[<span data-ttu-id="426c5-131">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="426c5-131">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="426c5-132">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="426c5-132">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="426c5-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="426c5-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="426c5-134">Új – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="426c5-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="426c5-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="426c5-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="426c5-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="426c5-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)