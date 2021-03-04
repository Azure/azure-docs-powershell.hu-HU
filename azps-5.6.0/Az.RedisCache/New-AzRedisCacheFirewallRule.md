---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: bd0d6995cae0d32a7fb0ce46d42f87a480c275f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920953"
---
# <span data-ttu-id="6d8f8-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6d8f8-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="6d8f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d8f8-102">SYNOPSIS</span></span>
<span data-ttu-id="6d8f8-103">Hozzon létre tűzfalszabályt a redis cache-re.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="6d8f8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6d8f8-104">SYNTAX</span></span>

### <span data-ttu-id="6d8f8-105">NormalParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6d8f8-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d8f8-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="6d8f8-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d8f8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d8f8-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d8f8-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6d8f8-108">DESCRIPTION</span></span>
<span data-ttu-id="6d8f8-109">Hozzon létre tűzfalszabályt a redis cache-re.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="6d8f8-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6d8f8-110">EXAMPLES</span></span>

### <span data-ttu-id="6d8f8-111">1. példa: Tűzfalszabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="6d8f8-111">Example 1: Create a firewall rule</span></span>
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

<span data-ttu-id="6d8f8-112">Ez a parancs létrehoz egy ruleone nevű tűzfalszabályt a mycache nevű Redis gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="6d8f8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d8f8-113">PARAMETERS</span></span>

### <span data-ttu-id="6d8f8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d8f8-114">-DefaultProfile</span></span>
<span data-ttu-id="6d8f8-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d8f8-116">-EndIP</span><span class="sxs-lookup"><span data-stu-id="6d8f8-116">-EndIP</span></span>
<span data-ttu-id="6d8f8-117">Ip-cím befejezése</span><span class="sxs-lookup"><span data-stu-id="6d8f8-117">Ending IP address.</span></span>

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

### <span data-ttu-id="6d8f8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d8f8-118">-InputObject</span></span>
<span data-ttu-id="6d8f8-119">RedisCacheAttributes típusú objektum</span><span class="sxs-lookup"><span data-stu-id="6d8f8-119">object of type RedisCacheAttributes</span></span>

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

### <span data-ttu-id="6d8f8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6d8f8-120">-Name</span></span>
<span data-ttu-id="6d8f8-121">A redis cache neve.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="6d8f8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d8f8-122">-ResourceGroupName</span></span>
<span data-ttu-id="6d8f8-123">Annak az erőforráscsoportnak a neve, amelyben a gyorsítótár létezik.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="6d8f8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d8f8-124">-ResourceId</span></span>
<span data-ttu-id="6d8f8-125">ARM a Redis cache azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-125">ARM Id of Redis Cache.</span></span>

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

### <span data-ttu-id="6d8f8-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="6d8f8-126">-RuleName</span></span>
<span data-ttu-id="6d8f8-127">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="6d8f8-128">-StartIP</span><span class="sxs-lookup"><span data-stu-id="6d8f8-128">-StartIP</span></span>
<span data-ttu-id="6d8f8-129">Kezdő IP-cím.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-129">Starting IP address.</span></span>

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

### <span data-ttu-id="6d8f8-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d8f8-130">-Confirm</span></span>
<span data-ttu-id="6d8f8-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d8f8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d8f8-132">-WhatIf</span></span>
<span data-ttu-id="6d8f8-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d8f8-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d8f8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d8f8-135">CommonParameters</span></span>
<span data-ttu-id="6d8f8-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d8f8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d8f8-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d8f8-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d8f8-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d8f8-138">INPUTS</span></span>

### <span data-ttu-id="6d8f8-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6d8f8-139">System.String</span></span>

### <span data-ttu-id="6d8f8-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="6d8f8-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="6d8f8-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d8f8-141">OUTPUTS</span></span>

### <span data-ttu-id="6d8f8-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6d8f8-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="6d8f8-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6d8f8-143">NOTES</span></span>

## <span data-ttu-id="6d8f8-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d8f8-144">RELATED LINKS</span></span>

[<span data-ttu-id="6d8f8-145">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6d8f8-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="6d8f8-146">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6d8f8-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="6d8f8-147">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6d8f8-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="6d8f8-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6d8f8-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="6d8f8-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6d8f8-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="6d8f8-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6d8f8-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)