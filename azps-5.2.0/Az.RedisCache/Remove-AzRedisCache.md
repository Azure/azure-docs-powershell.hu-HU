---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
ms.openlocfilehash: 4b7719a43535de4af595e634dea2061ab9cba19d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344154"
---
# <span data-ttu-id="df9d3-101">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="df9d3-101">Remove-AzRedisCache</span></span>

## <span data-ttu-id="df9d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df9d3-102">SYNOPSIS</span></span>
<span data-ttu-id="df9d3-103">A redis-gyorsítótár eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="df9d3-103">Removes a Redis Cache.</span></span>

## <span data-ttu-id="df9d3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="df9d3-104">SYNTAX</span></span>

```
Remove-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df9d3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="df9d3-105">DESCRIPTION</span></span>
<span data-ttu-id="df9d3-106">A **Remove-AzRedisCache** parancsmag eltávolítja az Azure Redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="df9d3-106">The **Remove-AzRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="df9d3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="df9d3-107">EXAMPLES</span></span>

### <span data-ttu-id="df9d3-108">1. példa: A redis cache eltávolítása és az eredmény visszaadése</span><span class="sxs-lookup"><span data-stu-id="df9d3-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="df9d3-109">Ez a parancs eltávolítja a redis cache-t, és megjeleníti, hogy a művelet sikeres-e.</span><span class="sxs-lookup"><span data-stu-id="df9d3-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="df9d3-110">2. példa: A redis cache eltávolítása, és az eredmény nem jelenik meg</span><span class="sxs-lookup"><span data-stu-id="df9d3-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="df9d3-111">Ez a parancs eltávolítja a redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="df9d3-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="df9d3-112">Mivel a *PassThru* paraméter nincs megadva, a művelet eredménye nem jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="df9d3-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="df9d3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df9d3-113">PARAMETERS</span></span>

### <span data-ttu-id="df9d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df9d3-114">-DefaultProfile</span></span>
<span data-ttu-id="df9d3-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df9d3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df9d3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="df9d3-116">-Force</span></span>
<span data-ttu-id="df9d3-117">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="df9d3-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="df9d3-118">-Name</span><span class="sxs-lookup"><span data-stu-id="df9d3-118">-Name</span></span>
<span data-ttu-id="df9d3-119">Az eltávolítható redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df9d3-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="df9d3-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df9d3-120">-PassThru</span></span>
<span data-ttu-id="df9d3-121">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="df9d3-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="df9d3-122">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="df9d3-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="df9d3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df9d3-123">-ResourceGroupName</span></span>
<span data-ttu-id="df9d3-124">Annak az erőforráscsoportnak a neve, amely az eltávolítható Redis cache-t tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="df9d3-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="df9d3-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df9d3-125">-Confirm</span></span>
<span data-ttu-id="df9d3-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="df9d3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df9d3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df9d3-127">-WhatIf</span></span>
<span data-ttu-id="df9d3-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="df9d3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df9d3-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df9d3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df9d3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df9d3-130">CommonParameters</span></span>
<span data-ttu-id="df9d3-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df9d3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df9d3-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df9d3-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df9d3-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df9d3-133">INPUTS</span></span>

### <span data-ttu-id="df9d3-134">System.String</span><span class="sxs-lookup"><span data-stu-id="df9d3-134">System.String</span></span>

## <span data-ttu-id="df9d3-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df9d3-135">OUTPUTS</span></span>

### <span data-ttu-id="df9d3-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="df9d3-136">System.Boolean</span></span>

## <span data-ttu-id="df9d3-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="df9d3-137">NOTES</span></span>

## <span data-ttu-id="df9d3-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df9d3-138">RELATED LINKS</span></span>

[<span data-ttu-id="df9d3-139">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="df9d3-139">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="df9d3-140">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="df9d3-140">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="df9d3-141">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="df9d3-141">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


