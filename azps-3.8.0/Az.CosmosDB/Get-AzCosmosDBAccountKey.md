---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
ms.openlocfilehash: 6c0fb28010aff759c406ddd04db281dc05ce1f0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845645"
---
# <span data-ttu-id="55974-101">Get-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="55974-101">Get-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="55974-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="55974-102">SYNOPSIS</span></span>
<span data-ttu-id="55974-103">A "ConnectionKeys", "PrimaryReadOnly" vagy a "kulcsok"} beolvasása a megadott CosmosDB-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="55974-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span></span> 

## <span data-ttu-id="55974-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="55974-104">SYNTAX</span></span>

### <span data-ttu-id="55974-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="55974-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55974-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55974-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="55974-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55974-107">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55974-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="55974-108">DESCRIPTION</span></span>
<span data-ttu-id="55974-109">A kapcsolati kulcsok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="55974-109">Get the list of connection keys.</span></span>

## <span data-ttu-id="55974-110">Példák</span><span class="sxs-lookup"><span data-stu-id="55974-110">EXAMPLES</span></span>

### <span data-ttu-id="55974-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="55974-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzCosmosDBAccountKey -ResourceGroupName rg1 -Name dbname -Type "ReadOnlyKeys"

Name                           Value
----                           -----
PrimaryReadonlyMasterKey       qjw0ISW1WNN0BIVPeaI7Tm3H8uZ1h7ESQjxaUendxHmIUNQowVvcL84fTqeXoC2HFgyu8Zo1mCFEcg0jZJHPjA==
SecondaryReadonlyMasterKey     9YRcTABuOHcKyHAKf0lmCeHsrcXu02aeID1g3wjXjlX8SU4s2WNlEB5htJoy3xqxNDqIyGfnq3dblLbrZDbesg==
```

<span data-ttu-id="55974-112">Az CosmosDB-fiók kulcsait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="55974-112">Lists the keys for CosmosDB Account.</span></span> <span data-ttu-id="55974-113">A kulcs típusa: ConnectionStrings, billentyűk és ReadOnlyKeys.</span><span class="sxs-lookup"><span data-stu-id="55974-113">The Key Type can be value from : ConnectionStrings, Keys and ReadOnlyKeys.</span></span> <span data-ttu-id="55974-114">Az alapértelmezett érték a kulcsok.</span><span class="sxs-lookup"><span data-stu-id="55974-114">Default is Keys.</span></span>

## <span data-ttu-id="55974-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="55974-115">PARAMETERS</span></span>

### <span data-ttu-id="55974-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55974-116">-DefaultProfile</span></span>
<span data-ttu-id="55974-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="55974-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55974-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55974-118">-InputObject</span></span>
<span data-ttu-id="55974-119">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="55974-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="55974-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="55974-120">-Name</span></span>
<span data-ttu-id="55974-121">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="55974-121">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="55974-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55974-122">-ResourceGroupName</span></span>
<span data-ttu-id="55974-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="55974-123">Name of resource group.</span></span>

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

### <span data-ttu-id="55974-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55974-124">-ResourceId</span></span>
<span data-ttu-id="55974-125">Az erőforrás ResourceId.</span><span class="sxs-lookup"><span data-stu-id="55974-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="55974-126">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="55974-126">-Type</span></span>
<span data-ttu-id="55974-127">Az érték: {ConnectionStrings, Keys, ReadOnlyKeys}.</span><span class="sxs-lookup"><span data-stu-id="55974-127">Value from: {ConnectionStrings, Keys, ReadOnlyKeys}.</span></span>
<span data-ttu-id="55974-128">Az alapértelmezett érték a kulcsok.</span><span class="sxs-lookup"><span data-stu-id="55974-128">Default is Keys.</span></span>

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

### <span data-ttu-id="55974-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55974-129">CommonParameters</span></span>
<span data-ttu-id="55974-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="55974-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55974-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="55974-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55974-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="55974-132">INPUTS</span></span>

### <span data-ttu-id="55974-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="55974-133">None</span></span>

## <span data-ttu-id="55974-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55974-134">OUTPUTS</span></span>

### <span data-ttu-id="55974-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="55974-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span></span>

### <span data-ttu-id="55974-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="55974-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span></span>

### <span data-ttu-id="55974-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span><span class="sxs-lookup"><span data-stu-id="55974-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span></span>

## <span data-ttu-id="55974-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="55974-138">NOTES</span></span>

## <span data-ttu-id="55974-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55974-139">RELATED LINKS</span></span>
