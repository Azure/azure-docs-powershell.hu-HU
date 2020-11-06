---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
ms.openlocfilehash: 103567021d7317a6777ca5fdb01c53d1f9f023a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503964"
---
# <span data-ttu-id="c6a19-101">Set-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="c6a19-101">Set-AzureRmRedisCacheDiagnostics</span></span>

## <span data-ttu-id="c6a19-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6a19-102">SYNOPSIS</span></span>
<span data-ttu-id="c6a19-103">A diagnosztika engedélyezése Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="c6a19-103">Enables diagnostics on an Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6a19-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6a19-104">SYNTAX</span></span>

```
Set-AzureRmRedisCacheDiagnostics -ResourceGroupName <String> -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6a19-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6a19-105">DESCRIPTION</span></span>
<span data-ttu-id="c6a19-106">A **set-AzureRmRedisCacheDiagnostics** parancsmag engedélyezi az Azure Redis-gyorsítótár diagnosztizálását.</span><span class="sxs-lookup"><span data-stu-id="c6a19-106">The **Set-AzureRmRedisCacheDiagnostics** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="c6a19-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c6a19-107">EXAMPLES</span></span>

### <span data-ttu-id="c6a19-108">Példa 1: diagnosztika engedélyezése</span><span class="sxs-lookup"><span data-stu-id="c6a19-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzureRmRedisCacheDiagnostics -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="c6a19-109">Ez a parancs engedélyezi az Azure Redis-gyorsítótár diagnosztizálását.</span><span class="sxs-lookup"><span data-stu-id="c6a19-109">This command enables diagnostics for an Azure Redis cache.</span></span>

<span data-ttu-id="c6a19-110">Ez a parancs lehetővé teszi a diagnosztika engedélyezését vagy a tárolási fiók frissítését az összes Azure Redis-gyorsítótárhoz ugyanazon a régióban az előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="c6a19-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="c6a19-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6a19-111">PARAMETERS</span></span>

### <span data-ttu-id="c6a19-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c6a19-112">-Name</span></span>
<span data-ttu-id="c6a19-113">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6a19-113">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="c6a19-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6a19-114">-ResourceGroupName</span></span>
<span data-ttu-id="c6a19-115">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6a19-115">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="c6a19-116">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c6a19-116">-StorageAccountId</span></span>
<span data-ttu-id="c6a19-117">A diagnosztikai adatainak tárolására használt tárolási fiók erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6a19-117">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="c6a19-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6a19-118">-DefaultProfile</span></span>
<span data-ttu-id="c6a19-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6a19-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6a19-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6a19-120">CommonParameters</span></span>
<span data-ttu-id="c6a19-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6a19-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6a19-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6a19-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6a19-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6a19-123">INPUTS</span></span>

### <span data-ttu-id="c6a19-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="c6a19-124">None</span></span>

## <span data-ttu-id="c6a19-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6a19-125">OUTPUTS</span></span>

### <span data-ttu-id="c6a19-126">Érték</span><span class="sxs-lookup"><span data-stu-id="c6a19-126">Void</span></span>

## <span data-ttu-id="c6a19-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6a19-127">NOTES</span></span>
* <span data-ttu-id="c6a19-128">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="c6a19-128">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="c6a19-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6a19-129">RELATED LINKS</span></span>

[<span data-ttu-id="c6a19-130">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="c6a19-130">Remove-AzureRmRedisCacheDiagnostics</span></span>](./Remove-AzureRmRedisCacheDiagnostics.md)


