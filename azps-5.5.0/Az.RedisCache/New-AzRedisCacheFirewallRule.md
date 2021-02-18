---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 50a2df73d6cfa1e9d34f2c5c4b426f601c9d9309
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206166"
---
# <span data-ttu-id="ad5e6-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ad5e6-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="ad5e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad5e6-102">SYNOPSIS</span></span>
<span data-ttu-id="ad5e6-103">Hozzon létre tűzfalszabályt a redis cache-re.</span><span class="sxs-lookup"><span data-stu-id="ad5e6-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="ad5e6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ad5e6-104">SYNTAX</span></span>

### <span data-ttu-id="ad5e6-105">NormalParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ad5e6-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad5e6-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="ad5e6-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad5e6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad5e6-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad5e6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ad5e6-108">DESCRIPTION</span></span>
<span data-ttu-id="ad5e6-109">Hozzon létre tűzfalszabályt a redis-gyorsítótáron.</span><span class="sxs-lookup"><span data-stu-id="ad5e6-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="ad5e6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ad5e6-110">EXAMPLES</span></span>

### <span data-ttu-id="ad5e6-111">1. példa: Tűzfalszabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="ad5e6-111">Example 1: Create a firewall rule</span></span>
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

<span data-ttu-id="ad5e6-112">Ez a parancs létrehoz egy szabály nevű tűzfalszabályt a mycache nevű redis gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="ad5e6-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="ad5e6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad5e6-113">PARAMETERS</span></span>

### <span data-ttu-id="ad5e6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad5e6-114">-DefaultProfile</span></span>
<span data-ttu-id="ad5e6-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad5e6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad5e6-116">-EndIP</span><span class="sxs-lookup"><span data-stu-id="ad5e6-116">-EndIP</span></span>
<span data-ttu-id="ad5e6-117">Ip-cím befejezése</span><span class="sxs-lookup"><span data-stu-id="ad5e6-117">Ending IP address.</span></span>

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

### <span data-ttu-id="ad5e6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad5e6-118">-InputObject</span></span>
<span data-ttu-id="ad5e6-119">RedisCacheAttributes típusú objektum</span><span class="sxs-lookup"><span data-stu-id="ad5e6-119">object of type RedisCacheAttributes</span></span>

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

### <span data-ttu-id="ad5e6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ad5e6-120">-Name</span></span>
<span data-ttu-id="ad5e6-121">A redis cache neve.</span><span class="sxs-lookup"><span data-stu-id="ad5e6-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="ad5e6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad5e6-122">-ResourceGroupName</span></span>
<span data-ttu-id="ad5e6-123">Annak az erőforráscsoportnak a neve, amelyben a gyorsítótár létezik.</span><span class="sxs-lookup"><span data-stu-id="ad5e6-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="ad5e6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad5e6-124">-ResourceId</span></span>
<span data-ttu-id="ad5e6-125">ARM a Redis cache azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ad5e6-125">ARM Id of Redis Cache.</span></span>

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

### <span data-ttu-id="ad5e6-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="ad5e6-126">-RuleName</span></span>
<span data-ttu-id="ad5e6-127">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="ad5e6-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="ad5e6-128">-StartIP</span><span class="sxs-lookup"><span data-stu-id="ad5e6-128">-StartIP</span></span>
<span data-ttu-id="ad5e6-129">Kezdő IP-cím.</span><span class="sxs-lookup"><span data-stu-id="ad5e6-129">Starting IP address.</span></span>

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

### <span data-ttu-id="ad5e6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad5e6-130">-Confirm</span></span>
<span data-ttu-id="ad5e6-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ad5e6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad5e6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad5e6-132">-WhatIf</span></span>
<span data-ttu-id="ad5e6-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ad5e6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad5e6-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad5e6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad5e6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad5e6-135">CommonParameters</span></span>
<span data-ttu-id="ad5e6-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad5e6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad5e6-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad5e6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad5e6-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad5e6-138">INPUTS</span></span>

### <span data-ttu-id="ad5e6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ad5e6-139">System.String</span></span>

### <span data-ttu-id="ad5e6-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="ad5e6-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="ad5e6-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad5e6-141">OUTPUTS</span></span>

### <span data-ttu-id="ad5e6-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ad5e6-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="ad5e6-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ad5e6-143">NOTES</span></span>

## <span data-ttu-id="ad5e6-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad5e6-144">RELATED LINKS</span></span>

[<span data-ttu-id="ad5e6-145">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ad5e6-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="ad5e6-146">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ad5e6-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="ad5e6-147">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ad5e6-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="ad5e6-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ad5e6-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="ad5e6-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ad5e6-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="ad5e6-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ad5e6-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)