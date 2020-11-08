---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 50a2df73d6cfa1e9d34f2c5c4b426f601c9d9309
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184009"
---
# <span data-ttu-id="691da-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="691da-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="691da-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="691da-102">SYNOPSIS</span></span>
<span data-ttu-id="691da-103">Tűzfal-szabály létrehozása Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="691da-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="691da-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="691da-104">SYNTAX</span></span>

### <span data-ttu-id="691da-105">NormalParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="691da-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="691da-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="691da-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="691da-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="691da-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="691da-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="691da-108">DESCRIPTION</span></span>
<span data-ttu-id="691da-109">Tűzfal-szabály létrehozása Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="691da-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="691da-110">Példák</span><span class="sxs-lookup"><span data-stu-id="691da-110">EXAMPLES</span></span>

### <span data-ttu-id="691da-111">Példa 1: tűzfalszabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="691da-111">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -StartIP "10.0.0.1" -EndIP "10.0.0.32"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="691da-112">A parancs létrehozza a ruleone nevű Redis-gyorsítótárban a mycache nevű tűzfal-szabályt.</span><span class="sxs-lookup"><span data-stu-id="691da-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="691da-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="691da-113">PARAMETERS</span></span>

### <span data-ttu-id="691da-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="691da-114">-DefaultProfile</span></span>
<span data-ttu-id="691da-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="691da-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="691da-116">-ZáróIP</span><span class="sxs-lookup"><span data-stu-id="691da-116">-EndIP</span></span>
<span data-ttu-id="691da-117">Záró IP-cím.</span><span class="sxs-lookup"><span data-stu-id="691da-117">Ending IP address.</span></span>

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

### <span data-ttu-id="691da-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="691da-118">-InputObject</span></span>
<span data-ttu-id="691da-119">RedisCacheAttributes típusú objektum</span><span class="sxs-lookup"><span data-stu-id="691da-119">object of type RedisCacheAttributes</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes
Parameter Sets: RedisCacheAttributesObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="691da-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="691da-120">-Name</span></span>
<span data-ttu-id="691da-121">A Redis-gyorsítótár neve</span><span class="sxs-lookup"><span data-stu-id="691da-121">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="691da-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="691da-122">-ResourceGroupName</span></span>
<span data-ttu-id="691da-123">Annak az erőforráscsoportnek a neve, amelyben a gyorsítótár létezik.</span><span class="sxs-lookup"><span data-stu-id="691da-123">Name of resource group in which cache exists.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="691da-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="691da-124">-ResourceId</span></span>
<span data-ttu-id="691da-125">A Redis-gyorsítótár ARM azonosítója</span><span class="sxs-lookup"><span data-stu-id="691da-125">ARM Id of Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="691da-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="691da-126">-RuleName</span></span>
<span data-ttu-id="691da-127">Tűzfal-szabály neve.</span><span class="sxs-lookup"><span data-stu-id="691da-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="691da-128">-KezdőIP</span><span class="sxs-lookup"><span data-stu-id="691da-128">-StartIP</span></span>
<span data-ttu-id="691da-129">Kezdő IP-cím.</span><span class="sxs-lookup"><span data-stu-id="691da-129">Starting IP address.</span></span>

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

### <span data-ttu-id="691da-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="691da-130">-Confirm</span></span>
<span data-ttu-id="691da-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="691da-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="691da-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="691da-132">-WhatIf</span></span>
<span data-ttu-id="691da-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="691da-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="691da-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="691da-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="691da-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="691da-135">CommonParameters</span></span>
<span data-ttu-id="691da-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="691da-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="691da-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="691da-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="691da-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="691da-138">INPUTS</span></span>

### <span data-ttu-id="691da-139">System. String</span><span class="sxs-lookup"><span data-stu-id="691da-139">System.String</span></span>

### <span data-ttu-id="691da-140">Microsoft. Azure. Command. RedisCache. models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="691da-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="691da-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="691da-141">OUTPUTS</span></span>

### <span data-ttu-id="691da-142">Microsoft. Azure. Command. RedisCache. models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="691da-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="691da-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="691da-143">NOTES</span></span>

## <span data-ttu-id="691da-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="691da-144">RELATED LINKS</span></span>

[<span data-ttu-id="691da-145">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="691da-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="691da-146">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="691da-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="691da-147">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="691da-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="691da-148">Új – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="691da-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="691da-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="691da-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="691da-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="691da-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)