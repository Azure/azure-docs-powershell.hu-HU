---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheLink.md
ms.openlocfilehash: e4c45095dba8ec72e00fa26eee2d8a3fb6f029fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679834"
---
# <span data-ttu-id="0c5e5-101">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="0c5e5-101">Remove-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="0c5e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0c5e5-102">SYNOPSIS</span></span>
<span data-ttu-id="0c5e5-103">Geo-replikációs hivatkozás eltávolítása két Redis-gyorsítótár között</span><span class="sxs-lookup"><span data-stu-id="0c5e5-103">Remove a geo replication link between two Redis Caches.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c5e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0c5e5-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c5e5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0c5e5-105">DESCRIPTION</span></span>
<span data-ttu-id="0c5e5-106">Geo-replikációs hivatkozás eltávolítása két Redis-gyorsítótár között</span><span class="sxs-lookup"><span data-stu-id="0c5e5-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="0c5e5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0c5e5-107">EXAMPLES</span></span>

### <span data-ttu-id="0c5e5-108">Példa 1: Geo-replikációs hivatkozás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0c5e5-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="0c5e5-109">Ez a parancs eltávolítja a Geo-replikációs hivatkozásokat, amelyekben az mycache1 nevű Redis-gyorsítótár az elsődleges, a Redis gyorsítótára pedig másodlagos.</span><span class="sxs-lookup"><span data-stu-id="0c5e5-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="0c5e5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0c5e5-110">PARAMETERS</span></span>

### <span data-ttu-id="0c5e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c5e5-111">-DefaultProfile</span></span>
<span data-ttu-id="0c5e5-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c5e5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c5e5-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c5e5-113">-PassThru</span></span>
<span data-ttu-id="0c5e5-114">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="0c5e5-114">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0c5e5-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="0c5e5-115">-PrimaryServerName</span></span>
<span data-ttu-id="0c5e5-116">Az elsődleges Redis-gyorsítótár neve hivatkozásban.</span><span class="sxs-lookup"><span data-stu-id="0c5e5-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="0c5e5-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="0c5e5-117">-SecondaryServerName</span></span>
<span data-ttu-id="0c5e5-118">A másodlagos Redis-gyorsítótár neve hivatkozásban.</span><span class="sxs-lookup"><span data-stu-id="0c5e5-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="0c5e5-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0c5e5-119">-Confirm</span></span>
<span data-ttu-id="0c5e5-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0c5e5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c5e5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c5e5-121">-WhatIf</span></span>
<span data-ttu-id="0c5e5-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0c5e5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c5e5-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0c5e5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c5e5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c5e5-124">CommonParameters</span></span>
<span data-ttu-id="0c5e5-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0c5e5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c5e5-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c5e5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c5e5-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c5e5-127">INPUTS</span></span>

### <span data-ttu-id="0c5e5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0c5e5-128">System.String</span></span>

## <span data-ttu-id="0c5e5-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c5e5-129">OUTPUTS</span></span>

### <span data-ttu-id="0c5e5-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0c5e5-130">System.Boolean</span></span>

## <span data-ttu-id="0c5e5-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0c5e5-131">NOTES</span></span>

## <span data-ttu-id="0c5e5-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c5e5-132">RELATED LINKS</span></span>

[<span data-ttu-id="0c5e5-133">Új – AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="0c5e5-133">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="0c5e5-134">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="0c5e5-134">Get-AzureRmRedisCacheLink</span></span>](./Get-AzureRmRedisCacheLink.md)

[<span data-ttu-id="0c5e5-135">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0c5e5-135">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="0c5e5-136">Új – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0c5e5-136">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="0c5e5-137">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0c5e5-137">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="0c5e5-138">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0c5e5-138">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
