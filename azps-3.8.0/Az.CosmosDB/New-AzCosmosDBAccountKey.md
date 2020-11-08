---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccountKey.md
ms.openlocfilehash: a9cea343a67e7e23e820c0995484aab9a1434f90
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011917"
---
# <span data-ttu-id="73092-101">New-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="73092-101">New-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="73092-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="73092-102">SYNOPSIS</span></span>
<span data-ttu-id="73092-103">Adott CosmosDB-fiók újragenerálása</span><span class="sxs-lookup"><span data-stu-id="73092-103">Regenerate a given CosmosDB Account Key.</span></span>

## <span data-ttu-id="73092-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="73092-104">SYNTAX</span></span>

### <span data-ttu-id="73092-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="73092-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-KeyKind <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73092-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73092-106">ByResourceIdParameterSet</span></span>
```
New-AzCosmosDBAccountKey [-KeyKind <String>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73092-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73092-107">ByObjectParameterSet</span></span>
```
New-AzCosmosDBAccountKey [-KeyKind <String>] -InputObject <PSDatabaseAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73092-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="73092-108">DESCRIPTION</span></span>
<span data-ttu-id="73092-109">Hozzon létre egy új CosmosDB-fiókot az adott ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="73092-109">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="73092-110">Példák</span><span class="sxs-lookup"><span data-stu-id="73092-110">EXAMPLES</span></span>

### <span data-ttu-id="73092-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="73092-111">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBAccountKey -ResourceGroupName rg -Name dbname
```

<span data-ttu-id="73092-112">Új kulcsok jönnek létre a fióknév dbname a ResourceGroup RG-ban.</span><span class="sxs-lookup"><span data-stu-id="73092-112">New keys are generated for Account with account name dbname in ResourceGroup rg.</span></span>

## <span data-ttu-id="73092-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="73092-113">PARAMETERS</span></span>

### <span data-ttu-id="73092-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73092-114">-AsJob</span></span>
<span data-ttu-id="73092-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="73092-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="73092-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="73092-116">-Confirm</span></span>
<span data-ttu-id="73092-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="73092-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73092-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73092-118">-DefaultProfile</span></span>
<span data-ttu-id="73092-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73092-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73092-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73092-120">-InputObject</span></span>
<span data-ttu-id="73092-121">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="73092-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73092-122">-Kind</span><span class="sxs-lookup"><span data-stu-id="73092-122">-KeyKind</span></span>
<span data-ttu-id="73092-123">Az újragenerálni kívánt hozzáférési kulcs.</span><span class="sxs-lookup"><span data-stu-id="73092-123">The access key to regenerate.</span></span>
<span data-ttu-id="73092-124">Elfogadott értékek: elsődleges, primaryReadonly, másodlagos, secondaryReadonly</span><span class="sxs-lookup"><span data-stu-id="73092-124">Accepted values: primary, primaryReadonly, secondary, secondaryReadonly</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73092-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="73092-125">-Name</span></span>
<span data-ttu-id="73092-126">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="73092-126">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73092-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73092-127">-ResourceGroupName</span></span>
<span data-ttu-id="73092-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="73092-128">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73092-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73092-129">-ResourceId</span></span>
<span data-ttu-id="73092-130">Az erőforrás ResourceId.</span><span class="sxs-lookup"><span data-stu-id="73092-130">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73092-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73092-131">-WhatIf</span></span>
<span data-ttu-id="73092-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="73092-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73092-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="73092-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73092-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73092-134">CommonParameters</span></span>
<span data-ttu-id="73092-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="73092-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73092-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="73092-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73092-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="73092-137">INPUTS</span></span>

### <span data-ttu-id="73092-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="73092-138">None</span></span>

## <span data-ttu-id="73092-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73092-139">OUTPUTS</span></span>

### <span data-ttu-id="73092-140">System. Void</span><span class="sxs-lookup"><span data-stu-id="73092-140">System.Void</span></span>

## <span data-ttu-id="73092-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="73092-141">NOTES</span></span>

## <span data-ttu-id="73092-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73092-142">RELATED LINKS</span></span>
