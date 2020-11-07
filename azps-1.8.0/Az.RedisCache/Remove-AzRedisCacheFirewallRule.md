---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
ms.openlocfilehash: e24ea6e0b5bf88b17a6209f2ea69634200a10a62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669531"
---
# <span data-ttu-id="d8942-101">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d8942-101">Remove-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="d8942-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d8942-102">SYNOPSIS</span></span>
<span data-ttu-id="d8942-103">Tűzfalszabály eltávolítása Redis-gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="d8942-103">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="d8942-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d8942-104">SYNTAX</span></span>

### <span data-ttu-id="d8942-105">NormalParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d8942-105">NormalParameterSet (Default)</span></span>
```
Remove-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8942-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="d8942-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8942-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d8942-107">DESCRIPTION</span></span>
<span data-ttu-id="d8942-108">Tűzfalszabály eltávolítása Redis-gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="d8942-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="d8942-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d8942-109">EXAMPLES</span></span>

### <span data-ttu-id="d8942-110">1. példa: egyetlen tűzfalszabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d8942-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="d8942-111">Ez a parancs eltávolítja a ruleone nevű tűzfal-szabályt a mycache nevű Redis-gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="d8942-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="d8942-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d8942-112">PARAMETERS</span></span>

### <span data-ttu-id="d8942-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8942-113">-DefaultProfile</span></span>
<span data-ttu-id="d8942-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d8942-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8942-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8942-115">-InputObject</span></span>
<span data-ttu-id="d8942-116">PSRedisFirewallRule típusú objektum</span><span class="sxs-lookup"><span data-stu-id="d8942-116">object of type PSRedisFirewallRule</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule
Parameter Sets: PSRedisFirewallRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8942-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d8942-117">-Name</span></span>
<span data-ttu-id="d8942-118">A Redis-gyorsítótár neve</span><span class="sxs-lookup"><span data-stu-id="d8942-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="d8942-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8942-119">-PassThru</span></span>
<span data-ttu-id="d8942-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d8942-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d8942-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8942-121">-ResourceGroupName</span></span>
<span data-ttu-id="d8942-122">Annak az erőforráscsoportnek a neve, amelyben a gyorsítótár létezik.</span><span class="sxs-lookup"><span data-stu-id="d8942-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="d8942-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="d8942-123">-RuleName</span></span>
<span data-ttu-id="d8942-124">Tűzfal-szabály neve.</span><span class="sxs-lookup"><span data-stu-id="d8942-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="d8942-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d8942-125">-Confirm</span></span>
<span data-ttu-id="d8942-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d8942-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8942-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8942-127">-WhatIf</span></span>
<span data-ttu-id="d8942-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d8942-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8942-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d8942-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8942-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8942-130">CommonParameters</span></span>
<span data-ttu-id="d8942-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d8942-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8942-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8942-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8942-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8942-133">INPUTS</span></span>

### <span data-ttu-id="d8942-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d8942-134">System.String</span></span>

### <span data-ttu-id="d8942-135">Microsoft. Azure. Command. RedisCache. models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d8942-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="d8942-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8942-136">OUTPUTS</span></span>

### <span data-ttu-id="d8942-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d8942-137">System.Boolean</span></span>

## <span data-ttu-id="d8942-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d8942-138">NOTES</span></span>

## <span data-ttu-id="d8942-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8942-139">RELATED LINKS</span></span>

[<span data-ttu-id="d8942-140">Új – AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d8942-140">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="d8942-141">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d8942-141">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="d8942-142">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d8942-142">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="d8942-143">Új – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d8942-143">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="d8942-144">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d8942-144">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="d8942-145">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d8942-145">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)