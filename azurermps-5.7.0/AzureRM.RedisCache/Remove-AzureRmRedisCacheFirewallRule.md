---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 7f2e9a3bb54aab9def9eba7bdc2a84680fe121c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492202"
---
# <span data-ttu-id="e0816-101">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e0816-101">Remove-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="e0816-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0816-102">SYNOPSIS</span></span>
<span data-ttu-id="e0816-103">Tűzfalszabály eltávolítása Redis-gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="e0816-103">Remove a firewall rule from a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0816-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0816-104">SYNTAX</span></span>

### <span data-ttu-id="e0816-105">NormalParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e0816-105">NormalParameterSet (Default)</span></span>
```
Remove-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0816-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="e0816-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzureRmRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0816-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0816-107">DESCRIPTION</span></span>
<span data-ttu-id="e0816-108">Tűzfalszabály eltávolítása Redis-gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="e0816-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="e0816-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e0816-109">EXAMPLES</span></span>

### <span data-ttu-id="e0816-110">1. példa: egyetlen tűzfalszabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e0816-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="e0816-111">Ez a parancs eltávolítja a ruleone nevű tűzfal-szabályt a mycache nevű Redis-gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="e0816-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="e0816-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0816-112">PARAMETERS</span></span>

### <span data-ttu-id="e0816-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0816-113">-DefaultProfile</span></span>
<span data-ttu-id="e0816-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0816-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0816-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0816-115">-InputObject</span></span>
<span data-ttu-id="e0816-116">PSRedisFirewallRule típusú objektum</span><span class="sxs-lookup"><span data-stu-id="e0816-116">object of type PSRedisFirewallRule</span></span>

```yaml
Type: PSRedisFirewallRule
Parameter Sets: PSRedisFirewallRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0816-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e0816-117">-Name</span></span>
<span data-ttu-id="e0816-118">A Redis-gyorsítótár neve</span><span class="sxs-lookup"><span data-stu-id="e0816-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="e0816-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0816-119">-PassThru</span></span>
<span data-ttu-id="e0816-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e0816-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0816-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0816-121">-ResourceGroupName</span></span>
<span data-ttu-id="e0816-122">Annak az erőforráscsoportnek a neve, amelyben a gyorsítótár létezik.</span><span class="sxs-lookup"><span data-stu-id="e0816-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="e0816-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="e0816-123">-RuleName</span></span>
<span data-ttu-id="e0816-124">Tűzfal-szabály neve.</span><span class="sxs-lookup"><span data-stu-id="e0816-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="e0816-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e0816-125">-Confirm</span></span>
<span data-ttu-id="e0816-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e0816-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0816-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0816-127">-WhatIf</span></span>
<span data-ttu-id="e0816-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e0816-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0816-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e0816-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0816-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0816-130">CommonParameters</span></span>
<span data-ttu-id="e0816-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0816-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0816-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0816-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0816-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0816-133">INPUTS</span></span>

### <span data-ttu-id="e0816-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e0816-134">System.String</span></span>

## <span data-ttu-id="e0816-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0816-135">OUTPUTS</span></span>

### <span data-ttu-id="e0816-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e0816-136">System.Boolean</span></span>

## <span data-ttu-id="e0816-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0816-137">NOTES</span></span>

## <span data-ttu-id="e0816-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0816-138">RELATED LINKS</span></span>

[<span data-ttu-id="e0816-139">Új – AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e0816-139">New-AzureRmRedisCacheFirewallRule</span></span>](./New-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="e0816-140">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e0816-140">Get-AzureRmRedisCacheFirewallRule</span></span>](./Get-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="e0816-141">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e0816-141">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="e0816-142">Új – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e0816-142">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="e0816-143">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e0816-143">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="e0816-144">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e0816-144">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
