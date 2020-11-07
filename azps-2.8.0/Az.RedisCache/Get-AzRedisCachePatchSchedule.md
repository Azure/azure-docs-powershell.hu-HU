---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 6b2fbc3f28b34e1c71f8093953c54c107f4a0357
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838226"
---
# <span data-ttu-id="2d849-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="2d849-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="2d849-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d849-102">SYNOPSIS</span></span>
<span data-ttu-id="2d849-103">Egy javítócsomag-ütemezést kap.</span><span class="sxs-lookup"><span data-stu-id="2d849-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="2d849-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d849-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d849-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d849-105">DESCRIPTION</span></span>
<span data-ttu-id="2d849-106">A **Get-AzRedisCachePatchSchedule** parancsmag kijavítási ütemtervet kap az Azure Redis-gyorsítótárban lévő gyorsítótárhoz.</span><span class="sxs-lookup"><span data-stu-id="2d849-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="2d849-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2d849-107">EXAMPLES</span></span>

### <span data-ttu-id="2d849-108">Példa 1: a javítócsomag-ütemezés beszerzése</span><span class="sxs-lookup"><span data-stu-id="2d849-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="2d849-109">Ez a parancs a RedisCache06 nevű gyorsítótárból kapja meg a javítás ütemezését.</span><span class="sxs-lookup"><span data-stu-id="2d849-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="2d849-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d849-110">PARAMETERS</span></span>

### <span data-ttu-id="2d849-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d849-111">-DefaultProfile</span></span>
<span data-ttu-id="2d849-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2d849-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d849-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2d849-113">-Name</span></span>
<span data-ttu-id="2d849-114">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d849-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="2d849-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d849-115">-ResourceGroupName</span></span>
<span data-ttu-id="2d849-116">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d849-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="2d849-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d849-117">CommonParameters</span></span>
<span data-ttu-id="2d849-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d849-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d849-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d849-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d849-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d849-120">INPUTS</span></span>

### <span data-ttu-id="2d849-121">System. String</span><span class="sxs-lookup"><span data-stu-id="2d849-121">System.String</span></span>

## <span data-ttu-id="2d849-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d849-122">OUTPUTS</span></span>

### <span data-ttu-id="2d849-123">Microsoft. Azure. Command. RedisCache. models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="2d849-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="2d849-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d849-124">NOTES</span></span>
* <span data-ttu-id="2d849-125">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="2d849-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="2d849-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d849-126">RELATED LINKS</span></span>

[<span data-ttu-id="2d849-127">Új – AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="2d849-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="2d849-128">Új – AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="2d849-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="2d849-129">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="2d849-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


