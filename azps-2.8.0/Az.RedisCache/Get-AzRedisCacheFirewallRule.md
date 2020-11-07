---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 1bf6394621435293be1d00d4a9e9f435c160e668
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838521"
---
# <span data-ttu-id="3328d-101">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3328d-101">Get-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="3328d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3328d-102">SYNOPSIS</span></span>
<span data-ttu-id="3328d-103">Tűzfal-szabályok beszerzése a Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="3328d-103">Get firewall rules set on Redis Cache.</span></span>

## <span data-ttu-id="3328d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3328d-104">SYNTAX</span></span>

```
Get-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3328d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3328d-105">DESCRIPTION</span></span>
<span data-ttu-id="3328d-106">Ha a **RuleName** paraméter, ha meg van adva, a **Get-AzRedisCacheFirewallRule** parancsmag részletesen ismerteti az Azure Redis gyorsítótárában lévő megadott tűzfalszabályok adatait.</span><span class="sxs-lookup"><span data-stu-id="3328d-106">If **RuleName** parameter if provided, **Get-AzRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="3328d-107">Ha csak a **név** érték van megadva, ez a művelet a Redis-gyorsítótárban elérhető összes tűzfal-szabályt beilleszti.</span><span class="sxs-lookup"><span data-stu-id="3328d-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="3328d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3328d-108">EXAMPLES</span></span>

### <span data-ttu-id="3328d-109">Példa 1: egyetlen tűzfalszabály beszerzése</span><span class="sxs-lookup"><span data-stu-id="3328d-109">Example 1: Get a single firewall rule</span></span>
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

<span data-ttu-id="3328d-110">Ez a parancs a mycache nevű Redis-gyorsítótárból kapja meg a ruleone nevű tűzfal-szabályt.</span><span class="sxs-lookup"><span data-stu-id="3328d-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="3328d-111">2. példa: a tűzfalszabályok minden szabályának beolvasása</span><span class="sxs-lookup"><span data-stu-id="3328d-111">Example 2: Get all firewall rules</span></span>
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

<span data-ttu-id="3328d-112">Ez a parancs a mycache nevű Redis-gyorsítótárból kapja meg az összes tűzfal-szabályt.</span><span class="sxs-lookup"><span data-stu-id="3328d-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="3328d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3328d-113">PARAMETERS</span></span>

### <span data-ttu-id="3328d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3328d-114">-DefaultProfile</span></span>
<span data-ttu-id="3328d-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3328d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3328d-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3328d-116">-Name</span></span>
<span data-ttu-id="3328d-117">A Redis-gyorsítótár neve</span><span class="sxs-lookup"><span data-stu-id="3328d-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="3328d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3328d-118">-ResourceGroupName</span></span>
<span data-ttu-id="3328d-119">Annak az erőforráscsoportnek a neve, amelyben a gyorsítótár létezik.</span><span class="sxs-lookup"><span data-stu-id="3328d-119">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="3328d-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="3328d-120">-RuleName</span></span>
<span data-ttu-id="3328d-121">Tűzfal-szabály neve.</span><span class="sxs-lookup"><span data-stu-id="3328d-121">Name of firewall rule.</span></span>

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

### <span data-ttu-id="3328d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3328d-122">CommonParameters</span></span>
<span data-ttu-id="3328d-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3328d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3328d-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3328d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3328d-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3328d-125">INPUTS</span></span>

### <span data-ttu-id="3328d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3328d-126">System.String</span></span>

## <span data-ttu-id="3328d-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3328d-127">OUTPUTS</span></span>

### <span data-ttu-id="3328d-128">Microsoft. Azure. Command. RedisCache. models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3328d-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="3328d-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3328d-129">NOTES</span></span>

## <span data-ttu-id="3328d-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3328d-130">RELATED LINKS</span></span>

[<span data-ttu-id="3328d-131">Új – AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3328d-131">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="3328d-132">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3328d-132">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="3328d-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3328d-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="3328d-134">Új – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3328d-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="3328d-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3328d-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="3328d-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3328d-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)