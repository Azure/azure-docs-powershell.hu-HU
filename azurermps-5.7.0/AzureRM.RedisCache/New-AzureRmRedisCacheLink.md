---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
ms.openlocfilehash: dd9e070a0228cf9bc492f8680917ae0f308e9019
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679266"
---
# <span data-ttu-id="20d9c-101">New-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="20d9c-101">New-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="20d9c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20d9c-102">SYNOPSIS</span></span>
<span data-ttu-id="20d9c-103">Geo-replikációs hivatkozás létrehozása két Redis-gyorsítótár között</span><span class="sxs-lookup"><span data-stu-id="20d9c-103">Create a geo replication link between two Redis Caches.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20d9c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20d9c-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20d9c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="20d9c-105">DESCRIPTION</span></span>
<span data-ttu-id="20d9c-106">Geo-replikációs hivatkozás létrehozása két Redis-gyorsítótár között</span><span class="sxs-lookup"><span data-stu-id="20d9c-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="20d9c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="20d9c-107">EXAMPLES</span></span>

### <span data-ttu-id="20d9c-108">Példa 1: hivatkozás létrehozása két gyorsítótár között</span><span class="sxs-lookup"><span data-stu-id="20d9c-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="20d9c-109">Ez a parancs geo-replikációs kapcsolatot hoz létre a Redis-gyorsítótár mycache1 és a mycache2 között.</span><span class="sxs-lookup"><span data-stu-id="20d9c-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="20d9c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20d9c-110">PARAMETERS</span></span>

### <span data-ttu-id="20d9c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20d9c-111">-DefaultProfile</span></span>
<span data-ttu-id="20d9c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20d9c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20d9c-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="20d9c-113">-PrimaryServerName</span></span>
<span data-ttu-id="20d9c-114">Az elsődleges Redis-gyorsítótár neve hivatkozásban.</span><span class="sxs-lookup"><span data-stu-id="20d9c-114">Name of primary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20d9c-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="20d9c-115">-SecondaryServerName</span></span>
<span data-ttu-id="20d9c-116">A másodlagos Redis-gyorsítótár neve hivatkozásban.</span><span class="sxs-lookup"><span data-stu-id="20d9c-116">Name of secondary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20d9c-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="20d9c-117">-Confirm</span></span>
<span data-ttu-id="20d9c-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="20d9c-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20d9c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20d9c-119">-WhatIf</span></span>
<span data-ttu-id="20d9c-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="20d9c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20d9c-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="20d9c-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20d9c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20d9c-122">CommonParameters</span></span>
<span data-ttu-id="20d9c-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20d9c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20d9c-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20d9c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20d9c-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20d9c-125">INPUTS</span></span>

### <span data-ttu-id="20d9c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="20d9c-126">System.String</span></span>

## <span data-ttu-id="20d9c-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20d9c-127">OUTPUTS</span></span>

### <span data-ttu-id="20d9c-128">Microsoft. Azure. Command. RedisCache. models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="20d9c-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="20d9c-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20d9c-129">NOTES</span></span>

## <span data-ttu-id="20d9c-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20d9c-130">RELATED LINKS</span></span>

[<span data-ttu-id="20d9c-131">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="20d9c-131">Get-AzureRmRedisCacheLink</span></span>](./Get-AzureRmRedisCacheLink.md)

[<span data-ttu-id="20d9c-132">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="20d9c-132">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="20d9c-133">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="20d9c-133">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="20d9c-134">Új – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="20d9c-134">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="20d9c-135">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="20d9c-135">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="20d9c-136">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="20d9c-136">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
