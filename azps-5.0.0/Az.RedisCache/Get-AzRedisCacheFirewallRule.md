---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 8e28951f826c5a049f345bb3182bda10e7de82fb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194868"
---
# <span data-ttu-id="04e8b-101">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="04e8b-101">Get-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="04e8b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="04e8b-102">SYNOPSIS</span></span>
<span data-ttu-id="04e8b-103">Tűzfal-szabályok beszerzése a Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="04e8b-103">Get firewall rules set on Redis Cache.</span></span>

## <span data-ttu-id="04e8b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="04e8b-104">SYNTAX</span></span>

```
Get-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04e8b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="04e8b-105">DESCRIPTION</span></span>
<span data-ttu-id="04e8b-106">Ha a **RuleName** paraméter, ha meg van adva, a **Get-AzRedisCacheFirewallRule** parancsmag részletesen ismerteti az Azure Redis gyorsítótárában lévő megadott tűzfalszabályok adatait.</span><span class="sxs-lookup"><span data-stu-id="04e8b-106">If **RuleName** parameter if provided, **Get-AzRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="04e8b-107">Ha csak a **név** érték van megadva, ez a művelet a Redis-gyorsítótárban elérhető összes tűzfal-szabályt beilleszti.</span><span class="sxs-lookup"><span data-stu-id="04e8b-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="04e8b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="04e8b-108">EXAMPLES</span></span>

### <span data-ttu-id="04e8b-109">Példa 1: egyetlen tűzfalszabály beszerzése</span><span class="sxs-lookup"><span data-stu-id="04e8b-109">Example 1: Get a single firewall rule</span></span>
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

<span data-ttu-id="04e8b-110">Ez a parancs a mycache nevű Redis-gyorsítótárból kapja meg a ruleone nevű tűzfal-szabályt.</span><span class="sxs-lookup"><span data-stu-id="04e8b-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="04e8b-111">2. példa: a tűzfalszabályok minden szabályának beolvasása</span><span class="sxs-lookup"><span data-stu-id="04e8b-111">Example 2: Get all firewall rules</span></span>
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

<span data-ttu-id="04e8b-112">Ez a parancs a mycache nevű Redis-gyorsítótárból kapja meg az összes tűzfal-szabályt.</span><span class="sxs-lookup"><span data-stu-id="04e8b-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="04e8b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="04e8b-113">PARAMETERS</span></span>

### <span data-ttu-id="04e8b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04e8b-114">-DefaultProfile</span></span>
<span data-ttu-id="04e8b-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04e8b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04e8b-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="04e8b-116">-Name</span></span>
<span data-ttu-id="04e8b-117">A Redis-gyorsítótár neve</span><span class="sxs-lookup"><span data-stu-id="04e8b-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="04e8b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04e8b-118">-ResourceGroupName</span></span>
<span data-ttu-id="04e8b-119">Annak az erőforráscsoportnek a neve, amelyben a gyorsítótár létezik.</span><span class="sxs-lookup"><span data-stu-id="04e8b-119">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="04e8b-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="04e8b-120">-RuleName</span></span>
<span data-ttu-id="04e8b-121">Tűzfal-szabály neve.</span><span class="sxs-lookup"><span data-stu-id="04e8b-121">Name of firewall rule.</span></span>

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

### <span data-ttu-id="04e8b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04e8b-122">CommonParameters</span></span>
<span data-ttu-id="04e8b-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="04e8b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04e8b-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04e8b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04e8b-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="04e8b-125">INPUTS</span></span>

### <span data-ttu-id="04e8b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="04e8b-126">System.String</span></span>

## <span data-ttu-id="04e8b-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04e8b-127">OUTPUTS</span></span>

### <span data-ttu-id="04e8b-128">Microsoft. Azure. Command. RedisCache. models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="04e8b-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="04e8b-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="04e8b-129">NOTES</span></span>

## <span data-ttu-id="04e8b-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04e8b-130">RELATED LINKS</span></span>

[<span data-ttu-id="04e8b-131">Új – AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="04e8b-131">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="04e8b-132">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="04e8b-132">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="04e8b-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="04e8b-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="04e8b-134">Új – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="04e8b-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="04e8b-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="04e8b-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="04e8b-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="04e8b-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)