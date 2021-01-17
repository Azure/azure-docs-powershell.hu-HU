---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
ms.openlocfilehash: d27f3ece14e18465fc534bff1a3451eaec2c40a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336438"
---
# <span data-ttu-id="4ac9f-101">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="4ac9f-101">New-AzRedisCacheLink</span></span>

## <span data-ttu-id="4ac9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ac9f-102">SYNOPSIS</span></span>
<span data-ttu-id="4ac9f-103">Hozzon létre geo replikációs kapcsolatot két redis-gyorsítótár között.</span><span class="sxs-lookup"><span data-stu-id="4ac9f-103">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="4ac9f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4ac9f-104">SYNTAX</span></span>

```
New-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ac9f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4ac9f-105">DESCRIPTION</span></span>
<span data-ttu-id="4ac9f-106">Hozzon létre geo replikációs kapcsolatot két redis-gyorsítótár között.</span><span class="sxs-lookup"><span data-stu-id="4ac9f-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="4ac9f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4ac9f-107">EXAMPLES</span></span>

### <span data-ttu-id="4ac9f-108">1. példa: Hivatkozás létrehozása két gyorsítótár között</span><span class="sxs-lookup"><span data-stu-id="4ac9f-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="4ac9f-109">Ez a parancs geo replikációs kapcsolatot hoz létre a Redis Cache mycache1 és a mycache2 között.</span><span class="sxs-lookup"><span data-stu-id="4ac9f-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="4ac9f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ac9f-110">PARAMETERS</span></span>

### <span data-ttu-id="4ac9f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ac9f-111">-DefaultProfile</span></span>
<span data-ttu-id="4ac9f-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ac9f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ac9f-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="4ac9f-113">-PrimaryServerName</span></span>
<span data-ttu-id="4ac9f-114">A csatolásban lévő elsődleges redis cache neve.</span><span class="sxs-lookup"><span data-stu-id="4ac9f-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="4ac9f-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="4ac9f-115">-SecondaryServerName</span></span>
<span data-ttu-id="4ac9f-116">A másodlagos redis-gyorsítótár neve a csatolásban.</span><span class="sxs-lookup"><span data-stu-id="4ac9f-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="4ac9f-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ac9f-117">-Confirm</span></span>
<span data-ttu-id="4ac9f-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4ac9f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ac9f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ac9f-119">-WhatIf</span></span>
<span data-ttu-id="4ac9f-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4ac9f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ac9f-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4ac9f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ac9f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ac9f-122">CommonParameters</span></span>
<span data-ttu-id="4ac9f-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ac9f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ac9f-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ac9f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ac9f-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ac9f-125">INPUTS</span></span>

### <span data-ttu-id="4ac9f-126">System.String</span><span class="sxs-lookup"><span data-stu-id="4ac9f-126">System.String</span></span>

## <span data-ttu-id="4ac9f-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ac9f-127">OUTPUTS</span></span>

### <span data-ttu-id="4ac9f-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="4ac9f-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="4ac9f-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4ac9f-129">NOTES</span></span>

## <span data-ttu-id="4ac9f-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ac9f-130">RELATED LINKS</span></span>

[<span data-ttu-id="4ac9f-131">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="4ac9f-131">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="4ac9f-132">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="4ac9f-132">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="4ac9f-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4ac9f-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="4ac9f-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4ac9f-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="4ac9f-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4ac9f-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="4ac9f-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4ac9f-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)