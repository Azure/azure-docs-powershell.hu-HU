---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
ms.openlocfilehash: 60c552b0878907c7b2c4a56d8068968c3ace862a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181457"
---
# <span data-ttu-id="8e046-101">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8e046-101">Set-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="8e046-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e046-102">SYNOPSIS</span></span>
<span data-ttu-id="8e046-103">A diagnosztika engedélyezése Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="8e046-103">Enables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="8e046-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e046-104">SYNTAX</span></span>

```
Set-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e046-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e046-105">DESCRIPTION</span></span>
<span data-ttu-id="8e046-106">A **set-AzRedisCacheDiagnostic** parancsmag engedélyezi az Azure Redis-gyorsítótár diagnosztizálását.</span><span class="sxs-lookup"><span data-stu-id="8e046-106">The **Set-AzRedisCacheDiagnostic** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="8e046-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8e046-107">EXAMPLES</span></span>

### <span data-ttu-id="8e046-108">Példa 1: diagnosztika engedélyezése</span><span class="sxs-lookup"><span data-stu-id="8e046-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="8e046-109">Ez a parancs engedélyezi az Azure Redis-gyorsítótár diagnosztizálását.</span><span class="sxs-lookup"><span data-stu-id="8e046-109">This command enables diagnostics for an Azure Redis cache.</span></span>
<span data-ttu-id="8e046-110">Ez a parancs lehetővé teszi a diagnosztika engedélyezését vagy a tárolási fiók frissítését az összes Azure Redis-gyorsítótárhoz ugyanazon a régióban az előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="8e046-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="8e046-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e046-111">PARAMETERS</span></span>

### <span data-ttu-id="8e046-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e046-112">-DefaultProfile</span></span>
<span data-ttu-id="8e046-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e046-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e046-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8e046-114">-Name</span></span>
<span data-ttu-id="8e046-115">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e046-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="8e046-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e046-116">-ResourceGroupName</span></span>
<span data-ttu-id="8e046-117">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e046-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="8e046-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8e046-118">-StorageAccountId</span></span>
<span data-ttu-id="8e046-119">A diagnosztikai adatainak tárolására használt tárolási fiók erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e046-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="8e046-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8e046-120">-Confirm</span></span>
<span data-ttu-id="8e046-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8e046-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e046-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e046-122">-WhatIf</span></span>
<span data-ttu-id="8e046-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8e046-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e046-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e046-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e046-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e046-125">CommonParameters</span></span>
<span data-ttu-id="8e046-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e046-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e046-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e046-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e046-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e046-128">INPUTS</span></span>

### <span data-ttu-id="8e046-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8e046-129">System.String</span></span>

## <span data-ttu-id="8e046-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e046-130">OUTPUTS</span></span>

### <span data-ttu-id="8e046-131">System. Void</span><span class="sxs-lookup"><span data-stu-id="8e046-131">System.Void</span></span>

## <span data-ttu-id="8e046-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e046-132">NOTES</span></span>
* <span data-ttu-id="8e046-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="8e046-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="8e046-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e046-134">RELATED LINKS</span></span>

[<span data-ttu-id="8e046-135">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8e046-135">Remove-AzRedisCacheDiagnostic</span></span>](./Remove-AzRedisCacheDiagnostic.md)


