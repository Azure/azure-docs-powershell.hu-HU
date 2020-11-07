---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 83fab07a44dd85e000e86597881341cad6c641e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669527"
---
# <span data-ttu-id="a92fc-101">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a92fc-101">Remove-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="a92fc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a92fc-102">SYNOPSIS</span></span>
<span data-ttu-id="a92fc-103">Eltávolítja a javítás ütemezését.</span><span class="sxs-lookup"><span data-stu-id="a92fc-103">Removes the patch schedule.</span></span>

## <span data-ttu-id="a92fc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a92fc-104">SYNTAX</span></span>

```
Remove-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a92fc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a92fc-105">DESCRIPTION</span></span>
<span data-ttu-id="a92fc-106">A **Remove-AzRedisCachePatchSchedule** parancsmag eltávolítja a javítás ütemezését egy gyorsítótárból az Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="a92fc-106">The **Remove-AzRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="a92fc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a92fc-107">EXAMPLES</span></span>

### <span data-ttu-id="a92fc-108">1. példa: a javítás ütemezésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a92fc-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="a92fc-109">Ez a parancs eltávolítja a javítás ütemezését a RedisCache06 nevű gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="a92fc-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="a92fc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a92fc-110">PARAMETERS</span></span>

### <span data-ttu-id="a92fc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a92fc-111">-DefaultProfile</span></span>
<span data-ttu-id="a92fc-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a92fc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a92fc-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a92fc-113">-Name</span></span>
<span data-ttu-id="a92fc-114">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a92fc-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="a92fc-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a92fc-115">-PassThru</span></span>
<span data-ttu-id="a92fc-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a92fc-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a92fc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a92fc-117">-ResourceGroupName</span></span>
<span data-ttu-id="a92fc-118">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a92fc-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="a92fc-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a92fc-119">-Confirm</span></span>
<span data-ttu-id="a92fc-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a92fc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a92fc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a92fc-121">-WhatIf</span></span>
<span data-ttu-id="a92fc-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a92fc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a92fc-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a92fc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a92fc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a92fc-124">CommonParameters</span></span>
<span data-ttu-id="a92fc-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a92fc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a92fc-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a92fc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a92fc-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a92fc-127">INPUTS</span></span>

### <span data-ttu-id="a92fc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a92fc-128">System.String</span></span>

## <span data-ttu-id="a92fc-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a92fc-129">OUTPUTS</span></span>

### <span data-ttu-id="a92fc-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a92fc-130">System.Boolean</span></span>

## <span data-ttu-id="a92fc-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a92fc-131">NOTES</span></span>
* <span data-ttu-id="a92fc-132">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="a92fc-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="a92fc-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a92fc-133">RELATED LINKS</span></span>

[<span data-ttu-id="a92fc-134">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a92fc-134">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="a92fc-135">Új – AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a92fc-135">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="a92fc-136">Új – AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="a92fc-136">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)


