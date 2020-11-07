---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
ms.openlocfilehash: 4b7719a43535de4af595e634dea2061ab9cba19d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846934"
---
# <span data-ttu-id="1629a-101">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1629a-101">Remove-AzRedisCache</span></span>

## <span data-ttu-id="1629a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1629a-102">SYNOPSIS</span></span>
<span data-ttu-id="1629a-103">Eltávolítja a Redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="1629a-103">Removes a Redis Cache.</span></span>

## <span data-ttu-id="1629a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1629a-104">SYNTAX</span></span>

```
Remove-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1629a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1629a-105">DESCRIPTION</span></span>
<span data-ttu-id="1629a-106">A **Remove-AzRedisCache** parancsmag eltávolítja az Azure Redis-gyorsítótárát.</span><span class="sxs-lookup"><span data-stu-id="1629a-106">The **Remove-AzRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="1629a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1629a-107">EXAMPLES</span></span>

### <span data-ttu-id="1629a-108">1. példa: Redis-gyorsítótár eltávolítása és az eredmény visszaadása</span><span class="sxs-lookup"><span data-stu-id="1629a-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="1629a-109">Ez a parancs eltávolítja a Redis-gyorsítótárat, és megjeleníti, hogy a művelet sikeres-e.</span><span class="sxs-lookup"><span data-stu-id="1629a-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="1629a-110">2. példa: Redis-gyorsítótár eltávolítása, és az eredmény nem jeleníthető meg</span><span class="sxs-lookup"><span data-stu-id="1629a-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="1629a-111">Ez a parancs eltávolítja a Redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="1629a-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="1629a-112">Mivel a *PassThru* paraméter nincs megadva, a művelet eredménye nem jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="1629a-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="1629a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1629a-113">PARAMETERS</span></span>

### <span data-ttu-id="1629a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1629a-114">-DefaultProfile</span></span>
<span data-ttu-id="1629a-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1629a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1629a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1629a-116">-Force</span></span>
<span data-ttu-id="1629a-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="1629a-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1629a-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1629a-118">-Name</span></span>
<span data-ttu-id="1629a-119">Az eltávolítandó Redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1629a-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="1629a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1629a-120">-PassThru</span></span>
<span data-ttu-id="1629a-121">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="1629a-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1629a-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="1629a-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1629a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1629a-123">-ResourceGroupName</span></span>
<span data-ttu-id="1629a-124">Az eltávolítandó Redis-gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1629a-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="1629a-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1629a-125">-Confirm</span></span>
<span data-ttu-id="1629a-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1629a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1629a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1629a-127">-WhatIf</span></span>
<span data-ttu-id="1629a-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1629a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1629a-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1629a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1629a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1629a-130">CommonParameters</span></span>
<span data-ttu-id="1629a-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1629a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1629a-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1629a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1629a-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1629a-133">INPUTS</span></span>

### <span data-ttu-id="1629a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1629a-134">System.String</span></span>

## <span data-ttu-id="1629a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1629a-135">OUTPUTS</span></span>

### <span data-ttu-id="1629a-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1629a-136">System.Boolean</span></span>

## <span data-ttu-id="1629a-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1629a-137">NOTES</span></span>

## <span data-ttu-id="1629a-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1629a-138">RELATED LINKS</span></span>

[<span data-ttu-id="1629a-139">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1629a-139">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="1629a-140">Új – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1629a-140">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="1629a-141">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1629a-141">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


