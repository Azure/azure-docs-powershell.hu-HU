---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
ms.openlocfilehash: b309875fd330df5695283c187e454556669b6652
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846930"
---
# <span data-ttu-id="d674b-101">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d674b-101">Remove-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="d674b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d674b-102">SYNOPSIS</span></span>
<span data-ttu-id="d674b-103">Letiltja a diagnosztikát az Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="d674b-103">Disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="d674b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d674b-104">SYNTAX</span></span>

```
Remove-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d674b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d674b-105">DESCRIPTION</span></span>
<span data-ttu-id="d674b-106">A **Remove-AzRedisCacheDiagnostic** parancsmag letiltja a diagnosztikát egy Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="d674b-106">The **Remove-AzRedisCacheDiagnostic** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="d674b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d674b-107">EXAMPLES</span></span>

### <span data-ttu-id="d674b-108">1. példa: a diagnosztika letiltása</span><span class="sxs-lookup"><span data-stu-id="d674b-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="d674b-109">Ez a parancs letiltja a diagnosztikát a megadott Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="d674b-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>
<span data-ttu-id="d674b-110">Ez letiltja a diagnosztikát az összes Azure Redis-gyorsítótárhoz az előfizetéshez tartozó régióban.</span><span class="sxs-lookup"><span data-stu-id="d674b-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="d674b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d674b-111">PARAMETERS</span></span>

### <span data-ttu-id="d674b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d674b-112">-DefaultProfile</span></span>
<span data-ttu-id="d674b-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d674b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d674b-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d674b-114">-Name</span></span>
<span data-ttu-id="d674b-115">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d674b-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="d674b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d674b-116">-ResourceGroupName</span></span>
<span data-ttu-id="d674b-117">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d674b-117">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d674b-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d674b-118">-Confirm</span></span>
<span data-ttu-id="d674b-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d674b-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d674b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d674b-120">-WhatIf</span></span>
<span data-ttu-id="d674b-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d674b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d674b-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d674b-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d674b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d674b-123">CommonParameters</span></span>
<span data-ttu-id="d674b-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d674b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d674b-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d674b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d674b-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d674b-126">INPUTS</span></span>

### <span data-ttu-id="d674b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d674b-127">System.String</span></span>

## <span data-ttu-id="d674b-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d674b-128">OUTPUTS</span></span>

### <span data-ttu-id="d674b-129">System. Void</span><span class="sxs-lookup"><span data-stu-id="d674b-129">System.Void</span></span>

## <span data-ttu-id="d674b-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d674b-130">NOTES</span></span>
* <span data-ttu-id="d674b-131">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="d674b-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="d674b-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d674b-132">RELATED LINKS</span></span>

[<span data-ttu-id="d674b-133">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d674b-133">Set-AzRedisCacheDiagnostic</span></span>](./Set-AzRedisCacheDiagnostic.md)


