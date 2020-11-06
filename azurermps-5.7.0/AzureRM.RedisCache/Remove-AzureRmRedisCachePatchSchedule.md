---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: dab4333907d50853474ff795d33263846af249b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500436"
---
# <span data-ttu-id="930b5-101">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="930b5-101">Remove-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="930b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="930b5-102">SYNOPSIS</span></span>
<span data-ttu-id="930b5-103">Eltávolítja a javítás ütemezését.</span><span class="sxs-lookup"><span data-stu-id="930b5-103">Removes the patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="930b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="930b5-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="930b5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="930b5-105">DESCRIPTION</span></span>
<span data-ttu-id="930b5-106">A **Remove-AzureRmRedisCachePatchSchedule** parancsmag eltávolítja a javítás ütemezését egy gyorsítótárból az Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="930b5-106">The **Remove-AzureRmRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="930b5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="930b5-107">EXAMPLES</span></span>

### <span data-ttu-id="930b5-108">1. példa: a javítás ütemezésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="930b5-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="930b5-109">Ez a parancs eltávolítja a javítás ütemezését a RedisCache06 nevű gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="930b5-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="930b5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="930b5-110">PARAMETERS</span></span>

### <span data-ttu-id="930b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="930b5-111">-DefaultProfile</span></span>
<span data-ttu-id="930b5-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="930b5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="930b5-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="930b5-113">-Name</span></span>
<span data-ttu-id="930b5-114">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="930b5-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="930b5-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="930b5-115">-PassThru</span></span>
<span data-ttu-id="930b5-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="930b5-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="930b5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="930b5-117">-ResourceGroupName</span></span>
<span data-ttu-id="930b5-118">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="930b5-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="930b5-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="930b5-119">-Confirm</span></span>
<span data-ttu-id="930b5-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="930b5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="930b5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="930b5-121">-WhatIf</span></span>
<span data-ttu-id="930b5-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="930b5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="930b5-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="930b5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="930b5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="930b5-124">CommonParameters</span></span>
<span data-ttu-id="930b5-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="930b5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="930b5-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="930b5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="930b5-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="930b5-127">INPUTS</span></span>

### <span data-ttu-id="930b5-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="930b5-128">None</span></span>
<span data-ttu-id="930b5-129">A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="930b5-129">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="930b5-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="930b5-130">OUTPUTS</span></span>

### <span data-ttu-id="930b5-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="930b5-131">None</span></span>

## <span data-ttu-id="930b5-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="930b5-132">NOTES</span></span>
* <span data-ttu-id="930b5-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="930b5-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="930b5-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="930b5-134">RELATED LINKS</span></span>

[<span data-ttu-id="930b5-135">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="930b5-135">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="930b5-136">Új – AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="930b5-136">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="930b5-137">Új – AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="930b5-137">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)


