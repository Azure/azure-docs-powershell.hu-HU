---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/reset-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
ms.openlocfilehash: c2373bb4ef093a35abc12b14f55f4c977fc54d64
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153795"
---
# <span data-ttu-id="5de2e-101">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5de2e-101">Reset-AzRedisCache</span></span>

## <span data-ttu-id="5de2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5de2e-102">SYNOPSIS</span></span>
<span data-ttu-id="5de2e-103">Egy gyorsítótár csomópontjainak újraindítása.</span><span class="sxs-lookup"><span data-stu-id="5de2e-103">Restarts nodes of a cache.</span></span>

## <span data-ttu-id="5de2e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5de2e-104">SYNTAX</span></span>

```
Reset-AzRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5de2e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5de2e-105">DESCRIPTION</span></span>
<span data-ttu-id="5de2e-106">A **Reset-AzRedisCache** parancsmag újraindítja egy Azure Redis Cache-példány csomópontját.</span><span class="sxs-lookup"><span data-stu-id="5de2e-106">The **Reset-AzRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="5de2e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5de2e-107">EXAMPLES</span></span>

### <span data-ttu-id="5de2e-108">1. példa: Mindkét csomópont újraindítása</span><span class="sxs-lookup"><span data-stu-id="5de2e-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="5de2e-109">Ez a parancs újraindítja a RedisCache06 nevű gyorsítótár mindkét csomópontját.</span><span class="sxs-lookup"><span data-stu-id="5de2e-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="5de2e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5de2e-110">PARAMETERS</span></span>

### <span data-ttu-id="5de2e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5de2e-111">-DefaultProfile</span></span>
<span data-ttu-id="5de2e-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5de2e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5de2e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5de2e-113">-Force</span></span>
<span data-ttu-id="5de2e-114">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="5de2e-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5de2e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5de2e-115">-Name</span></span>
<span data-ttu-id="5de2e-116">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5de2e-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="5de2e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5de2e-117">-PassThru</span></span>
<span data-ttu-id="5de2e-118">Azt jelzi, hogy ez a parancsmag egy logikai értéket ad vissza, amely jelzi, hogy a művelet sikeres-e.</span><span class="sxs-lookup"><span data-stu-id="5de2e-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="5de2e-119">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="5de2e-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5de2e-120">-RebootType</span><span class="sxs-lookup"><span data-stu-id="5de2e-120">-RebootType</span></span>
<span data-ttu-id="5de2e-121">Meghatározza, hogy melyik csomópontot vagy csomópontokat indítsa újra.</span><span class="sxs-lookup"><span data-stu-id="5de2e-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="5de2e-122">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="5de2e-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5de2e-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="5de2e-123">PrimaryNode</span></span> 
- <span data-ttu-id="5de2e-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="5de2e-124">SecondaryNode</span></span> 
- <span data-ttu-id="5de2e-125">AllNodes</span><span class="sxs-lookup"><span data-stu-id="5de2e-125">AllNodes</span></span>

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

### <span data-ttu-id="5de2e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5de2e-126">-ResourceGroupName</span></span>
<span data-ttu-id="5de2e-127">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5de2e-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="5de2e-128">-ShardId</span><span class="sxs-lookup"><span data-stu-id="5de2e-128">-ShardId</span></span>
<span data-ttu-id="5de2e-129">Annak a szegmensnek az azonosítóját adja meg, amely után a parancsmag újraindul egy olyan prémium szintű gyorsítótárban, amely engedélyezve van a fürtözéshez.</span><span class="sxs-lookup"><span data-stu-id="5de2e-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

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

### <span data-ttu-id="5de2e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5de2e-130">-Confirm</span></span>
<span data-ttu-id="5de2e-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5de2e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5de2e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5de2e-132">-WhatIf</span></span>
<span data-ttu-id="5de2e-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5de2e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5de2e-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5de2e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5de2e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5de2e-135">CommonParameters</span></span>
<span data-ttu-id="5de2e-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5de2e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5de2e-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5de2e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5de2e-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5de2e-138">INPUTS</span></span>

### <span data-ttu-id="5de2e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5de2e-139">System.String</span></span>

### <span data-ttu-id="5de2e-140">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5de2e-140">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5de2e-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5de2e-141">OUTPUTS</span></span>

### <span data-ttu-id="5de2e-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5de2e-142">System.Boolean</span></span>

## <span data-ttu-id="5de2e-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5de2e-143">NOTES</span></span>
* <span data-ttu-id="5de2e-144">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, redis, cache, web, webapp, webhely</span><span class="sxs-lookup"><span data-stu-id="5de2e-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="5de2e-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5de2e-145">RELATED LINKS</span></span>

[<span data-ttu-id="5de2e-146">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5de2e-146">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="5de2e-147">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5de2e-147">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="5de2e-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5de2e-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="5de2e-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5de2e-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="5de2e-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5de2e-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


