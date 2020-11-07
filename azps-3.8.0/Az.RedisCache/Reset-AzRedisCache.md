---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/reset-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
ms.openlocfilehash: c2373bb4ef093a35abc12b14f55f4c977fc54d64
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846921"
---
# <span data-ttu-id="17278-101">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="17278-101">Reset-AzRedisCache</span></span>

## <span data-ttu-id="17278-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="17278-102">SYNOPSIS</span></span>
<span data-ttu-id="17278-103">Egy gyorsítótár csomópontjainak újraindítása.</span><span class="sxs-lookup"><span data-stu-id="17278-103">Restarts nodes of a cache.</span></span>

## <span data-ttu-id="17278-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="17278-104">SYNTAX</span></span>

```
Reset-AzRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17278-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="17278-105">DESCRIPTION</span></span>
<span data-ttu-id="17278-106">A **reset-AzRedisCache** parancsmag az Azure Redis-gyorsítótár-példány csomópontjait indítja újra.</span><span class="sxs-lookup"><span data-stu-id="17278-106">The **Reset-AzRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="17278-107">Példák</span><span class="sxs-lookup"><span data-stu-id="17278-107">EXAMPLES</span></span>

### <span data-ttu-id="17278-108">Példa 1: mindkét csomópont újraindítása</span><span class="sxs-lookup"><span data-stu-id="17278-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="17278-109">Ez a parancs a RedisCache06 nevű gyorsítótárban mindkét csomópontot újraindul.</span><span class="sxs-lookup"><span data-stu-id="17278-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="17278-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="17278-110">PARAMETERS</span></span>

### <span data-ttu-id="17278-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17278-111">-DefaultProfile</span></span>
<span data-ttu-id="17278-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="17278-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17278-113">-Force</span><span class="sxs-lookup"><span data-stu-id="17278-113">-Force</span></span>
<span data-ttu-id="17278-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="17278-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="17278-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="17278-115">-Name</span></span>
<span data-ttu-id="17278-116">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="17278-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="17278-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17278-117">-PassThru</span></span>
<span data-ttu-id="17278-118">Jelzi, hogy ez a parancsmag olyan logikai értéket ad eredményül, amely azt jelzi, hogy a művelet sikerül-e.</span><span class="sxs-lookup"><span data-stu-id="17278-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="17278-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="17278-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="17278-120">-RebootType</span><span class="sxs-lookup"><span data-stu-id="17278-120">-RebootType</span></span>
<span data-ttu-id="17278-121">Az újraindítani kívánt csomópontot vagy csomópontokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="17278-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="17278-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="17278-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="17278-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="17278-123">PrimaryNode</span></span> 
- <span data-ttu-id="17278-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="17278-124">SecondaryNode</span></span> 
- <span data-ttu-id="17278-125">AllNodes</span><span class="sxs-lookup"><span data-stu-id="17278-125">AllNodes</span></span>

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

### <span data-ttu-id="17278-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17278-126">-ResourceGroupName</span></span>
<span data-ttu-id="17278-127">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="17278-127">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17278-128">-ShardId</span><span class="sxs-lookup"><span data-stu-id="17278-128">-ShardId</span></span>
<span data-ttu-id="17278-129">Annak a szilánknak az AZONOSÍTÓját adja meg, amelyre a parancsmag engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="17278-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

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

### <span data-ttu-id="17278-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="17278-130">-Confirm</span></span>
<span data-ttu-id="17278-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="17278-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17278-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17278-132">-WhatIf</span></span>
<span data-ttu-id="17278-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="17278-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17278-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="17278-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17278-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17278-135">CommonParameters</span></span>
<span data-ttu-id="17278-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="17278-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17278-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17278-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17278-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="17278-138">INPUTS</span></span>

### <span data-ttu-id="17278-139">System. String</span><span class="sxs-lookup"><span data-stu-id="17278-139">System.String</span></span>

### <span data-ttu-id="17278-140">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="17278-140">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="17278-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17278-141">OUTPUTS</span></span>

### <span data-ttu-id="17278-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="17278-142">System.Boolean</span></span>

## <span data-ttu-id="17278-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="17278-143">NOTES</span></span>
* <span data-ttu-id="17278-144">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="17278-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="17278-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17278-145">RELATED LINKS</span></span>

[<span data-ttu-id="17278-146">Exportálás – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="17278-146">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="17278-147">Importálás – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="17278-147">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="17278-148">Új – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="17278-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="17278-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="17278-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="17278-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="17278-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)

