---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
ms.openlocfilehash: 2b352c649d01e2fceb42f99a6c4dad20859a2adc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672416"
---
# <span data-ttu-id="44b31-101">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="44b31-101">Reset-AzureRmRedisCache</span></span>

## <span data-ttu-id="44b31-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="44b31-102">SYNOPSIS</span></span>
<span data-ttu-id="44b31-103">Egy gyorsítótár csomópontjainak újraindítása.</span><span class="sxs-lookup"><span data-stu-id="44b31-103">Restarts nodes of a cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44b31-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="44b31-104">SYNTAX</span></span>

```
Reset-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44b31-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="44b31-105">DESCRIPTION</span></span>
<span data-ttu-id="44b31-106">A **reset-AzureRmRedisCache** parancsmag az Azure Redis-gyorsítótár-példány csomópontjait indítja újra.</span><span class="sxs-lookup"><span data-stu-id="44b31-106">The **Reset-AzureRmRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="44b31-107">Példák</span><span class="sxs-lookup"><span data-stu-id="44b31-107">EXAMPLES</span></span>

### <span data-ttu-id="44b31-108">Példa 1: mindkét csomópont újraindítása</span><span class="sxs-lookup"><span data-stu-id="44b31-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="44b31-109">Ez a parancs a RedisCache06 nevű gyorsítótárban mindkét csomópontot újraindul.</span><span class="sxs-lookup"><span data-stu-id="44b31-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="44b31-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="44b31-110">PARAMETERS</span></span>

### <span data-ttu-id="44b31-111">-Force</span><span class="sxs-lookup"><span data-stu-id="44b31-111">-Force</span></span>
<span data-ttu-id="44b31-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="44b31-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="44b31-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="44b31-113">-Name</span></span>
<span data-ttu-id="44b31-114">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="44b31-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="44b31-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44b31-115">-PassThru</span></span>
<span data-ttu-id="44b31-116">Jelzi, hogy ez a parancsmag olyan logikai értéket ad eredményül, amely azt jelzi, hogy a művelet sikerül-e.</span><span class="sxs-lookup"><span data-stu-id="44b31-116">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="44b31-117">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="44b31-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="44b31-118">-RebootType</span><span class="sxs-lookup"><span data-stu-id="44b31-118">-RebootType</span></span>
<span data-ttu-id="44b31-119">Az újraindítani kívánt csomópontot vagy csomópontokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="44b31-119">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="44b31-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="44b31-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="44b31-121">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="44b31-121">PrimaryNode</span></span> 
- <span data-ttu-id="44b31-122">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="44b31-122">SecondaryNode</span></span> 
- <span data-ttu-id="44b31-123">AllNodes</span><span class="sxs-lookup"><span data-stu-id="44b31-123">AllNodes</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryNode, SecondaryNode, AllNodes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44b31-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44b31-124">-ResourceGroupName</span></span>
<span data-ttu-id="44b31-125">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="44b31-125">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="44b31-126">-ShardId</span><span class="sxs-lookup"><span data-stu-id="44b31-126">-ShardId</span></span>
<span data-ttu-id="44b31-127">Annak a szilánknak az AZONOSÍTÓját adja meg, amelyre a parancsmag engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="44b31-127">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44b31-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="44b31-128">-Confirm</span></span>
<span data-ttu-id="44b31-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="44b31-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b31-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44b31-130">-WhatIf</span></span>
<span data-ttu-id="44b31-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="44b31-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44b31-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="44b31-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b31-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44b31-133">-DefaultProfile</span></span>
<span data-ttu-id="44b31-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44b31-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b31-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44b31-135">CommonParameters</span></span>
<span data-ttu-id="44b31-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="44b31-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44b31-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44b31-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44b31-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="44b31-138">INPUTS</span></span>

### <span data-ttu-id="44b31-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="44b31-139">None</span></span>
<span data-ttu-id="44b31-140">A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="44b31-140">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="44b31-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44b31-141">OUTPUTS</span></span>

### <span data-ttu-id="44b31-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="44b31-142">None</span></span>

## <span data-ttu-id="44b31-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="44b31-143">NOTES</span></span>
* <span data-ttu-id="44b31-144">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="44b31-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="44b31-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44b31-145">RELATED LINKS</span></span>

[<span data-ttu-id="44b31-146">Exportálás – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="44b31-146">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="44b31-147">Importálás – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="44b31-147">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="44b31-148">Új – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="44b31-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="44b31-149">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="44b31-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="44b31-150">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="44b31-150">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


