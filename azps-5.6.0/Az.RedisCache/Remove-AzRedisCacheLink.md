---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/remove-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
ms.openlocfilehash: 2227f4fc9cd8128018160a3e62d9ba56bd664d8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919161"
---
# <span data-ttu-id="2e606-101">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="2e606-101">Remove-AzRedisCacheLink</span></span>

## <span data-ttu-id="2e606-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e606-102">SYNOPSIS</span></span>
<span data-ttu-id="2e606-103">Távolítsa el a geo replikációs kapcsolatot két redis-gyorsítótár között.</span><span class="sxs-lookup"><span data-stu-id="2e606-103">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="2e606-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2e606-104">SYNTAX</span></span>

```
Remove-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e606-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2e606-105">DESCRIPTION</span></span>
<span data-ttu-id="2e606-106">Távolítsa el a geo replikációs kapcsolatot két redis-gyorsítótár között.</span><span class="sxs-lookup"><span data-stu-id="2e606-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="2e606-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2e606-107">EXAMPLES</span></span>

### <span data-ttu-id="2e606-108">1. példa: Földrajzi replikációs hivatkozás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2e606-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="2e606-109">Ez a parancs eltávolítja a georeplikációs hivatkozásokat, amelyekben a mycache1 nevű Redis Cache az elsődleges, a Redis Cache pedig másodlagos.</span><span class="sxs-lookup"><span data-stu-id="2e606-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="2e606-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e606-110">PARAMETERS</span></span>

### <span data-ttu-id="2e606-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e606-111">-DefaultProfile</span></span>
<span data-ttu-id="2e606-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e606-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e606-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e606-113">-PassThru</span></span>
<span data-ttu-id="2e606-114">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="2e606-114">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2e606-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="2e606-115">-PrimaryServerName</span></span>
<span data-ttu-id="2e606-116">A csatolásban lévő elsődleges redis cache neve.</span><span class="sxs-lookup"><span data-stu-id="2e606-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="2e606-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="2e606-117">-SecondaryServerName</span></span>
<span data-ttu-id="2e606-118">A másodlagos redis-gyorsítótár neve a csatolásban.</span><span class="sxs-lookup"><span data-stu-id="2e606-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="2e606-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e606-119">-Confirm</span></span>
<span data-ttu-id="2e606-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2e606-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e606-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e606-121">-WhatIf</span></span>
<span data-ttu-id="2e606-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2e606-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e606-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e606-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e606-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e606-124">CommonParameters</span></span>
<span data-ttu-id="2e606-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e606-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e606-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e606-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e606-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e606-127">INPUTS</span></span>

### <span data-ttu-id="2e606-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2e606-128">System.String</span></span>

## <span data-ttu-id="2e606-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e606-129">OUTPUTS</span></span>

### <span data-ttu-id="2e606-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2e606-130">System.Boolean</span></span>

## <span data-ttu-id="2e606-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2e606-131">NOTES</span></span>

## <span data-ttu-id="2e606-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e606-132">RELATED LINKS</span></span>

[<span data-ttu-id="2e606-133">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="2e606-133">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="2e606-134">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="2e606-134">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="2e606-135">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2e606-135">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="2e606-136">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2e606-136">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="2e606-137">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2e606-137">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="2e606-138">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2e606-138">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)