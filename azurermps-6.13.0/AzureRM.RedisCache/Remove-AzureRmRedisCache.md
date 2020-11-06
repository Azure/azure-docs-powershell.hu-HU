---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
ms.openlocfilehash: 35b7d3e05cced593da748f430cb121da43cd0380
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501099"
---
# <span data-ttu-id="c8bef-101">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c8bef-101">Remove-AzureRmRedisCache</span></span>

## <span data-ttu-id="c8bef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c8bef-102">SYNOPSIS</span></span>
<span data-ttu-id="c8bef-103">Eltávolítja a Redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="c8bef-103">Removes a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8bef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c8bef-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8bef-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c8bef-105">DESCRIPTION</span></span>
<span data-ttu-id="c8bef-106">A **Remove-AzureRmRedisCache** parancsmag eltávolítja az Azure Redis-gyorsítótárát.</span><span class="sxs-lookup"><span data-stu-id="c8bef-106">The **Remove-AzureRmRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="c8bef-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c8bef-107">EXAMPLES</span></span>

### <span data-ttu-id="c8bef-108">1. példa: Redis-gyorsítótár eltávolítása és az eredmény visszaadása</span><span class="sxs-lookup"><span data-stu-id="c8bef-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="c8bef-109">Ez a parancs eltávolítja a Redis-gyorsítótárat, és megjeleníti, hogy a művelet sikeres-e.</span><span class="sxs-lookup"><span data-stu-id="c8bef-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="c8bef-110">2. példa: Redis-gyorsítótár eltávolítása, és az eredmény nem jeleníthető meg</span><span class="sxs-lookup"><span data-stu-id="c8bef-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="c8bef-111">Ez a parancs eltávolítja a Redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="c8bef-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="c8bef-112">Mivel a *PassThru* paraméter nincs megadva, a művelet eredménye nem jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="c8bef-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="c8bef-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c8bef-113">PARAMETERS</span></span>

### <span data-ttu-id="c8bef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8bef-114">-DefaultProfile</span></span>
<span data-ttu-id="c8bef-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8bef-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8bef-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c8bef-116">-Force</span></span>
<span data-ttu-id="c8bef-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="c8bef-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c8bef-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c8bef-118">-Name</span></span>
<span data-ttu-id="c8bef-119">Az eltávolítandó Redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8bef-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="c8bef-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8bef-120">-PassThru</span></span>
<span data-ttu-id="c8bef-121">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="c8bef-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c8bef-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="c8bef-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c8bef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8bef-123">-ResourceGroupName</span></span>
<span data-ttu-id="c8bef-124">Az eltávolítandó Redis-gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8bef-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="c8bef-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c8bef-125">-Confirm</span></span>
<span data-ttu-id="c8bef-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c8bef-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8bef-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8bef-127">-WhatIf</span></span>
<span data-ttu-id="c8bef-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c8bef-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8bef-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c8bef-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8bef-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8bef-130">CommonParameters</span></span>
<span data-ttu-id="c8bef-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c8bef-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8bef-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8bef-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8bef-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8bef-133">INPUTS</span></span>

### <span data-ttu-id="c8bef-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c8bef-134">System.String</span></span>

## <span data-ttu-id="c8bef-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8bef-135">OUTPUTS</span></span>

### <span data-ttu-id="c8bef-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c8bef-136">System.Boolean</span></span>

## <span data-ttu-id="c8bef-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c8bef-137">NOTES</span></span>

## <span data-ttu-id="c8bef-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8bef-138">RELATED LINKS</span></span>

[<span data-ttu-id="c8bef-139">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c8bef-139">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="c8bef-140">Új – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c8bef-140">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="c8bef-141">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c8bef-141">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


