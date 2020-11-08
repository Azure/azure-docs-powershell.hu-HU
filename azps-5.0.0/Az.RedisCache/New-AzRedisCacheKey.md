---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
ms.openlocfilehash: f48d49a59b21cbae3f314926f4de92e74a2b10e8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195551"
---
# <span data-ttu-id="18e1a-101">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="18e1a-101">New-AzRedisCacheKey</span></span>

## <span data-ttu-id="18e1a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="18e1a-102">SYNOPSIS</span></span>
<span data-ttu-id="18e1a-103">Újra létrehoz egy Redis-gyorsítótár elérési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="18e1a-103">Regenerates the access key of a Redis Cache.</span></span>

## <span data-ttu-id="18e1a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="18e1a-104">SYNTAX</span></span>

```
New-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18e1a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="18e1a-105">DESCRIPTION</span></span>
<span data-ttu-id="18e1a-106">A **New-AzRedisCacheKey** parancsmag újból létrehoz egy Azure Redis-gyorsítótár elérési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="18e1a-106">The **New-AzRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="18e1a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="18e1a-107">EXAMPLES</span></span>

### <span data-ttu-id="18e1a-108">1. példa: elsődleges kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="18e1a-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="18e1a-109">Ez a parancs újból létrehoz egy Redis-gyorsítótár elsődleges kulcsát.</span><span class="sxs-lookup"><span data-stu-id="18e1a-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="18e1a-110">2. példa: másodlagos kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="18e1a-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="18e1a-111">Ez a parancs újból létrehoz egy Redis-gyorsítótár másodlagos kulcsát.</span><span class="sxs-lookup"><span data-stu-id="18e1a-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="18e1a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="18e1a-112">PARAMETERS</span></span>

### <span data-ttu-id="18e1a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18e1a-113">-DefaultProfile</span></span>
<span data-ttu-id="18e1a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18e1a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18e1a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="18e1a-115">-Force</span></span>
<span data-ttu-id="18e1a-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="18e1a-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="18e1a-117">-Típus</span><span class="sxs-lookup"><span data-stu-id="18e1a-117">-KeyType</span></span>
<span data-ttu-id="18e1a-118">Itt adhatja meg, hogy az elsődleges vagy másodlagos hozzáférési kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="18e1a-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="18e1a-119">Az érvényes értékek: elsődleges, másodlagos.</span><span class="sxs-lookup"><span data-stu-id="18e1a-119">Valid values are: Primary, Secondary.</span></span>

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

### <span data-ttu-id="18e1a-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="18e1a-120">-Name</span></span>
<span data-ttu-id="18e1a-121">A Redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="18e1a-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="18e1a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18e1a-122">-ResourceGroupName</span></span>
<span data-ttu-id="18e1a-123">A Redis-gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="18e1a-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="18e1a-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="18e1a-124">-Confirm</span></span>
<span data-ttu-id="18e1a-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="18e1a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18e1a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18e1a-126">-WhatIf</span></span>
<span data-ttu-id="18e1a-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="18e1a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18e1a-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="18e1a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18e1a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18e1a-129">CommonParameters</span></span>
<span data-ttu-id="18e1a-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="18e1a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18e1a-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18e1a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18e1a-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="18e1a-132">INPUTS</span></span>

### <span data-ttu-id="18e1a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="18e1a-133">System.String</span></span>

## <span data-ttu-id="18e1a-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18e1a-134">OUTPUTS</span></span>

### <span data-ttu-id="18e1a-135">Microsoft. Azure. Management. Redis. models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="18e1a-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="18e1a-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="18e1a-136">NOTES</span></span>

## <span data-ttu-id="18e1a-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18e1a-137">RELATED LINKS</span></span>

[<span data-ttu-id="18e1a-138">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="18e1a-138">Get-AzRedisCacheKey</span></span>](./Get-AzRedisCacheKey.md)

