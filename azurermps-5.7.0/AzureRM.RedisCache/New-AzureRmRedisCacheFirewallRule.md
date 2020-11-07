---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: c89589d966c03614255751bf13769689ff875332
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672516"
---
# <span data-ttu-id="2e553-101">New-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2e553-101">New-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="2e553-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e553-102">SYNOPSIS</span></span>
<span data-ttu-id="2e553-103">Tűzfal-szabály létrehozása Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="2e553-103">Create a firewall rule on a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e553-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e553-104">SYNTAX</span></span>

### <span data-ttu-id="2e553-105">NormalParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2e553-105">NormalParameterSet (Default)</span></span>
```
New-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String>
 -StartIP <String> -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e553-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="2e553-106">RedisCacheAttributesObject</span></span>
```
New-AzureRmRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e553-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e553-107">ResourceIdParameterSet</span></span>
```
New-AzureRmRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e553-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e553-108">DESCRIPTION</span></span>
<span data-ttu-id="2e553-109">Tűzfal-szabály létrehozása Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="2e553-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="2e553-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2e553-110">EXAMPLES</span></span>

### <span data-ttu-id="2e553-111">Példa 1: tűzfalszabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="2e553-111">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -StartIP "10.0.0.1" -EndIP "10.0.0.32"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="2e553-112">A parancs létrehozza a ruleone nevű Redis-gyorsítótárban a mycache nevű tűzfal-szabályt.</span><span class="sxs-lookup"><span data-stu-id="2e553-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="2e553-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e553-113">PARAMETERS</span></span>

### <span data-ttu-id="2e553-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e553-114">-DefaultProfile</span></span>
<span data-ttu-id="2e553-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e553-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e553-116">-ZáróIP</span><span class="sxs-lookup"><span data-stu-id="2e553-116">-EndIP</span></span>
<span data-ttu-id="2e553-117">Záró IP-cím.</span><span class="sxs-lookup"><span data-stu-id="2e553-117">Ending IP address.</span></span>

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

### <span data-ttu-id="2e553-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e553-118">-InputObject</span></span>
<span data-ttu-id="2e553-119">RedisCacheAttributes típusú objektum</span><span class="sxs-lookup"><span data-stu-id="2e553-119">object of type RedisCacheAttributes</span></span>

```yaml
Type: RedisCacheAttributes
Parameter Sets: RedisCacheAttributesObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e553-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2e553-120">-Name</span></span>
<span data-ttu-id="2e553-121">A Redis-gyorsítótár neve</span><span class="sxs-lookup"><span data-stu-id="2e553-121">Name of redis cache.</span></span>

```yaml
Type: String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e553-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e553-122">-ResourceGroupName</span></span>
<span data-ttu-id="2e553-123">Annak az erőforráscsoportnek a neve, amelyben a gyorsítótár létezik.</span><span class="sxs-lookup"><span data-stu-id="2e553-123">Name of resource group in which cache exists.</span></span>

```yaml
Type: String
Parameter Sets: NormalParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e553-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e553-124">-ResourceId</span></span>
<span data-ttu-id="2e553-125">A Redis-gyorsítótár ARM azonosítója</span><span class="sxs-lookup"><span data-stu-id="2e553-125">ARM Id of Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e553-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="2e553-126">-RuleName</span></span>
<span data-ttu-id="2e553-127">Tűzfal-szabály neve.</span><span class="sxs-lookup"><span data-stu-id="2e553-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="2e553-128">-KezdőIP</span><span class="sxs-lookup"><span data-stu-id="2e553-128">-StartIP</span></span>
<span data-ttu-id="2e553-129">Kezdő IP-cím.</span><span class="sxs-lookup"><span data-stu-id="2e553-129">Starting IP address.</span></span>

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

### <span data-ttu-id="2e553-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2e553-130">-Confirm</span></span>
<span data-ttu-id="2e553-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2e553-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e553-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e553-132">-WhatIf</span></span>
<span data-ttu-id="2e553-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2e553-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e553-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e553-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e553-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e553-135">CommonParameters</span></span>
<span data-ttu-id="2e553-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e553-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e553-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e553-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e553-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e553-138">INPUTS</span></span>

### <span data-ttu-id="2e553-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2e553-139">System.String</span></span>

## <span data-ttu-id="2e553-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e553-140">OUTPUTS</span></span>

### <span data-ttu-id="2e553-141">Microsoft. Azure. Command. RedisCache. models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2e553-141">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="2e553-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e553-142">NOTES</span></span>

## <span data-ttu-id="2e553-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e553-143">RELATED LINKS</span></span>

[<span data-ttu-id="2e553-144">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2e553-144">Get-AzureRmRedisCacheFirewallRule</span></span>](./Get-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="2e553-145">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2e553-145">Remove-AzureRmRedisCacheFirewallRule</span></span>](./Remove-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="2e553-146">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2e553-146">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="2e553-147">Új – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2e553-147">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="2e553-148">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2e553-148">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="2e553-149">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2e553-149">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
