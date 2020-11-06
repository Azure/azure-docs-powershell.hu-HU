---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
ms.openlocfilehash: 4e49fbd2ac2604dab09d79255e7134fee02afd97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495289"
---
# <span data-ttu-id="4a561-101">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4a561-101">Remove-AzureRmRedisCache</span></span>

## <span data-ttu-id="4a561-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4a561-102">SYNOPSIS</span></span>
<span data-ttu-id="4a561-103">Eltávolítja a Redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="4a561-103">Removes a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a561-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4a561-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a561-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4a561-105">DESCRIPTION</span></span>
<span data-ttu-id="4a561-106">A **Remove-AzureRmRedisCache** parancsmag eltávolítja az Azure Redis-gyorsítótárát.</span><span class="sxs-lookup"><span data-stu-id="4a561-106">The **Remove-AzureRmRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="4a561-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4a561-107">EXAMPLES</span></span>

### <span data-ttu-id="4a561-108">1. példa: Redis-gyorsítótár eltávolítása és az eredmény visszaadása</span><span class="sxs-lookup"><span data-stu-id="4a561-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="4a561-109">Ez a parancs eltávolítja a Redis-gyorsítótárat, és megjeleníti, hogy a művelet sikeres-e.</span><span class="sxs-lookup"><span data-stu-id="4a561-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="4a561-110">2. példa: Redis-gyorsítótár eltávolítása, és az eredmény nem jeleníthető meg</span><span class="sxs-lookup"><span data-stu-id="4a561-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="4a561-111">Ez a parancs eltávolítja a Redis-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="4a561-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="4a561-112">Mivel a *PassThru* paraméter nincs megadva, a művelet eredménye nem jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="4a561-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="4a561-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4a561-113">PARAMETERS</span></span>

### <span data-ttu-id="4a561-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a561-114">-DefaultProfile</span></span>
<span data-ttu-id="4a561-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4a561-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a561-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4a561-116">-Force</span></span>
<span data-ttu-id="4a561-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="4a561-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4a561-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4a561-118">-Name</span></span>
<span data-ttu-id="4a561-119">Az eltávolítandó Redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a561-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="4a561-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a561-120">-PassThru</span></span>
<span data-ttu-id="4a561-121">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="4a561-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4a561-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="4a561-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4a561-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a561-123">-ResourceGroupName</span></span>
<span data-ttu-id="4a561-124">Az eltávolítandó Redis-gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a561-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a561-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4a561-125">-Confirm</span></span>
<span data-ttu-id="4a561-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4a561-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a561-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a561-127">-WhatIf</span></span>
<span data-ttu-id="4a561-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4a561-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a561-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4a561-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a561-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a561-130">CommonParameters</span></span>
<span data-ttu-id="4a561-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4a561-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a561-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a561-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a561-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a561-133">INPUTS</span></span>

### <span data-ttu-id="4a561-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="4a561-134">None</span></span>
<span data-ttu-id="4a561-135">A parancsmagot név szerint, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="4a561-135">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="4a561-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a561-136">OUTPUTS</span></span>

### <span data-ttu-id="4a561-137">Logikai</span><span class="sxs-lookup"><span data-stu-id="4a561-137">Boolean</span></span>
<span data-ttu-id="4a561-138">A $True akkor ad eredményül, ha nincs kivétel.</span><span class="sxs-lookup"><span data-stu-id="4a561-138">Returns $True if no exception occurs.</span></span>

## <span data-ttu-id="4a561-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4a561-139">NOTES</span></span>

## <span data-ttu-id="4a561-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a561-140">RELATED LINKS</span></span>

[<span data-ttu-id="4a561-141">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4a561-141">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="4a561-142">Új – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4a561-142">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="4a561-143">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4a561-143">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


