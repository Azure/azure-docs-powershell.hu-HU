---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
ms.openlocfilehash: c19be1f524519a55a5a95a575e97cfd250952570
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169211"
---
# <span data-ttu-id="9b6fc-101">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9b6fc-101">Remove-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="9b6fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b6fc-102">SYNOPSIS</span></span>
<span data-ttu-id="9b6fc-103">Tűzfalszabály eltávolítása a redis-gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="9b6fc-103">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="9b6fc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9b6fc-104">SYNTAX</span></span>

### <span data-ttu-id="9b6fc-105">NormalParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9b6fc-105">NormalParameterSet (Default)</span></span>
```
Remove-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b6fc-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="9b6fc-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b6fc-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9b6fc-107">DESCRIPTION</span></span>
<span data-ttu-id="9b6fc-108">Tűzfalszabály eltávolítása a redis-gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="9b6fc-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="9b6fc-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9b6fc-109">EXAMPLES</span></span>

### <span data-ttu-id="9b6fc-110">1. példa: Egyetlen tűzfalszabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9b6fc-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="9b6fc-111">Ez a parancs eltávolítja a ruleone nevű tűzfalszabályt a mycache nevű redis gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="9b6fc-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="9b6fc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b6fc-112">PARAMETERS</span></span>

### <span data-ttu-id="9b6fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b6fc-113">-DefaultProfile</span></span>
<span data-ttu-id="9b6fc-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b6fc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b6fc-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b6fc-115">-InputObject</span></span>
<span data-ttu-id="9b6fc-116">PSRedisFirewallRule típusú objektum</span><span class="sxs-lookup"><span data-stu-id="9b6fc-116">object of type PSRedisFirewallRule</span></span>

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

### <span data-ttu-id="9b6fc-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9b6fc-117">-Name</span></span>
<span data-ttu-id="9b6fc-118">A redis cache neve.</span><span class="sxs-lookup"><span data-stu-id="9b6fc-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="9b6fc-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b6fc-119">-PassThru</span></span>
<span data-ttu-id="9b6fc-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9b6fc-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9b6fc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b6fc-121">-ResourceGroupName</span></span>
<span data-ttu-id="9b6fc-122">Annak az erőforráscsoportnak a neve, amelyben a gyorsítótár létezik.</span><span class="sxs-lookup"><span data-stu-id="9b6fc-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="9b6fc-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="9b6fc-123">-RuleName</span></span>
<span data-ttu-id="9b6fc-124">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="9b6fc-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="9b6fc-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b6fc-125">-Confirm</span></span>
<span data-ttu-id="9b6fc-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9b6fc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b6fc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b6fc-127">-WhatIf</span></span>
<span data-ttu-id="9b6fc-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9b6fc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b6fc-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9b6fc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b6fc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b6fc-130">CommonParameters</span></span>
<span data-ttu-id="9b6fc-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b6fc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b6fc-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b6fc-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b6fc-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b6fc-133">INPUTS</span></span>

### <span data-ttu-id="9b6fc-134">System.String</span><span class="sxs-lookup"><span data-stu-id="9b6fc-134">System.String</span></span>

### <span data-ttu-id="9b6fc-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9b6fc-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="9b6fc-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b6fc-136">OUTPUTS</span></span>

### <span data-ttu-id="9b6fc-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9b6fc-137">System.Boolean</span></span>

## <span data-ttu-id="9b6fc-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9b6fc-138">NOTES</span></span>

## <span data-ttu-id="9b6fc-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b6fc-139">RELATED LINKS</span></span>

[<span data-ttu-id="9b6fc-140">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9b6fc-140">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="9b6fc-141">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9b6fc-141">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="9b6fc-142">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9b6fc-142">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="9b6fc-143">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9b6fc-143">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="9b6fc-144">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9b6fc-144">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="9b6fc-145">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9b6fc-145">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)