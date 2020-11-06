---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
ms.openlocfilehash: b453b47da35addb8a04a19957c148c5ec1929e75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494724"
---
# <span data-ttu-id="fb35a-101">New-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="fb35a-101">New-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="fb35a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb35a-102">SYNOPSIS</span></span>
<span data-ttu-id="fb35a-103">Újra létrehoz egy Redis-gyorsítótár elérési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="fb35a-103">Regenerates the access key of a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb35a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb35a-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheKey -ResourceGroupName <String> -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb35a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb35a-105">DESCRIPTION</span></span>
<span data-ttu-id="fb35a-106">A **New-AzureRmRedisCacheKey** parancsmag újból létrehoz egy Azure Redis-gyorsítótár elérési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="fb35a-106">The **New-AzureRmRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="fb35a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fb35a-107">EXAMPLES</span></span>

### <span data-ttu-id="fb35a-108">1. példa: elsődleges kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="fb35a-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="fb35a-109">Ez a parancs újból létrehoz egy Redis-gyorsítótár elsődleges kulcsát.</span><span class="sxs-lookup"><span data-stu-id="fb35a-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="fb35a-110">2. példa: másodlagos kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="fb35a-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="fb35a-111">Ez a parancs újból létrehoz egy Redis-gyorsítótár másodlagos kulcsát.</span><span class="sxs-lookup"><span data-stu-id="fb35a-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="fb35a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb35a-112">PARAMETERS</span></span>

### <span data-ttu-id="fb35a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="fb35a-113">-Force</span></span>
<span data-ttu-id="fb35a-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="fb35a-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fb35a-115">-Típus</span><span class="sxs-lookup"><span data-stu-id="fb35a-115">-KeyType</span></span>
<span data-ttu-id="fb35a-116">Itt adhatja meg, hogy az elsődleges vagy másodlagos hozzáférési kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="fb35a-116">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="fb35a-117">Az érvényes értékek: elsődleges, másodlagos.</span><span class="sxs-lookup"><span data-stu-id="fb35a-117">Valid values are: Primary, Secondary.</span></span>

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

### <span data-ttu-id="fb35a-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fb35a-118">-Name</span></span>
<span data-ttu-id="fb35a-119">A Redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb35a-119">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="fb35a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb35a-120">-ResourceGroupName</span></span>
<span data-ttu-id="fb35a-121">A Redis-gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb35a-121">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="fb35a-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fb35a-122">-Confirm</span></span>
<span data-ttu-id="fb35a-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fb35a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb35a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb35a-124">-WhatIf</span></span>
<span data-ttu-id="fb35a-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fb35a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb35a-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb35a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb35a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb35a-127">-DefaultProfile</span></span>
<span data-ttu-id="fb35a-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb35a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb35a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb35a-129">CommonParameters</span></span>
<span data-ttu-id="fb35a-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb35a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb35a-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb35a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb35a-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb35a-132">INPUTS</span></span>

### <span data-ttu-id="fb35a-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="fb35a-133">None</span></span>
<span data-ttu-id="fb35a-134">A parancsmagot név szerint, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="fb35a-134">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="fb35a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb35a-135">OUTPUTS</span></span>

### <span data-ttu-id="fb35a-136">Microsoft. Azure. Management. Redis. models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="fb35a-136">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>
<span data-ttu-id="fb35a-137">Ez a parancsmag egy Redis-gyorsítótár elsődleges és másodlagos elérési kulcsát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="fb35a-137">This cmdlet returns the primary and secondary access key of a Redis Cache.</span></span>

## <span data-ttu-id="fb35a-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb35a-138">NOTES</span></span>

## <span data-ttu-id="fb35a-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb35a-139">RELATED LINKS</span></span>

[<span data-ttu-id="fb35a-140">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="fb35a-140">Get-AzureRmRedisCacheKey</span></span>](./Get-AzureRmRedisCacheKey.md)


