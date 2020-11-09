---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
ms.openlocfilehash: 60c552b0878907c7b2c4a56d8068968c3ace862a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302635"
---
# <span data-ttu-id="f075c-101">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="f075c-101">Set-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="f075c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f075c-102">SYNOPSIS</span></span>
<span data-ttu-id="f075c-103">A diagnosztika engedélyezése Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="f075c-103">Enables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="f075c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f075c-104">SYNTAX</span></span>

```
Set-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f075c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f075c-105">DESCRIPTION</span></span>
<span data-ttu-id="f075c-106">A **set-AzRedisCacheDiagnostic** parancsmag engedélyezi az Azure Redis-gyorsítótár diagnosztizálását.</span><span class="sxs-lookup"><span data-stu-id="f075c-106">The **Set-AzRedisCacheDiagnostic** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="f075c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f075c-107">EXAMPLES</span></span>

### <span data-ttu-id="f075c-108">Példa 1: diagnosztika engedélyezése</span><span class="sxs-lookup"><span data-stu-id="f075c-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="f075c-109">Ez a parancs engedélyezi az Azure Redis-gyorsítótár diagnosztizálását.</span><span class="sxs-lookup"><span data-stu-id="f075c-109">This command enables diagnostics for an Azure Redis cache.</span></span>
<span data-ttu-id="f075c-110">Ez a parancs lehetővé teszi a diagnosztika engedélyezését vagy a tárolási fiók frissítését az összes Azure Redis-gyorsítótárhoz ugyanazon a régióban az előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="f075c-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="f075c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f075c-111">PARAMETERS</span></span>

### <span data-ttu-id="f075c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f075c-112">-DefaultProfile</span></span>
<span data-ttu-id="f075c-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f075c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f075c-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f075c-114">-Name</span></span>
<span data-ttu-id="f075c-115">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f075c-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="f075c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f075c-116">-ResourceGroupName</span></span>
<span data-ttu-id="f075c-117">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f075c-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="f075c-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f075c-118">-StorageAccountId</span></span>
<span data-ttu-id="f075c-119">A diagnosztikai adatainak tárolására használt tárolási fiók erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f075c-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="f075c-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f075c-120">-Confirm</span></span>
<span data-ttu-id="f075c-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f075c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f075c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f075c-122">-WhatIf</span></span>
<span data-ttu-id="f075c-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f075c-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f075c-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f075c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f075c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f075c-125">CommonParameters</span></span>
<span data-ttu-id="f075c-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f075c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f075c-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f075c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f075c-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f075c-128">INPUTS</span></span>

### <span data-ttu-id="f075c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f075c-129">System.String</span></span>

## <span data-ttu-id="f075c-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f075c-130">OUTPUTS</span></span>

### <span data-ttu-id="f075c-131">System. Void</span><span class="sxs-lookup"><span data-stu-id="f075c-131">System.Void</span></span>

## <span data-ttu-id="f075c-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f075c-132">NOTES</span></span>
* <span data-ttu-id="f075c-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="f075c-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="f075c-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f075c-134">RELATED LINKS</span></span>

[<span data-ttu-id="f075c-135">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="f075c-135">Remove-AzRedisCacheDiagnostic</span></span>](./Remove-AzRedisCacheDiagnostic.md)


