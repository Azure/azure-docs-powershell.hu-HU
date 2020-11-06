---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 231787f57061ff4e118510c3dc166915b39da436
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495292"
---
# <span data-ttu-id="e5285-101">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e5285-101">Get-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="e5285-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5285-102">SYNOPSIS</span></span>
<span data-ttu-id="e5285-103">Tűzfal-szabályok beszerzése a Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="e5285-103">Get firewall rules set on Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5285-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5285-104">SYNTAX</span></span>

```
Get-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5285-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5285-105">DESCRIPTION</span></span>
<span data-ttu-id="e5285-106">Ha a **RuleName** paraméter, ha meg van adva, a **Get-AzureRmRedisCacheFirewallRule** parancsmag részletesen ismerteti az Azure Redis gyorsítótárában lévő megadott tűzfalszabályok adatait.</span><span class="sxs-lookup"><span data-stu-id="e5285-106">If **RuleName** parameter if provided, **Get-AzureRmRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="e5285-107">Ha csak a **név** érték van megadva, ez a művelet a Redis-gyorsítótárban elérhető összes tűzfal-szabályt beilleszti.</span><span class="sxs-lookup"><span data-stu-id="e5285-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="e5285-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e5285-108">EXAMPLES</span></span>

### <span data-ttu-id="e5285-109">Példa 1: egyetlen tűzfalszabály beszerzése</span><span class="sxs-lookup"><span data-stu-id="e5285-109">Example 1: Get a single firewall rule</span></span>
```
PS C:\>Get-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="e5285-110">Ez a parancs a mycache nevű Redis-gyorsítótárból kapja meg a ruleone nevű tűzfal-szabályt.</span><span class="sxs-lookup"><span data-stu-id="e5285-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="e5285-111">2. példa: a tűzfalszabályok minden szabályának beolvasása</span><span class="sxs-lookup"><span data-stu-id="e5285-111">Example 2: Get all firewall rules</span></span>
```
PS C:\>Get-AzureRmRedisCacheFirewallRule -Name "mycache"

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

<span data-ttu-id="e5285-112">Ez a parancs a mycache nevű Redis-gyorsítótárból kapja meg az összes tűzfal-szabályt.</span><span class="sxs-lookup"><span data-stu-id="e5285-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="e5285-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5285-113">PARAMETERS</span></span>

### <span data-ttu-id="e5285-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5285-114">-DefaultProfile</span></span>
<span data-ttu-id="e5285-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5285-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5285-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e5285-116">-Name</span></span>
<span data-ttu-id="e5285-117">A Redis-gyorsítótár neve</span><span class="sxs-lookup"><span data-stu-id="e5285-117">Name of redis cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5285-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5285-118">-ResourceGroupName</span></span>
<span data-ttu-id="e5285-119">Annak az erőforráscsoportnek a neve, amelyben a gyorsítótár létezik.</span><span class="sxs-lookup"><span data-stu-id="e5285-119">Name of resource group in which cache exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5285-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="e5285-120">-RuleName</span></span>
<span data-ttu-id="e5285-121">Tűzfal-szabály neve.</span><span class="sxs-lookup"><span data-stu-id="e5285-121">Name of firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5285-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5285-122">CommonParameters</span></span>
<span data-ttu-id="e5285-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5285-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5285-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5285-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5285-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5285-125">INPUTS</span></span>

### <span data-ttu-id="e5285-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e5285-126">System.String</span></span>
<span data-ttu-id="e5285-127">A parancsmagot név szerint, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="e5285-127">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="e5285-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5285-128">OUTPUTS</span></span>

### <span data-ttu-id="e5285-129">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. RedisCache. models. PSRedisFirewallRule, Microsoft. Azure. commands. RedisCache, Version = 4.0.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e5285-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule, Microsoft.Azure.Commands.RedisCache, Version=4.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e5285-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5285-130">NOTES</span></span>

## <span data-ttu-id="e5285-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5285-131">RELATED LINKS</span></span>

[<span data-ttu-id="e5285-132">Új – AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e5285-132">New-AzureRmRedisCacheFirewallRule</span></span>](./New-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="e5285-133">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e5285-133">Remove-AzureRmRedisCacheFirewallRule</span></span>](./Remove-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="e5285-134">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e5285-134">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="e5285-135">Új – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e5285-135">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="e5285-136">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e5285-136">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="e5285-137">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e5285-137">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
