---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
ms.openlocfilehash: b9e78e4ff9811f5ff52b64369fd546d5f5a8c474
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352001"
---
# <span data-ttu-id="557a0-101">Get-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="557a0-101">Get-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="557a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="557a0-102">SYNOPSIS</span></span>
<span data-ttu-id="557a0-103">Szerezze be a Keys{"ConnectionKeys", a "PrimaryReadOnly" vagy a "Keys"} billentyűparancsot az adott CossDB-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="557a0-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span></span> 

## <span data-ttu-id="557a0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="557a0-104">SYNTAX</span></span>

### <span data-ttu-id="557a0-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="557a0-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="557a0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="557a0-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="557a0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="557a0-107">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="557a0-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="557a0-108">DESCRIPTION</span></span>
<span data-ttu-id="557a0-109">A kapcsolatbillentyűk listájának lekérte.</span><span class="sxs-lookup"><span data-stu-id="557a0-109">Get the list of connection keys.</span></span>

## <span data-ttu-id="557a0-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="557a0-110">EXAMPLES</span></span>

### <span data-ttu-id="557a0-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="557a0-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzCosmosDBAccountKey -ResourceGroupName rg1 -Name dbname -Type "ReadOnlyKeys"

Name                           Value
----                           -----
PrimaryReadonlyMasterKey       qjw0ISW1WNN0BIVPeaI7Tm3H8uZ1h7ESQjxaUendxHmIUNQowVvcL84fTqeXoC2HFgyu8Zo1mCFEcg0jZJHPjA==
SecondaryReadonlyMasterKey     9YRcTABuOHcKyHAKf0lmCeHsrcXu02aeID1g3wjXjlX8SU4s2WNlEB5htJoy3xqxNDqIyGfnq3dblLbrZDbesg==
```

<span data-ttu-id="557a0-112">A 2010-es fiók kulcsait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="557a0-112">Lists the keys for CosmosDB Account.</span></span> <span data-ttu-id="557a0-113">A kulcstípus értéke a következő lehet: ConnectionStrings, Keys and ReadOnlyKeys.</span><span class="sxs-lookup"><span data-stu-id="557a0-113">The Key Type can be value from : ConnectionStrings, Keys and ReadOnlyKeys.</span></span> <span data-ttu-id="557a0-114">Az alapértelmezett érték a Kulcsok.</span><span class="sxs-lookup"><span data-stu-id="557a0-114">Default is Keys.</span></span>

## <span data-ttu-id="557a0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="557a0-115">PARAMETERS</span></span>

### <span data-ttu-id="557a0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="557a0-116">-DefaultProfile</span></span>
<span data-ttu-id="557a0-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="557a0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="557a0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="557a0-118">-InputObject</span></span>
<span data-ttu-id="557a0-119">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="557a0-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="557a0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="557a0-120">-Name</span></span>
<span data-ttu-id="557a0-121">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="557a0-121">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="557a0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="557a0-122">-ResourceGroupName</span></span>
<span data-ttu-id="557a0-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="557a0-123">Name of resource group.</span></span>

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

### <span data-ttu-id="557a0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="557a0-124">-ResourceId</span></span>
<span data-ttu-id="557a0-125">Az erőforrás Erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="557a0-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="557a0-126">-Type</span><span class="sxs-lookup"><span data-stu-id="557a0-126">-Type</span></span>
<span data-ttu-id="557a0-127">Érték: {ConnectionStrings, Keys, ReadOnlyKeys}.</span><span class="sxs-lookup"><span data-stu-id="557a0-127">Value from: {ConnectionStrings, Keys, ReadOnlyKeys}.</span></span>
<span data-ttu-id="557a0-128">Az alapértelmezett érték a Kulcsok.</span><span class="sxs-lookup"><span data-stu-id="557a0-128">Default is Keys.</span></span>

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

### <span data-ttu-id="557a0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="557a0-129">CommonParameters</span></span>
<span data-ttu-id="557a0-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="557a0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="557a0-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="557a0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="557a0-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="557a0-132">INPUTS</span></span>

### <span data-ttu-id="557a0-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="557a0-133">None</span></span>

## <span data-ttu-id="557a0-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="557a0-134">OUTPUTS</span></span>

### <span data-ttu-id="557a0-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="557a0-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span></span>

### <span data-ttu-id="557a0-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="557a0-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span></span>

### <span data-ttu-id="557a0-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span><span class="sxs-lookup"><span data-stu-id="557a0-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span></span>

## <span data-ttu-id="557a0-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="557a0-138">NOTES</span></span>

## <span data-ttu-id="557a0-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="557a0-139">RELATED LINKS</span></span>
