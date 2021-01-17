---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
ms.openlocfilehash: a6fe478aa8221060974f54e75b63a64edf0beae4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466596"
---
# <span data-ttu-id="a5d44-101">Get-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="a5d44-101">Get-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="a5d44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5d44-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d44-103">Információt kap egy RedisEnterprise fürtről és a hozzá tartozó adatbázisról</span><span class="sxs-lookup"><span data-stu-id="a5d44-103">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="a5d44-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a5d44-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCache -ResourceGroupName <String> [-ClusterName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a5d44-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a5d44-105">DESCRIPTION</span></span>
<span data-ttu-id="a5d44-106">Információt kap egy RedisEnterprise fürtről és a hozzá tartozó adatbázisról</span><span class="sxs-lookup"><span data-stu-id="a5d44-106">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="a5d44-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a5d44-107">EXAMPLES</span></span>

### <span data-ttu-id="a5d44-108">1. példa: A nagyvállalati gyorsítótár név alapján való lekértése</span><span class="sxs-lookup"><span data-stu-id="a5d44-108">Example 1: Get a Redis Enterprise Cache by name</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup" -Name "MyCache"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="a5d44-109">Ez a parancs a MyCache nevű Nagyvállalati gyorsítótárat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a5d44-109">This command gets the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="a5d44-110">2. példa: Erőforráscsoport minden újradiskedő nagyvállalati gyorsítótárának lekérte</span><span class="sxs-lookup"><span data-stu-id="a5d44-110">Example 2: Get every Redis Enterprise Cache in a resource group</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup"

Location Name     Type                            Zone      Database
-------- ----     ----                            ----      --------
East US  MyCache1 Microsoft.Cache/redisEnterprise           {default}
East US  MyCache2 Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="a5d44-111">Ez a parancs a megadott erőforráscsoportban lévő összes redis enterprise cache-t beveszi.</span><span class="sxs-lookup"><span data-stu-id="a5d44-111">This command gets every Redis Enterprise Cache in the specified resource group.</span></span>

## <span data-ttu-id="a5d44-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5d44-112">PARAMETERS</span></span>

### <span data-ttu-id="a5d44-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a5d44-113">-ClusterName</span></span>
<span data-ttu-id="a5d44-114">A RedisEnterprise fürt neve.</span><span class="sxs-lookup"><span data-stu-id="a5d44-114">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d44-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d44-115">-DefaultProfile</span></span>
<span data-ttu-id="a5d44-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5d44-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5d44-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5d44-117">-ResourceGroupName</span></span>
<span data-ttu-id="a5d44-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a5d44-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="a5d44-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5d44-119">-SubscriptionId</span></span>
<span data-ttu-id="a5d44-120">Olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="a5d44-120">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a5d44-121">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="a5d44-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a5d44-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d44-122">CommonParameters</span></span>
<span data-ttu-id="a5d44-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5d44-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d44-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5d44-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d44-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5d44-125">INPUTS</span></span>

## <span data-ttu-id="a5d44-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5d44-126">OUTPUTS</span></span>

### <span data-ttu-id="a5d44-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="a5d44-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="a5d44-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a5d44-128">NOTES</span></span>

<span data-ttu-id="a5d44-129">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a5d44-129">ALIASES</span></span>

## <span data-ttu-id="a5d44-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5d44-130">RELATED LINKS</span></span>

