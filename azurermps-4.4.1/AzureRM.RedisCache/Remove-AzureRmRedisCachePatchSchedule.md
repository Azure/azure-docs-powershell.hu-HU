---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 768b37444155829ba33a5996fb969c21f85ca797
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493381"
---
# <span data-ttu-id="a01d2-101">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a01d2-101">Remove-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="a01d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a01d2-102">SYNOPSIS</span></span>
<span data-ttu-id="a01d2-103">Eltávolítja a javítás ütemezését.</span><span class="sxs-lookup"><span data-stu-id="a01d2-103">Removes the patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a01d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a01d2-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a01d2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a01d2-105">DESCRIPTION</span></span>
<span data-ttu-id="a01d2-106">A **Remove-AzureRmRedisCachePatchSchedule** parancsmag eltávolítja a javítás ütemezését egy gyorsítótárból az Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="a01d2-106">The **Remove-AzureRmRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="a01d2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a01d2-107">EXAMPLES</span></span>

### <span data-ttu-id="a01d2-108">1. példa: a javítás ütemezésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a01d2-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="a01d2-109">Ez a parancs eltávolítja a javítás ütemezését a RedisCache06 nevű gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="a01d2-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="a01d2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a01d2-110">PARAMETERS</span></span>

### <span data-ttu-id="a01d2-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a01d2-111">-Name</span></span>
<span data-ttu-id="a01d2-112">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a01d2-112">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="a01d2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a01d2-113">-ResourceGroupName</span></span>
<span data-ttu-id="a01d2-114">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a01d2-114">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="a01d2-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a01d2-115">-Confirm</span></span>
<span data-ttu-id="a01d2-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a01d2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a01d2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a01d2-117">-WhatIf</span></span>
<span data-ttu-id="a01d2-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a01d2-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a01d2-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a01d2-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a01d2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a01d2-120">-DefaultProfile</span></span>
<span data-ttu-id="a01d2-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a01d2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a01d2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a01d2-122">CommonParameters</span></span>
<span data-ttu-id="a01d2-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a01d2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a01d2-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a01d2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a01d2-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a01d2-125">INPUTS</span></span>

### <span data-ttu-id="a01d2-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="a01d2-126">None</span></span>
<span data-ttu-id="a01d2-127">A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="a01d2-127">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="a01d2-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a01d2-128">OUTPUTS</span></span>

### <span data-ttu-id="a01d2-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="a01d2-129">None</span></span>

## <span data-ttu-id="a01d2-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a01d2-130">NOTES</span></span>
* <span data-ttu-id="a01d2-131">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="a01d2-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="a01d2-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a01d2-132">RELATED LINKS</span></span>

[<span data-ttu-id="a01d2-133">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a01d2-133">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="a01d2-134">Új – AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a01d2-134">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="a01d2-135">Új – AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="a01d2-135">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)


