---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
ms.openlocfilehash: f48d49a59b21cbae3f314926f4de92e74a2b10e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206159"
---
# <span data-ttu-id="3b572-101">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="3b572-101">New-AzRedisCacheKey</span></span>

## <span data-ttu-id="3b572-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b572-102">SYNOPSIS</span></span>
<span data-ttu-id="3b572-103">A redis-gyorsítótár hozzáférési kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="3b572-103">Regenerates the access key of a Redis Cache.</span></span>

## <span data-ttu-id="3b572-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3b572-104">SYNTAX</span></span>

```
New-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b572-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3b572-105">DESCRIPTION</span></span>
<span data-ttu-id="3b572-106">A **New-AzRedisCacheKey** parancsmag újragenerálja az Azure Redis-gyorsítótár hozzáférési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="3b572-106">The **New-AzRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="3b572-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3b572-107">EXAMPLES</span></span>

### <span data-ttu-id="3b572-108">1. példa: Elsődleges kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="3b572-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="3b572-109">Ez a parancs újra létrehozza a redis-gyorsítótár elsődleges kulcsát.</span><span class="sxs-lookup"><span data-stu-id="3b572-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="3b572-110">2. példa: Másodlagos kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="3b572-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="3b572-111">Ez a parancs újra létrehozza a redis-gyorsítótár másodlagos kulcsát.</span><span class="sxs-lookup"><span data-stu-id="3b572-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="3b572-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b572-112">PARAMETERS</span></span>

### <span data-ttu-id="3b572-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b572-113">-DefaultProfile</span></span>
<span data-ttu-id="3b572-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b572-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b572-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3b572-115">-Force</span></span>
<span data-ttu-id="3b572-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="3b572-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3b572-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="3b572-117">-KeyType</span></span>
<span data-ttu-id="3b572-118">Azt adja meg, hogy az elsődleges vagy másodlagos hozzáférési kulcs újragenerálva legyen-e.</span><span class="sxs-lookup"><span data-stu-id="3b572-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="3b572-119">Érvényes értékek: Elsődleges, Másodlagos.</span><span class="sxs-lookup"><span data-stu-id="3b572-119">Valid values are: Primary, Secondary.</span></span>

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

### <span data-ttu-id="3b572-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3b572-120">-Name</span></span>
<span data-ttu-id="3b572-121">A redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b572-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="3b572-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b572-122">-ResourceGroupName</span></span>
<span data-ttu-id="3b572-123">A Redis cache-t tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b572-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="3b572-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b572-124">-Confirm</span></span>
<span data-ttu-id="3b572-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3b572-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b572-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b572-126">-WhatIf</span></span>
<span data-ttu-id="3b572-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3b572-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b572-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3b572-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b572-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b572-129">CommonParameters</span></span>
<span data-ttu-id="3b572-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b572-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b572-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b572-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b572-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3b572-132">INPUTS</span></span>

### <span data-ttu-id="3b572-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3b572-133">System.String</span></span>

## <span data-ttu-id="3b572-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b572-134">OUTPUTS</span></span>

### <span data-ttu-id="3b572-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="3b572-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="3b572-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3b572-136">NOTES</span></span>

## <span data-ttu-id="3b572-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b572-137">RELATED LINKS</span></span>

[<span data-ttu-id="3b572-138">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="3b572-138">Get-AzRedisCacheKey</span></span>](./Get-AzRedisCacheKey.md)


