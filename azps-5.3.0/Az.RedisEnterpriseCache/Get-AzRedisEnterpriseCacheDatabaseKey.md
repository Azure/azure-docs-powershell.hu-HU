---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: e602cb4fc86ede6a4e1f7cc894c1825fd1d560fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466595"
---
# <span data-ttu-id="3fca1-101">Get-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="3fca1-101">Get-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="3fca1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fca1-102">SYNOPSIS</span></span>
<span data-ttu-id="3fca1-103">Beolvassa a RedisEnterprise adatbázis hozzáférési kulcsait.</span><span class="sxs-lookup"><span data-stu-id="3fca1-103">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="3fca1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3fca1-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3fca1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3fca1-105">DESCRIPTION</span></span>
<span data-ttu-id="3fca1-106">Beolvassa a RedisEnterprise adatbázis hozzáférési kulcsait.</span><span class="sxs-lookup"><span data-stu-id="3fca1-106">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="3fca1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3fca1-107">EXAMPLES</span></span>

### <span data-ttu-id="3fca1-108">1. példa: Adatbázis-hozzáférési kulcsok lekérte</span><span class="sxs-lookup"><span data-stu-id="3fca1-108">Example 1: Get database access keys</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  secondary-key

```

<span data-ttu-id="3fca1-109">Ez a parancs a MyCache nevű Redis Enterprise Cache adatbázisával létesített kapcsolatok hitelesítésére használt titkos hozzáférési kulcsokat kapja.</span><span class="sxs-lookup"><span data-stu-id="3fca1-109">This command gets the secret access keys used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="3fca1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fca1-110">PARAMETERS</span></span>

### <span data-ttu-id="3fca1-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3fca1-111">-ClusterName</span></span>
<span data-ttu-id="3fca1-112">A RedisEnterprise fürt neve.</span><span class="sxs-lookup"><span data-stu-id="3fca1-112">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="3fca1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fca1-113">-DefaultProfile</span></span>
<span data-ttu-id="3fca1-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3fca1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fca1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fca1-115">-ResourceGroupName</span></span>
<span data-ttu-id="3fca1-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3fca1-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="3fca1-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3fca1-117">-SubscriptionId</span></span>
<span data-ttu-id="3fca1-118">Olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="3fca1-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3fca1-119">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="3fca1-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3fca1-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3fca1-120">-Confirm</span></span>
<span data-ttu-id="3fca1-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3fca1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fca1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fca1-122">-WhatIf</span></span>
<span data-ttu-id="3fca1-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3fca1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fca1-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3fca1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fca1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fca1-125">CommonParameters</span></span>
<span data-ttu-id="3fca1-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fca1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fca1-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3fca1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fca1-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3fca1-128">INPUTS</span></span>

## <span data-ttu-id="3fca1-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3fca1-129">OUTPUTS</span></span>

### <span data-ttu-id="3fca1-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="3fca1-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="3fca1-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3fca1-131">NOTES</span></span>

<span data-ttu-id="3fca1-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3fca1-132">ALIASES</span></span>

## <span data-ttu-id="3fca1-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3fca1-133">RELATED LINKS</span></span>

