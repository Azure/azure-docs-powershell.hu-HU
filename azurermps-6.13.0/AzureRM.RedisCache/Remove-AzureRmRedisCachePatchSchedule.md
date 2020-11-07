---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 7224e83333b281fac849ee9e5d99a0691aba3ccc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679147"
---
# <span data-ttu-id="a208a-101">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a208a-101">Remove-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="a208a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a208a-102">SYNOPSIS</span></span>
<span data-ttu-id="a208a-103">Eltávolítja a javítás ütemezését.</span><span class="sxs-lookup"><span data-stu-id="a208a-103">Removes the patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a208a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a208a-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a208a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a208a-105">DESCRIPTION</span></span>
<span data-ttu-id="a208a-106">A **Remove-AzureRmRedisCachePatchSchedule** parancsmag eltávolítja a javítás ütemezését egy gyorsítótárból az Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="a208a-106">The **Remove-AzureRmRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="a208a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a208a-107">EXAMPLES</span></span>

### <span data-ttu-id="a208a-108">1. példa: a javítás ütemezésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a208a-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="a208a-109">Ez a parancs eltávolítja a javítás ütemezését a RedisCache06 nevű gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="a208a-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="a208a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a208a-110">PARAMETERS</span></span>

### <span data-ttu-id="a208a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a208a-111">-DefaultProfile</span></span>
<span data-ttu-id="a208a-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a208a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a208a-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a208a-113">-Name</span></span>
<span data-ttu-id="a208a-114">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a208a-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="a208a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a208a-115">-PassThru</span></span>
<span data-ttu-id="a208a-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a208a-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a208a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a208a-117">-ResourceGroupName</span></span>
<span data-ttu-id="a208a-118">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a208a-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="a208a-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a208a-119">-Confirm</span></span>
<span data-ttu-id="a208a-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a208a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a208a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a208a-121">-WhatIf</span></span>
<span data-ttu-id="a208a-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a208a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a208a-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a208a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a208a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a208a-124">CommonParameters</span></span>
<span data-ttu-id="a208a-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a208a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a208a-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a208a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a208a-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a208a-127">INPUTS</span></span>

### <span data-ttu-id="a208a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a208a-128">System.String</span></span>

## <span data-ttu-id="a208a-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a208a-129">OUTPUTS</span></span>

### <span data-ttu-id="a208a-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a208a-130">System.Boolean</span></span>

## <span data-ttu-id="a208a-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a208a-131">NOTES</span></span>
* <span data-ttu-id="a208a-132">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="a208a-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="a208a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a208a-133">RELATED LINKS</span></span>

[<span data-ttu-id="a208a-134">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a208a-134">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="a208a-135">Új – AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a208a-135">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="a208a-136">Új – AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="a208a-136">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)


