---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 0e63f8e5f427a251db13c76f915dc615f259defc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182904"
---
# <span data-ttu-id="b215c-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="b215c-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="b215c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b215c-102">SYNOPSIS</span></span>
<span data-ttu-id="b215c-103">Egy javítócsomag-ütemezést kap.</span><span class="sxs-lookup"><span data-stu-id="b215c-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="b215c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b215c-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b215c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b215c-105">DESCRIPTION</span></span>
<span data-ttu-id="b215c-106">A **Get-AzRedisCachePatchSchedule** parancsmag kijavítási ütemtervet kap az Azure Redis-gyorsítótárban lévő gyorsítótárhoz.</span><span class="sxs-lookup"><span data-stu-id="b215c-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="b215c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b215c-107">EXAMPLES</span></span>

### <span data-ttu-id="b215c-108">Példa 1: a javítócsomag-ütemezés beszerzése</span><span class="sxs-lookup"><span data-stu-id="b215c-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="b215c-109">Ez a parancs a RedisCache06 nevű gyorsítótárból kapja meg a javítás ütemezését.</span><span class="sxs-lookup"><span data-stu-id="b215c-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="b215c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b215c-110">PARAMETERS</span></span>

### <span data-ttu-id="b215c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b215c-111">-DefaultProfile</span></span>
<span data-ttu-id="b215c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b215c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b215c-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b215c-113">-Name</span></span>
<span data-ttu-id="b215c-114">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b215c-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="b215c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b215c-115">-ResourceGroupName</span></span>
<span data-ttu-id="b215c-116">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b215c-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="b215c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b215c-117">CommonParameters</span></span>
<span data-ttu-id="b215c-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b215c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b215c-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b215c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b215c-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b215c-120">INPUTS</span></span>

### <span data-ttu-id="b215c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b215c-121">System.String</span></span>

## <span data-ttu-id="b215c-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b215c-122">OUTPUTS</span></span>

### <span data-ttu-id="b215c-123">Microsoft. Azure. Command. RedisCache. models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="b215c-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="b215c-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b215c-124">NOTES</span></span>
* <span data-ttu-id="b215c-125">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="b215c-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="b215c-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b215c-126">RELATED LINKS</span></span>

[<span data-ttu-id="b215c-127">Új – AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="b215c-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="b215c-128">Új – AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="b215c-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="b215c-129">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="b215c-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


