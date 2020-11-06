---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachediagnostics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheDiagnostics.md
ms.openlocfilehash: fca64401f4671db63d76d491476f0e276e92055a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498879"
---
# <span data-ttu-id="0e0c5-101">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0e0c5-101">Remove-AzureRmRedisCacheDiagnostics</span></span>

## <span data-ttu-id="0e0c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0e0c5-102">SYNOPSIS</span></span>
<span data-ttu-id="0e0c5-103">Letiltja a diagnosztikát az Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="0e0c5-103">Disables diagnostics on an Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e0c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0e0c5-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCacheDiagnostics [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e0c5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0e0c5-105">DESCRIPTION</span></span>
<span data-ttu-id="0e0c5-106">A **Remove-AzureRmRedisCacheDiagnostics** parancsmag letiltja a diagnosztikát egy Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="0e0c5-106">The **Remove-AzureRmRedisCacheDiagnostics** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="0e0c5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0e0c5-107">EXAMPLES</span></span>

### <span data-ttu-id="0e0c5-108">1. példa: a diagnosztika letiltása</span><span class="sxs-lookup"><span data-stu-id="0e0c5-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzureRmRedisCacheDiagnostics -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="0e0c5-109">Ez a parancs letiltja a diagnosztikát a megadott Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="0e0c5-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>

<span data-ttu-id="0e0c5-110">Ez letiltja a diagnosztikát az összes Azure Redis-gyorsítótárhoz az előfizetéshez tartozó régióban.</span><span class="sxs-lookup"><span data-stu-id="0e0c5-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="0e0c5-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0e0c5-111">PARAMETERS</span></span>

### <span data-ttu-id="0e0c5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e0c5-112">-DefaultProfile</span></span>
<span data-ttu-id="0e0c5-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0e0c5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e0c5-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0e0c5-114">-Name</span></span>
<span data-ttu-id="0e0c5-115">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e0c5-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="0e0c5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e0c5-116">-ResourceGroupName</span></span>
<span data-ttu-id="0e0c5-117">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e0c5-117">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e0c5-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0e0c5-118">-Confirm</span></span>
<span data-ttu-id="0e0c5-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0e0c5-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e0c5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e0c5-120">-WhatIf</span></span>
<span data-ttu-id="0e0c5-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0e0c5-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e0c5-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0e0c5-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e0c5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e0c5-123">CommonParameters</span></span>
<span data-ttu-id="0e0c5-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0e0c5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e0c5-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e0c5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e0c5-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e0c5-126">INPUTS</span></span>

### <span data-ttu-id="0e0c5-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="0e0c5-127">None</span></span>

## <span data-ttu-id="0e0c5-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e0c5-128">OUTPUTS</span></span>

### <span data-ttu-id="0e0c5-129">Érték</span><span class="sxs-lookup"><span data-stu-id="0e0c5-129">Void</span></span>

## <span data-ttu-id="0e0c5-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0e0c5-130">NOTES</span></span>
* <span data-ttu-id="0e0c5-131">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="0e0c5-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="0e0c5-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e0c5-132">RELATED LINKS</span></span>

[<span data-ttu-id="0e0c5-133">Set-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0e0c5-133">Set-AzureRmRedisCacheDiagnostics</span></span>](./Set-AzureRmRedisCacheDiagnostics.md)


