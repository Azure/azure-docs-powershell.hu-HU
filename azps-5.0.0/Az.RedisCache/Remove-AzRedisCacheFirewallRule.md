---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
ms.openlocfilehash: c19be1f524519a55a5a95a575e97cfd250952570
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187550"
---
# <span data-ttu-id="4fc03-101">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4fc03-101">Remove-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="4fc03-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4fc03-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc03-103">Tűzfalszabály eltávolítása Redis-gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="4fc03-103">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="4fc03-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4fc03-104">SYNTAX</span></span>

### <span data-ttu-id="4fc03-105">NormalParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4fc03-105">NormalParameterSet (Default)</span></span>
```
Remove-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fc03-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="4fc03-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fc03-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4fc03-107">DESCRIPTION</span></span>
<span data-ttu-id="4fc03-108">Tűzfalszabály eltávolítása Redis-gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="4fc03-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="4fc03-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4fc03-109">EXAMPLES</span></span>

### <span data-ttu-id="4fc03-110">1. példa: egyetlen tűzfalszabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4fc03-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="4fc03-111">Ez a parancs eltávolítja a ruleone nevű tűzfal-szabályt a mycache nevű Redis-gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="4fc03-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="4fc03-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4fc03-112">PARAMETERS</span></span>

### <span data-ttu-id="4fc03-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fc03-113">-DefaultProfile</span></span>
<span data-ttu-id="4fc03-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4fc03-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fc03-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fc03-115">-InputObject</span></span>
<span data-ttu-id="4fc03-116">PSRedisFirewallRule típusú objektum</span><span class="sxs-lookup"><span data-stu-id="4fc03-116">object of type PSRedisFirewallRule</span></span>

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

### <span data-ttu-id="4fc03-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4fc03-117">-Name</span></span>
<span data-ttu-id="4fc03-118">A Redis-gyorsítótár neve</span><span class="sxs-lookup"><span data-stu-id="4fc03-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="4fc03-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fc03-119">-PassThru</span></span>
<span data-ttu-id="4fc03-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4fc03-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4fc03-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fc03-121">-ResourceGroupName</span></span>
<span data-ttu-id="4fc03-122">Annak az erőforráscsoportnek a neve, amelyben a gyorsítótár létezik.</span><span class="sxs-lookup"><span data-stu-id="4fc03-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="4fc03-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="4fc03-123">-RuleName</span></span>
<span data-ttu-id="4fc03-124">Tűzfal-szabály neve.</span><span class="sxs-lookup"><span data-stu-id="4fc03-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="4fc03-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4fc03-125">-Confirm</span></span>
<span data-ttu-id="4fc03-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4fc03-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fc03-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fc03-127">-WhatIf</span></span>
<span data-ttu-id="4fc03-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4fc03-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fc03-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4fc03-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fc03-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc03-130">CommonParameters</span></span>
<span data-ttu-id="4fc03-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4fc03-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc03-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fc03-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc03-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fc03-133">INPUTS</span></span>

### <span data-ttu-id="4fc03-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4fc03-134">System.String</span></span>

### <span data-ttu-id="4fc03-135">Microsoft. Azure. Command. RedisCache. models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4fc03-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="4fc03-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fc03-136">OUTPUTS</span></span>

### <span data-ttu-id="4fc03-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4fc03-137">System.Boolean</span></span>

## <span data-ttu-id="4fc03-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4fc03-138">NOTES</span></span>

## <span data-ttu-id="4fc03-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fc03-139">RELATED LINKS</span></span>

[<span data-ttu-id="4fc03-140">Új – AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4fc03-140">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="4fc03-141">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4fc03-141">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="4fc03-142">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4fc03-142">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="4fc03-143">Új – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4fc03-143">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="4fc03-144">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4fc03-144">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="4fc03-145">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4fc03-145">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)