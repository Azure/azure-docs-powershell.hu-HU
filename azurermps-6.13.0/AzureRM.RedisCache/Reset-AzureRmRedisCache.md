---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/reset-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
ms.openlocfilehash: 8aad14bde950a5e98d8d9331428a62e957cb0afe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503424"
---
# <span data-ttu-id="cd387-101">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="cd387-101">Reset-AzureRmRedisCache</span></span>

## <span data-ttu-id="cd387-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd387-102">SYNOPSIS</span></span>
<span data-ttu-id="cd387-103">Egy gyorsítótár csomópontjainak újraindítása.</span><span class="sxs-lookup"><span data-stu-id="cd387-103">Restarts nodes of a cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd387-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd387-104">SYNTAX</span></span>

```
Reset-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd387-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd387-105">DESCRIPTION</span></span>
<span data-ttu-id="cd387-106">A **reset-AzureRmRedisCache** parancsmag az Azure Redis-gyorsítótár-példány csomópontjait indítja újra.</span><span class="sxs-lookup"><span data-stu-id="cd387-106">The **Reset-AzureRmRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="cd387-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cd387-107">EXAMPLES</span></span>

### <span data-ttu-id="cd387-108">Példa 1: mindkét csomópont újraindítása</span><span class="sxs-lookup"><span data-stu-id="cd387-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="cd387-109">Ez a parancs a RedisCache06 nevű gyorsítótárban mindkét csomópontot újraindul.</span><span class="sxs-lookup"><span data-stu-id="cd387-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="cd387-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd387-110">PARAMETERS</span></span>

### <span data-ttu-id="cd387-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd387-111">-DefaultProfile</span></span>
<span data-ttu-id="cd387-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd387-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd387-113">-Force</span><span class="sxs-lookup"><span data-stu-id="cd387-113">-Force</span></span>
<span data-ttu-id="cd387-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="cd387-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cd387-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cd387-115">-Name</span></span>
<span data-ttu-id="cd387-116">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd387-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="cd387-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd387-117">-PassThru</span></span>
<span data-ttu-id="cd387-118">Jelzi, hogy ez a parancsmag olyan logikai értéket ad eredményül, amely azt jelzi, hogy a művelet sikerül-e.</span><span class="sxs-lookup"><span data-stu-id="cd387-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="cd387-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="cd387-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cd387-120">-RebootType</span><span class="sxs-lookup"><span data-stu-id="cd387-120">-RebootType</span></span>
<span data-ttu-id="cd387-121">Az újraindítani kívánt csomópontot vagy csomópontokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd387-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="cd387-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="cd387-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cd387-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="cd387-123">PrimaryNode</span></span> 
- <span data-ttu-id="cd387-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="cd387-124">SecondaryNode</span></span> 
- <span data-ttu-id="cd387-125">AllNodes</span><span class="sxs-lookup"><span data-stu-id="cd387-125">AllNodes</span></span>

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

### <span data-ttu-id="cd387-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd387-126">-ResourceGroupName</span></span>
<span data-ttu-id="cd387-127">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd387-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="cd387-128">-ShardId</span><span class="sxs-lookup"><span data-stu-id="cd387-128">-ShardId</span></span>
<span data-ttu-id="cd387-129">Annak a szilánknak az AZONOSÍTÓját adja meg, amelyre a parancsmag engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="cd387-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

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

### <span data-ttu-id="cd387-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cd387-130">-Confirm</span></span>
<span data-ttu-id="cd387-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cd387-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd387-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd387-132">-WhatIf</span></span>
<span data-ttu-id="cd387-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cd387-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd387-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cd387-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd387-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd387-135">CommonParameters</span></span>
<span data-ttu-id="cd387-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd387-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd387-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd387-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd387-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd387-138">INPUTS</span></span>

### <span data-ttu-id="cd387-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cd387-139">System.String</span></span>

### <span data-ttu-id="cd387-140">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="cd387-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="cd387-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd387-141">OUTPUTS</span></span>

### <span data-ttu-id="cd387-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cd387-142">System.Boolean</span></span>

## <span data-ttu-id="cd387-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd387-143">NOTES</span></span>
* <span data-ttu-id="cd387-144">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="cd387-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="cd387-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd387-145">RELATED LINKS</span></span>

[<span data-ttu-id="cd387-146">Exportálás – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="cd387-146">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="cd387-147">Importálás – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="cd387-147">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="cd387-148">Új – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="cd387-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="cd387-149">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="cd387-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="cd387-150">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="cd387-150">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


