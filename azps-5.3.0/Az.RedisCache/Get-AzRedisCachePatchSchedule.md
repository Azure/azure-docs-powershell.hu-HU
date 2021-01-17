---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 0e63f8e5f427a251db13c76f915dc615f259defc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466631"
---
# <span data-ttu-id="dfa26-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="dfa26-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="dfa26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfa26-102">SYNOPSIS</span></span>
<span data-ttu-id="dfa26-103">Javításütemtervet kap.</span><span class="sxs-lookup"><span data-stu-id="dfa26-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="dfa26-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dfa26-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfa26-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dfa26-105">DESCRIPTION</span></span>
<span data-ttu-id="dfa26-106">A **Get-AzRedisCachePatchSchedule** parancsmag javításütemtervet kap az Azure Redis Cache gyorsítótárában lévő gyorsítótárhoz.</span><span class="sxs-lookup"><span data-stu-id="dfa26-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="dfa26-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dfa26-107">EXAMPLES</span></span>

### <span data-ttu-id="dfa26-108">1. példa: A javítás ütemezésének lekérte</span><span class="sxs-lookup"><span data-stu-id="dfa26-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="dfa26-109">Ez a parancs a Javítás ütemezését a RedisCache06 nevű gyorsítótárból kapja.</span><span class="sxs-lookup"><span data-stu-id="dfa26-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="dfa26-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfa26-110">PARAMETERS</span></span>

### <span data-ttu-id="dfa26-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfa26-111">-DefaultProfile</span></span>
<span data-ttu-id="dfa26-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dfa26-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfa26-113">-Name</span><span class="sxs-lookup"><span data-stu-id="dfa26-113">-Name</span></span>
<span data-ttu-id="dfa26-114">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dfa26-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="dfa26-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfa26-115">-ResourceGroupName</span></span>
<span data-ttu-id="dfa26-116">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dfa26-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="dfa26-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfa26-117">CommonParameters</span></span>
<span data-ttu-id="dfa26-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfa26-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfa26-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfa26-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfa26-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dfa26-120">INPUTS</span></span>

### <span data-ttu-id="dfa26-121">System.String</span><span class="sxs-lookup"><span data-stu-id="dfa26-121">System.String</span></span>

## <span data-ttu-id="dfa26-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfa26-122">OUTPUTS</span></span>

### <span data-ttu-id="dfa26-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="dfa26-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="dfa26-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dfa26-124">NOTES</span></span>
* <span data-ttu-id="dfa26-125">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, redis, cache, web, webapp, webhely</span><span class="sxs-lookup"><span data-stu-id="dfa26-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="dfa26-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dfa26-126">RELATED LINKS</span></span>

[<span data-ttu-id="dfa26-127">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="dfa26-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="dfa26-128">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="dfa26-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="dfa26-129">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="dfa26-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


