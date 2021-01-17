---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
ms.openlocfilehash: 4b7719a43535de4af595e634dea2061ab9cba19d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466621"
---
# <span data-ttu-id="26ea2-101">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="26ea2-101">Remove-AzRedisCache</span></span>

## <span data-ttu-id="26ea2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26ea2-102">SYNOPSIS</span></span>
<span data-ttu-id="26ea2-103">A redis-gyorsítótár eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="26ea2-103">Removes a Redis Cache.</span></span>

## <span data-ttu-id="26ea2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="26ea2-104">SYNTAX</span></span>

```
Remove-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26ea2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="26ea2-105">DESCRIPTION</span></span>
<span data-ttu-id="26ea2-106">A **Remove-AzRedisCache** parancsmag eltávolítja az Azure Redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="26ea2-106">The **Remove-AzRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="26ea2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="26ea2-107">EXAMPLES</span></span>

### <span data-ttu-id="26ea2-108">1. példa: A redis cache eltávolítása és az eredmény visszaadése</span><span class="sxs-lookup"><span data-stu-id="26ea2-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="26ea2-109">Ez a parancs eltávolítja a redis cache-t, és megjeleníti, hogy a művelet sikeres-e.</span><span class="sxs-lookup"><span data-stu-id="26ea2-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="26ea2-110">2. példa: A redis cache eltávolítása, és az eredmény nem jelenik meg</span><span class="sxs-lookup"><span data-stu-id="26ea2-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="26ea2-111">Ez a parancs eltávolítja a redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="26ea2-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="26ea2-112">Mivel a *PassThru* paraméter nincs megadva, a művelet eredménye nem jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="26ea2-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="26ea2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26ea2-113">PARAMETERS</span></span>

### <span data-ttu-id="26ea2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26ea2-114">-DefaultProfile</span></span>
<span data-ttu-id="26ea2-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26ea2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26ea2-116">-Force</span><span class="sxs-lookup"><span data-stu-id="26ea2-116">-Force</span></span>
<span data-ttu-id="26ea2-117">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="26ea2-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="26ea2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="26ea2-118">-Name</span></span>
<span data-ttu-id="26ea2-119">Az eltávolítható redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26ea2-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="26ea2-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26ea2-120">-PassThru</span></span>
<span data-ttu-id="26ea2-121">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="26ea2-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="26ea2-122">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="26ea2-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="26ea2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26ea2-123">-ResourceGroupName</span></span>
<span data-ttu-id="26ea2-124">Annak az erőforráscsoportnak a neve, amely az eltávolítható Redis cache-t tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="26ea2-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="26ea2-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26ea2-125">-Confirm</span></span>
<span data-ttu-id="26ea2-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="26ea2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26ea2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26ea2-127">-WhatIf</span></span>
<span data-ttu-id="26ea2-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="26ea2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26ea2-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="26ea2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26ea2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26ea2-130">CommonParameters</span></span>
<span data-ttu-id="26ea2-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26ea2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26ea2-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26ea2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26ea2-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26ea2-133">INPUTS</span></span>

### <span data-ttu-id="26ea2-134">System.String</span><span class="sxs-lookup"><span data-stu-id="26ea2-134">System.String</span></span>

## <span data-ttu-id="26ea2-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26ea2-135">OUTPUTS</span></span>

### <span data-ttu-id="26ea2-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="26ea2-136">System.Boolean</span></span>

## <span data-ttu-id="26ea2-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="26ea2-137">NOTES</span></span>

## <span data-ttu-id="26ea2-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26ea2-138">RELATED LINKS</span></span>

[<span data-ttu-id="26ea2-139">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="26ea2-139">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="26ea2-140">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="26ea2-140">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="26ea2-141">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="26ea2-141">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


