---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
ms.openlocfilehash: b309875fd330df5695283c187e454556669b6652
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182697"
---
# <span data-ttu-id="34cd8-101">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="34cd8-101">Remove-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="34cd8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="34cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="34cd8-103">Letiltja a diagnosztikát az Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="34cd8-103">Disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="34cd8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="34cd8-104">SYNTAX</span></span>

```
Remove-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34cd8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="34cd8-105">DESCRIPTION</span></span>
<span data-ttu-id="34cd8-106">A **Remove-AzRedisCacheDiagnostic** parancsmag letiltja a diagnosztikát egy Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="34cd8-106">The **Remove-AzRedisCacheDiagnostic** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="34cd8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="34cd8-107">EXAMPLES</span></span>

### <span data-ttu-id="34cd8-108">1. példa: a diagnosztika letiltása</span><span class="sxs-lookup"><span data-stu-id="34cd8-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="34cd8-109">Ez a parancs letiltja a diagnosztikát a megadott Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="34cd8-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>
<span data-ttu-id="34cd8-110">Ez letiltja a diagnosztikát az összes Azure Redis-gyorsítótárhoz az előfizetéshez tartozó régióban.</span><span class="sxs-lookup"><span data-stu-id="34cd8-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="34cd8-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="34cd8-111">PARAMETERS</span></span>

### <span data-ttu-id="34cd8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34cd8-112">-DefaultProfile</span></span>
<span data-ttu-id="34cd8-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="34cd8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34cd8-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="34cd8-114">-Name</span></span>
<span data-ttu-id="34cd8-115">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="34cd8-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="34cd8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34cd8-116">-ResourceGroupName</span></span>
<span data-ttu-id="34cd8-117">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="34cd8-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="34cd8-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="34cd8-118">-Confirm</span></span>
<span data-ttu-id="34cd8-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="34cd8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34cd8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34cd8-120">-WhatIf</span></span>
<span data-ttu-id="34cd8-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="34cd8-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34cd8-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="34cd8-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34cd8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34cd8-123">CommonParameters</span></span>
<span data-ttu-id="34cd8-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="34cd8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34cd8-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34cd8-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34cd8-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="34cd8-126">INPUTS</span></span>

### <span data-ttu-id="34cd8-127">System. String</span><span class="sxs-lookup"><span data-stu-id="34cd8-127">System.String</span></span>

## <span data-ttu-id="34cd8-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="34cd8-128">OUTPUTS</span></span>

### <span data-ttu-id="34cd8-129">System. Void</span><span class="sxs-lookup"><span data-stu-id="34cd8-129">System.Void</span></span>

## <span data-ttu-id="34cd8-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="34cd8-130">NOTES</span></span>
* <span data-ttu-id="34cd8-131">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="34cd8-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="34cd8-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="34cd8-132">RELATED LINKS</span></span>

[<span data-ttu-id="34cd8-133">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="34cd8-133">Set-AzRedisCacheDiagnostic</span></span>](./Set-AzRedisCacheDiagnostic.md)


