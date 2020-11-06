---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscachediagnostics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
ms.openlocfilehash: bab40aec2cd4a03d013f2c215f1baaaead3dc51e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492201"
---
# <span data-ttu-id="781b2-101">Set-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="781b2-101">Set-AzureRmRedisCacheDiagnostics</span></span>

## <span data-ttu-id="781b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="781b2-102">SYNOPSIS</span></span>
<span data-ttu-id="781b2-103">A diagnosztika engedélyezése Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="781b2-103">Enables diagnostics on an Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="781b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="781b2-104">SYNTAX</span></span>

```
Set-AzureRmRedisCacheDiagnostics [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="781b2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="781b2-105">DESCRIPTION</span></span>
<span data-ttu-id="781b2-106">A **set-AzureRmRedisCacheDiagnostics** parancsmag engedélyezi az Azure Redis-gyorsítótár diagnosztizálását.</span><span class="sxs-lookup"><span data-stu-id="781b2-106">The **Set-AzureRmRedisCacheDiagnostics** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="781b2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="781b2-107">EXAMPLES</span></span>

### <span data-ttu-id="781b2-108">Példa 1: diagnosztika engedélyezése</span><span class="sxs-lookup"><span data-stu-id="781b2-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzureRmRedisCacheDiagnostics -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="781b2-109">Ez a parancs engedélyezi az Azure Redis-gyorsítótár diagnosztizálását.</span><span class="sxs-lookup"><span data-stu-id="781b2-109">This command enables diagnostics for an Azure Redis cache.</span></span>

<span data-ttu-id="781b2-110">Ez a parancs lehetővé teszi a diagnosztika engedélyezését vagy a tárolási fiók frissítését az összes Azure Redis-gyorsítótárhoz ugyanazon a régióban az előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="781b2-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="781b2-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="781b2-111">PARAMETERS</span></span>

### <span data-ttu-id="781b2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="781b2-112">-DefaultProfile</span></span>
<span data-ttu-id="781b2-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="781b2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="781b2-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="781b2-114">-Name</span></span>
<span data-ttu-id="781b2-115">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="781b2-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="781b2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="781b2-116">-ResourceGroupName</span></span>
<span data-ttu-id="781b2-117">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="781b2-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="781b2-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="781b2-118">-StorageAccountId</span></span>
<span data-ttu-id="781b2-119">A diagnosztikai adatainak tárolására használt tárolási fiók erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="781b2-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="781b2-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="781b2-120">-Confirm</span></span>
<span data-ttu-id="781b2-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="781b2-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="781b2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="781b2-122">-WhatIf</span></span>
<span data-ttu-id="781b2-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="781b2-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="781b2-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="781b2-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="781b2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="781b2-125">CommonParameters</span></span>
<span data-ttu-id="781b2-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="781b2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="781b2-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="781b2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="781b2-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="781b2-128">INPUTS</span></span>

### <span data-ttu-id="781b2-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="781b2-129">None</span></span>

## <span data-ttu-id="781b2-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="781b2-130">OUTPUTS</span></span>

### <span data-ttu-id="781b2-131">Érték</span><span class="sxs-lookup"><span data-stu-id="781b2-131">Void</span></span>

## <span data-ttu-id="781b2-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="781b2-132">NOTES</span></span>
* <span data-ttu-id="781b2-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="781b2-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="781b2-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="781b2-134">RELATED LINKS</span></span>

[<span data-ttu-id="781b2-135">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="781b2-135">Remove-AzureRmRedisCacheDiagnostics</span></span>](./Remove-AzureRmRedisCacheDiagnostics.md)


