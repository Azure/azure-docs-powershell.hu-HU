---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
ms.openlocfilehash: d27f3ece14e18465fc534bff1a3451eaec2c40a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186559"
---
# <span data-ttu-id="51982-101">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="51982-101">New-AzRedisCacheLink</span></span>

## <span data-ttu-id="51982-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51982-102">SYNOPSIS</span></span>
<span data-ttu-id="51982-103">Geo-replikációs hivatkozás létrehozása két Redis-gyorsítótár között</span><span class="sxs-lookup"><span data-stu-id="51982-103">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="51982-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51982-104">SYNTAX</span></span>

```
New-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51982-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="51982-105">DESCRIPTION</span></span>
<span data-ttu-id="51982-106">Geo-replikációs hivatkozás létrehozása két Redis-gyorsítótár között</span><span class="sxs-lookup"><span data-stu-id="51982-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="51982-107">Példák</span><span class="sxs-lookup"><span data-stu-id="51982-107">EXAMPLES</span></span>

### <span data-ttu-id="51982-108">Példa 1: hivatkozás létrehozása két gyorsítótár között</span><span class="sxs-lookup"><span data-stu-id="51982-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="51982-109">Ez a parancs geo-replikációs kapcsolatot hoz létre a Redis-gyorsítótár mycache1 és a mycache2 között.</span><span class="sxs-lookup"><span data-stu-id="51982-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="51982-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51982-110">PARAMETERS</span></span>

### <span data-ttu-id="51982-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51982-111">-DefaultProfile</span></span>
<span data-ttu-id="51982-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51982-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51982-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="51982-113">-PrimaryServerName</span></span>
<span data-ttu-id="51982-114">Az elsődleges Redis-gyorsítótár neve hivatkozásban.</span><span class="sxs-lookup"><span data-stu-id="51982-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="51982-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="51982-115">-SecondaryServerName</span></span>
<span data-ttu-id="51982-116">A másodlagos Redis-gyorsítótár neve hivatkozásban.</span><span class="sxs-lookup"><span data-stu-id="51982-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="51982-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="51982-117">-Confirm</span></span>
<span data-ttu-id="51982-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="51982-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51982-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51982-119">-WhatIf</span></span>
<span data-ttu-id="51982-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="51982-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51982-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="51982-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51982-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51982-122">CommonParameters</span></span>
<span data-ttu-id="51982-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51982-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51982-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51982-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51982-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51982-125">INPUTS</span></span>

### <span data-ttu-id="51982-126">System. String</span><span class="sxs-lookup"><span data-stu-id="51982-126">System.String</span></span>

## <span data-ttu-id="51982-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51982-127">OUTPUTS</span></span>

### <span data-ttu-id="51982-128">Microsoft. Azure. Command. RedisCache. models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="51982-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="51982-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51982-129">NOTES</span></span>

## <span data-ttu-id="51982-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51982-130">RELATED LINKS</span></span>

[<span data-ttu-id="51982-131">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="51982-131">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="51982-132">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="51982-132">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="51982-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="51982-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="51982-134">Új – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="51982-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="51982-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="51982-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="51982-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="51982-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)