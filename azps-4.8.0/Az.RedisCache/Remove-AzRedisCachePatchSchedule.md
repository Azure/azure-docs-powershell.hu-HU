---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 8e66391ff613578d1306543c626908763a932d06
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181458"
---
# <span data-ttu-id="a68a9-101">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a68a9-101">Remove-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="a68a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a68a9-102">SYNOPSIS</span></span>
<span data-ttu-id="a68a9-103">Eltávolítja a javítás ütemezését.</span><span class="sxs-lookup"><span data-stu-id="a68a9-103">Removes the patch schedule.</span></span>

## <span data-ttu-id="a68a9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a68a9-104">SYNTAX</span></span>

```
Remove-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a68a9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a68a9-105">DESCRIPTION</span></span>
<span data-ttu-id="a68a9-106">A **Remove-AzRedisCachePatchSchedule** parancsmag eltávolítja a javítás ütemezését egy gyorsítótárból az Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="a68a9-106">The **Remove-AzRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="a68a9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a68a9-107">EXAMPLES</span></span>

### <span data-ttu-id="a68a9-108">1. példa: a javítás ütemezésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a68a9-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="a68a9-109">Ez a parancs eltávolítja a javítás ütemezését a RedisCache06 nevű gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="a68a9-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="a68a9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a68a9-110">PARAMETERS</span></span>

### <span data-ttu-id="a68a9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a68a9-111">-DefaultProfile</span></span>
<span data-ttu-id="a68a9-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a68a9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a68a9-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a68a9-113">-Name</span></span>
<span data-ttu-id="a68a9-114">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a68a9-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="a68a9-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a68a9-115">-PassThru</span></span>
<span data-ttu-id="a68a9-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a68a9-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a68a9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a68a9-117">-ResourceGroupName</span></span>
<span data-ttu-id="a68a9-118">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a68a9-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="a68a9-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a68a9-119">-Confirm</span></span>
<span data-ttu-id="a68a9-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a68a9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a68a9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a68a9-121">-WhatIf</span></span>
<span data-ttu-id="a68a9-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a68a9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a68a9-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a68a9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a68a9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a68a9-124">CommonParameters</span></span>
<span data-ttu-id="a68a9-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a68a9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a68a9-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a68a9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a68a9-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a68a9-127">INPUTS</span></span>

### <span data-ttu-id="a68a9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a68a9-128">System.String</span></span>

## <span data-ttu-id="a68a9-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a68a9-129">OUTPUTS</span></span>

### <span data-ttu-id="a68a9-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a68a9-130">System.Boolean</span></span>

## <span data-ttu-id="a68a9-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a68a9-131">NOTES</span></span>
* <span data-ttu-id="a68a9-132">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="a68a9-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="a68a9-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a68a9-133">RELATED LINKS</span></span>

[<span data-ttu-id="a68a9-134">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a68a9-134">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="a68a9-135">Új – AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a68a9-135">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="a68a9-136">Új – AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="a68a9-136">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)


