---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: e602cb4fc86ede6a4e1f7cc894c1825fd1d560fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151010"
---
# <span data-ttu-id="9ef1f-101">Get-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="9ef1f-101">Get-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="9ef1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ef1f-102">SYNOPSIS</span></span>
<span data-ttu-id="9ef1f-103">Beolvassa a RedisEnterprise adatbázis hozzáférési kulcsait.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-103">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="9ef1f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9ef1f-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9ef1f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9ef1f-105">DESCRIPTION</span></span>
<span data-ttu-id="9ef1f-106">Beolvassa a RedisEnterprise adatbázis hozzáférési kulcsait.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-106">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="9ef1f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9ef1f-107">EXAMPLES</span></span>

### <span data-ttu-id="9ef1f-108">1. példa: Adatbázis-hozzáférési kulcsok lekérte</span><span class="sxs-lookup"><span data-stu-id="9ef1f-108">Example 1: Get database access keys</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  secondary-key

```

<span data-ttu-id="9ef1f-109">Ez a parancs a MyCache nevű Redis Enterprise Cache adatbázisával létesített kapcsolatok hitelesítésére használt titkos hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-109">This command gets the secret access keys used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="9ef1f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ef1f-110">PARAMETERS</span></span>

### <span data-ttu-id="9ef1f-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9ef1f-111">-ClusterName</span></span>
<span data-ttu-id="9ef1f-112">A RedisEnterprise fürt neve.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-112">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="9ef1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ef1f-113">-DefaultProfile</span></span>
<span data-ttu-id="9ef1f-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ef1f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ef1f-115">-ResourceGroupName</span></span>
<span data-ttu-id="9ef1f-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="9ef1f-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9ef1f-117">-SubscriptionId</span></span>
<span data-ttu-id="9ef1f-118">Olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9ef1f-119">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9ef1f-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ef1f-120">-Confirm</span></span>
<span data-ttu-id="9ef1f-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ef1f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ef1f-122">-WhatIf</span></span>
<span data-ttu-id="9ef1f-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ef1f-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ef1f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ef1f-125">CommonParameters</span></span>
<span data-ttu-id="9ef1f-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ef1f-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ef1f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ef1f-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ef1f-128">INPUTS</span></span>

## <span data-ttu-id="9ef1f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ef1f-129">OUTPUTS</span></span>

### <span data-ttu-id="9ef1f-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="9ef1f-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="9ef1f-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9ef1f-131">NOTES</span></span>

<span data-ttu-id="9ef1f-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9ef1f-132">ALIASES</span></span>

## <span data-ttu-id="9ef1f-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ef1f-133">RELATED LINKS</span></span>

