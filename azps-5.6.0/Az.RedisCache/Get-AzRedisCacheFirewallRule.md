---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 5e17eced3525a7aa318cbba19b632d3ae11d79a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014933"
---
# <span data-ttu-id="5de2a-101">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5de2a-101">Get-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="5de2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5de2a-102">SYNOPSIS</span></span>
<span data-ttu-id="5de2a-103">Tűzfalszabályok beállítása a Redis cache-re.</span><span class="sxs-lookup"><span data-stu-id="5de2a-103">Get firewall rules set on Redis Cache.</span></span>

## <span data-ttu-id="5de2a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5de2a-104">SYNTAX</span></span>

```
Get-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5de2a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5de2a-105">DESCRIPTION</span></span>
<span data-ttu-id="5de2a-106">Ha meg van adva a **RuleName** paraméter, a **Get-AzRedisCacheFirewallRule** parancsmag részletes információkat kap a megadott tűzfalszabályról az Azure Redis cache-ben.</span><span class="sxs-lookup"><span data-stu-id="5de2a-106">If **RuleName** parameter if provided, **Get-AzRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="5de2a-107">Ha csak **a Név** van megadva, ez a művelet minden tűzfalszabályt elérhetővé fog tenni az adott redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="5de2a-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="5de2a-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5de2a-108">EXAMPLES</span></span>

### <span data-ttu-id="5de2a-109">1. példa: Egyetlen tűzfalszabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="5de2a-109">Example 1: Get a single firewall rule</span></span>
```
PS C:\>Get-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="5de2a-110">Ez a parancs egy szabály nevű tűzfalszabályt kap a Mycache nevű redis gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="5de2a-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="5de2a-111">2. példa: Az összes tűzfalszabály lekérte</span><span class="sxs-lookup"><span data-stu-id="5de2a-111">Example 2: Get all firewall rules</span></span>
```
PS C:\>Get-AzRedisCacheFirewallRule -Name "mycache"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruletwo
        RuleName          : ruletwo
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.33
        EndIP             : 10.0.0.64
```

<span data-ttu-id="5de2a-112">Ez a parancs az összes tűzfalszabályt a Mycache nevű redis gyorsítótárból kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5de2a-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="5de2a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5de2a-113">PARAMETERS</span></span>

### <span data-ttu-id="5de2a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5de2a-114">-DefaultProfile</span></span>
<span data-ttu-id="5de2a-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5de2a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5de2a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5de2a-116">-Name</span></span>
<span data-ttu-id="5de2a-117">A redis cache neve.</span><span class="sxs-lookup"><span data-stu-id="5de2a-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="5de2a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5de2a-118">-ResourceGroupName</span></span>
<span data-ttu-id="5de2a-119">Annak az erőforráscsoportnak a neve, amelyben a gyorsítótár létezik.</span><span class="sxs-lookup"><span data-stu-id="5de2a-119">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="5de2a-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="5de2a-120">-RuleName</span></span>
<span data-ttu-id="5de2a-121">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="5de2a-121">Name of firewall rule.</span></span>

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

### <span data-ttu-id="5de2a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5de2a-122">CommonParameters</span></span>
<span data-ttu-id="5de2a-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5de2a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5de2a-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5de2a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5de2a-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5de2a-125">INPUTS</span></span>

### <span data-ttu-id="5de2a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="5de2a-126">System.String</span></span>

## <span data-ttu-id="5de2a-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5de2a-127">OUTPUTS</span></span>

### <span data-ttu-id="5de2a-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5de2a-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="5de2a-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5de2a-129">NOTES</span></span>

## <span data-ttu-id="5de2a-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5de2a-130">RELATED LINKS</span></span>

[<span data-ttu-id="5de2a-131">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5de2a-131">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="5de2a-132">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5de2a-132">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="5de2a-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5de2a-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="5de2a-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5de2a-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="5de2a-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5de2a-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="5de2a-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5de2a-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)