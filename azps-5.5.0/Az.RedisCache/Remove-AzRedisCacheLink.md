---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
ms.openlocfilehash: 38c72a19e73d87272fb91fb6472a41496658e7d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151026"
---
# <span data-ttu-id="77cf8-101">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="77cf8-101">Remove-AzRedisCacheLink</span></span>

## <span data-ttu-id="77cf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77cf8-102">SYNOPSIS</span></span>
<span data-ttu-id="77cf8-103">Távolítsa el a geo replikációs kapcsolatot két redis-gyorsítótár között.</span><span class="sxs-lookup"><span data-stu-id="77cf8-103">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="77cf8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="77cf8-104">SYNTAX</span></span>

```
Remove-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77cf8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="77cf8-105">DESCRIPTION</span></span>
<span data-ttu-id="77cf8-106">Távolítsa el a geo replikációs kapcsolatot két redis-gyorsítótár között.</span><span class="sxs-lookup"><span data-stu-id="77cf8-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="77cf8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="77cf8-107">EXAMPLES</span></span>

### <span data-ttu-id="77cf8-108">1. példa: Földrajzi replikációs hivatkozás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="77cf8-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="77cf8-109">Ez a parancs eltávolítja a georeplikációs hivatkozásokat, ahol a mycache1 nevű Redis Cache elsődleges, a Redis Cache pedig másodlagos.</span><span class="sxs-lookup"><span data-stu-id="77cf8-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="77cf8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77cf8-110">PARAMETERS</span></span>

### <span data-ttu-id="77cf8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77cf8-111">-DefaultProfile</span></span>
<span data-ttu-id="77cf8-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="77cf8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77cf8-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77cf8-113">-PassThru</span></span>
<span data-ttu-id="77cf8-114">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="77cf8-114">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="77cf8-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="77cf8-115">-PrimaryServerName</span></span>
<span data-ttu-id="77cf8-116">A csatolásban lévő elsődleges redis cache neve.</span><span class="sxs-lookup"><span data-stu-id="77cf8-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="77cf8-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="77cf8-117">-SecondaryServerName</span></span>
<span data-ttu-id="77cf8-118">A másodlagos redis-gyorsítótár neve a csatolásban.</span><span class="sxs-lookup"><span data-stu-id="77cf8-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="77cf8-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77cf8-119">-Confirm</span></span>
<span data-ttu-id="77cf8-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="77cf8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77cf8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77cf8-121">-WhatIf</span></span>
<span data-ttu-id="77cf8-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="77cf8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77cf8-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="77cf8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77cf8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77cf8-124">CommonParameters</span></span>
<span data-ttu-id="77cf8-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77cf8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77cf8-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77cf8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77cf8-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77cf8-127">INPUTS</span></span>

### <span data-ttu-id="77cf8-128">System.String</span><span class="sxs-lookup"><span data-stu-id="77cf8-128">System.String</span></span>

## <span data-ttu-id="77cf8-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77cf8-129">OUTPUTS</span></span>

### <span data-ttu-id="77cf8-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="77cf8-130">System.Boolean</span></span>

## <span data-ttu-id="77cf8-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="77cf8-131">NOTES</span></span>

## <span data-ttu-id="77cf8-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77cf8-132">RELATED LINKS</span></span>

[<span data-ttu-id="77cf8-133">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="77cf8-133">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="77cf8-134">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="77cf8-134">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="77cf8-135">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="77cf8-135">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="77cf8-136">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="77cf8-136">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="77cf8-137">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="77cf8-137">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="77cf8-138">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="77cf8-138">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)