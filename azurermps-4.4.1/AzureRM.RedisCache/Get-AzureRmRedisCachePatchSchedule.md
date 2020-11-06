---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 1899a35f183f66fb938abe0c6492e826ad661e43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504772"
---
# <span data-ttu-id="05d61-101">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="05d61-101">Get-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="05d61-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="05d61-102">SYNOPSIS</span></span>
<span data-ttu-id="05d61-103">Egy javítócsomag-ütemezést kap.</span><span class="sxs-lookup"><span data-stu-id="05d61-103">Gets a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05d61-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="05d61-104">SYNTAX</span></span>

```
Get-AzureRmRedisCachePatchSchedule -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05d61-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="05d61-105">DESCRIPTION</span></span>
<span data-ttu-id="05d61-106">A **Get-AzureRmRedisCachePatchSchedule** parancsmag kijavítási ütemtervet kap az Azure Redis-gyorsítótárban lévő gyorsítótárhoz.</span><span class="sxs-lookup"><span data-stu-id="05d61-106">The **Get-AzureRmRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="05d61-107">Példák</span><span class="sxs-lookup"><span data-stu-id="05d61-107">EXAMPLES</span></span>

### <span data-ttu-id="05d61-108">Példa 1: a javítócsomag-ütemezés beszerzése</span><span class="sxs-lookup"><span data-stu-id="05d61-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="05d61-109">Ez a parancs a RedisCache06 nevű gyorsítótárból kapja meg a javítás ütemezését.</span><span class="sxs-lookup"><span data-stu-id="05d61-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="05d61-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="05d61-110">PARAMETERS</span></span>

### <span data-ttu-id="05d61-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="05d61-111">-Name</span></span>
<span data-ttu-id="05d61-112">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="05d61-112">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="05d61-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05d61-113">-ResourceGroupName</span></span>
<span data-ttu-id="05d61-114">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="05d61-114">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="05d61-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05d61-115">-DefaultProfile</span></span>
<span data-ttu-id="05d61-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="05d61-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05d61-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05d61-117">CommonParameters</span></span>
<span data-ttu-id="05d61-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="05d61-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05d61-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05d61-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05d61-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="05d61-120">INPUTS</span></span>

### <span data-ttu-id="05d61-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="05d61-121">None</span></span>
<span data-ttu-id="05d61-122">A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="05d61-122">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="05d61-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05d61-123">OUTPUTS</span></span>

### <span data-ttu-id="05d61-124">Microsoft. Azure. Command. RedisCache. models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="05d61-124">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="05d61-125">Ez a parancsmag a gyorsítótárban beállított javítócsomag-ütemezési bejegyzéseket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="05d61-125">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="05d61-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="05d61-126">NOTES</span></span>
* <span data-ttu-id="05d61-127">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="05d61-127">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="05d61-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05d61-128">RELATED LINKS</span></span>

[<span data-ttu-id="05d61-129">Új – AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="05d61-129">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="05d61-130">Új – AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="05d61-130">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="05d61-131">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="05d61-131">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


