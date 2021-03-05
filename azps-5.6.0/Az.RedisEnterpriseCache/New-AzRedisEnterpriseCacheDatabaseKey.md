---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/new-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: 3d28515ede93abf2ebb5be8bad2e961f2e22b572
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000757"
---
# <span data-ttu-id="4acc5-101">New-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="4acc5-101">New-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="4acc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4acc5-102">SYNOPSIS</span></span>
<span data-ttu-id="4acc5-103">Újragenerálja a RedisEnterprise adatbázis hozzáférési kulcsait.</span><span class="sxs-lookup"><span data-stu-id="4acc5-103">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="4acc5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4acc5-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 -KeyType <AccessKeyType> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4acc5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4acc5-105">DESCRIPTION</span></span>
<span data-ttu-id="4acc5-106">Újragenerálja a RedisEnterprise adatbázis hozzáférési kulcsait.</span><span class="sxs-lookup"><span data-stu-id="4acc5-106">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="4acc5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4acc5-107">EXAMPLES</span></span>

### <span data-ttu-id="4acc5-108">1. példa: Az elsődleges hozzáférési kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="4acc5-108">Example 1: Regenerate primary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Primary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
new-primary-key                              secondary-key

```

<span data-ttu-id="4acc5-109">Ez a parancs a MyCache nevű Redis Enterprise Cache adatbázisával létesített kapcsolatok hitelesítésére használt elsődleges titkos hozzáférési kulcsot újra létrehozza.</span><span class="sxs-lookup"><span data-stu-id="4acc5-109">This command regenerates the primary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="4acc5-110">2. példa: Másodlagos hozzáférési kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="4acc5-110">Example 2: Regenerate secondary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Secondary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  new-secondary-key

```

<span data-ttu-id="4acc5-111">Ez a parancs újra létrehozza a MyCache nevű Redis Enterprise Cache adatbázisával létesített kapcsolatok hitelesítésére használt másodlagos titkos hozzáférési kulcsot.</span><span class="sxs-lookup"><span data-stu-id="4acc5-111">This command regenerates the secondary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="4acc5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4acc5-112">PARAMETERS</span></span>

### <span data-ttu-id="4acc5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4acc5-113">-AsJob</span></span>
<span data-ttu-id="4acc5-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="4acc5-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4acc5-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4acc5-115">-ClusterName</span></span>
<span data-ttu-id="4acc5-116">A RedisEnterprise fürt neve.</span><span class="sxs-lookup"><span data-stu-id="4acc5-116">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="4acc5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4acc5-117">-DefaultProfile</span></span>
<span data-ttu-id="4acc5-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4acc5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4acc5-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="4acc5-119">-KeyType</span></span>
<span data-ttu-id="4acc5-120">Melyik hozzáférési kulcs az újrageneráláshoz?</span><span class="sxs-lookup"><span data-stu-id="4acc5-120">Which access key to regenerate.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.AccessKeyType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4acc5-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4acc5-121">-NoWait</span></span>
<span data-ttu-id="4acc5-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="4acc5-122">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4acc5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4acc5-123">-ResourceGroupName</span></span>
<span data-ttu-id="4acc5-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4acc5-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="4acc5-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4acc5-125">-SubscriptionId</span></span>
<span data-ttu-id="4acc5-126">Olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="4acc5-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4acc5-127">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="4acc5-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4acc5-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4acc5-128">-Confirm</span></span>
<span data-ttu-id="4acc5-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4acc5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4acc5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4acc5-130">-WhatIf</span></span>
<span data-ttu-id="4acc5-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4acc5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4acc5-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4acc5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4acc5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4acc5-133">CommonParameters</span></span>
<span data-ttu-id="4acc5-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4acc5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4acc5-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4acc5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4acc5-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4acc5-136">INPUTS</span></span>

## <span data-ttu-id="4acc5-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4acc5-137">OUTPUTS</span></span>

### <span data-ttu-id="4acc5-138">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="4acc5-138">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="4acc5-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4acc5-139">NOTES</span></span>

<span data-ttu-id="4acc5-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="4acc5-140">ALIASES</span></span>

## <span data-ttu-id="4acc5-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4acc5-141">RELATED LINKS</span></span>

