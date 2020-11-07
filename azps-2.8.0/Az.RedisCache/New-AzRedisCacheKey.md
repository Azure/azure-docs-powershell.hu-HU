---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
ms.openlocfilehash: fb9a46037aa550ee252546a5c7f4345299d4ffba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838516"
---
# <span data-ttu-id="2622b-101">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="2622b-101">New-AzRedisCacheKey</span></span>

## <span data-ttu-id="2622b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2622b-102">SYNOPSIS</span></span>
<span data-ttu-id="2622b-103">Újra létrehoz egy Redis-gyorsítótár elérési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="2622b-103">Regenerates the access key of a Redis Cache.</span></span>

## <span data-ttu-id="2622b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2622b-104">SYNTAX</span></span>

```
New-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2622b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2622b-105">DESCRIPTION</span></span>
<span data-ttu-id="2622b-106">A **New-AzRedisCacheKey** parancsmag újból létrehoz egy Azure Redis-gyorsítótár elérési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="2622b-106">The **New-AzRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="2622b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2622b-107">EXAMPLES</span></span>

### <span data-ttu-id="2622b-108">1. példa: elsődleges kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="2622b-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="2622b-109">Ez a parancs újból létrehoz egy Redis-gyorsítótár elsődleges kulcsát.</span><span class="sxs-lookup"><span data-stu-id="2622b-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="2622b-110">2. példa: másodlagos kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="2622b-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="2622b-111">Ez a parancs újból létrehoz egy Redis-gyorsítótár másodlagos kulcsát.</span><span class="sxs-lookup"><span data-stu-id="2622b-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="2622b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2622b-112">PARAMETERS</span></span>

### <span data-ttu-id="2622b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2622b-113">-DefaultProfile</span></span>
<span data-ttu-id="2622b-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2622b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2622b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2622b-115">-Force</span></span>
<span data-ttu-id="2622b-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="2622b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2622b-117">-Típus</span><span class="sxs-lookup"><span data-stu-id="2622b-117">-KeyType</span></span>
<span data-ttu-id="2622b-118">Itt adhatja meg, hogy az elsődleges vagy másodlagos hozzáférési kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="2622b-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="2622b-119">Az érvényes értékek: elsődleges, másodlagos.</span><span class="sxs-lookup"><span data-stu-id="2622b-119">Valid values are: Primary, Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2622b-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2622b-120">-Name</span></span>
<span data-ttu-id="2622b-121">A Redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2622b-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="2622b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2622b-122">-ResourceGroupName</span></span>
<span data-ttu-id="2622b-123">A Redis-gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2622b-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="2622b-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2622b-124">-Confirm</span></span>
<span data-ttu-id="2622b-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2622b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2622b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2622b-126">-WhatIf</span></span>
<span data-ttu-id="2622b-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2622b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2622b-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2622b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2622b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2622b-129">CommonParameters</span></span>
<span data-ttu-id="2622b-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2622b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2622b-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2622b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2622b-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2622b-132">INPUTS</span></span>

### <span data-ttu-id="2622b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2622b-133">System.String</span></span>

## <span data-ttu-id="2622b-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2622b-134">OUTPUTS</span></span>

### <span data-ttu-id="2622b-135">Microsoft. Azure. Management. Redis. models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="2622b-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="2622b-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2622b-136">NOTES</span></span>

## <span data-ttu-id="2622b-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2622b-137">RELATED LINKS</span></span>

[<span data-ttu-id="2622b-138">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="2622b-138">Get-AzRedisCacheKey</span></span>](./Get-AzRedisCacheKey.md)


