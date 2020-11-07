---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 091d3d52da1319842d221881f03fca2b21353fa9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672146"
---
# <span data-ttu-id="495e8-101">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="495e8-101">Get-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="495e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="495e8-102">SYNOPSIS</span></span>
<span data-ttu-id="495e8-103">Egy javítócsomag-ütemezést kap.</span><span class="sxs-lookup"><span data-stu-id="495e8-103">Gets a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="495e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="495e8-104">SYNTAX</span></span>

```
Get-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="495e8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="495e8-105">DESCRIPTION</span></span>
<span data-ttu-id="495e8-106">A **Get-AzureRmRedisCachePatchSchedule** parancsmag kijavítási ütemtervet kap az Azure Redis-gyorsítótárban lévő gyorsítótárhoz.</span><span class="sxs-lookup"><span data-stu-id="495e8-106">The **Get-AzureRmRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="495e8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="495e8-107">EXAMPLES</span></span>

### <span data-ttu-id="495e8-108">Példa 1: a javítócsomag-ütemezés beszerzése</span><span class="sxs-lookup"><span data-stu-id="495e8-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="495e8-109">Ez a parancs a RedisCache06 nevű gyorsítótárból kapja meg a javítás ütemezését.</span><span class="sxs-lookup"><span data-stu-id="495e8-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="495e8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="495e8-110">PARAMETERS</span></span>

### <span data-ttu-id="495e8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="495e8-111">-DefaultProfile</span></span>
<span data-ttu-id="495e8-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="495e8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="495e8-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="495e8-113">-Name</span></span>
<span data-ttu-id="495e8-114">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="495e8-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="495e8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="495e8-115">-ResourceGroupName</span></span>
<span data-ttu-id="495e8-116">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="495e8-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="495e8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="495e8-117">CommonParameters</span></span>
<span data-ttu-id="495e8-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="495e8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="495e8-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="495e8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="495e8-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="495e8-120">INPUTS</span></span>

### <span data-ttu-id="495e8-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="495e8-121">None</span></span>
<span data-ttu-id="495e8-122">A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="495e8-122">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="495e8-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="495e8-123">OUTPUTS</span></span>

### <span data-ttu-id="495e8-124">Microsoft. Azure. Command. RedisCache. models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="495e8-124">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="495e8-125">Ez a parancsmag a gyorsítótárban beállított javítócsomag-ütemezési bejegyzéseket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="495e8-125">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="495e8-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="495e8-126">NOTES</span></span>
* <span data-ttu-id="495e8-127">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="495e8-127">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="495e8-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="495e8-128">RELATED LINKS</span></span>

[<span data-ttu-id="495e8-129">Új – AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="495e8-129">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="495e8-130">Új – AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="495e8-130">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="495e8-131">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="495e8-131">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


