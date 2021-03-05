---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 9033082093d571fc60cd9b4c495688d11d87aea8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000805"
---
# <span data-ttu-id="2e4f9-101">Get-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="2e4f9-101">Get-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="2e4f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e4f9-102">SYNOPSIS</span></span>
<span data-ttu-id="2e4f9-103">Információkat kap egy RedisEnterprise fürtben található adatbázisról.</span><span class="sxs-lookup"><span data-stu-id="2e4f9-103">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="2e4f9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2e4f9-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2e4f9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2e4f9-105">DESCRIPTION</span></span>
<span data-ttu-id="2e4f9-106">Információkat kap egy RedisEnterprise fürtben található adatbázisról.</span><span class="sxs-lookup"><span data-stu-id="2e4f9-106">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="2e4f9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2e4f9-107">EXAMPLES</span></span>

### <span data-ttu-id="2e4f9-108">1. példa: Adatbázis lekérte</span><span class="sxs-lookup"><span data-stu-id="2e4f9-108">Example 1: Get database</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="2e4f9-109">Ez a parancs a MyCache nevű Redis Enterprise Cache adatbázisát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2e4f9-109">This command gets the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="2e4f9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e4f9-110">PARAMETERS</span></span>

### <span data-ttu-id="2e4f9-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2e4f9-111">-ClusterName</span></span>
<span data-ttu-id="2e4f9-112">A RedisEnterprise fürt neve.</span><span class="sxs-lookup"><span data-stu-id="2e4f9-112">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e4f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e4f9-113">-DefaultProfile</span></span>
<span data-ttu-id="2e4f9-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e4f9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e4f9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e4f9-115">-ResourceGroupName</span></span>
<span data-ttu-id="2e4f9-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2e4f9-116">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e4f9-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2e4f9-117">-SubscriptionId</span></span>
<span data-ttu-id="2e4f9-118">Olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="2e4f9-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2e4f9-119">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="2e4f9-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e4f9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e4f9-120">CommonParameters</span></span>
<span data-ttu-id="2e4f9-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e4f9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e4f9-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e4f9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e4f9-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e4f9-123">INPUTS</span></span>

## <span data-ttu-id="2e4f9-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e4f9-124">OUTPUTS</span></span>

### <span data-ttu-id="2e4f9-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span><span class="sxs-lookup"><span data-stu-id="2e4f9-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="2e4f9-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2e4f9-126">NOTES</span></span>

<span data-ttu-id="2e4f9-127">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="2e4f9-127">ALIASES</span></span>

## <span data-ttu-id="2e4f9-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e4f9-128">RELATED LINKS</span></span>

