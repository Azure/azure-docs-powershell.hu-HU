---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbaccountregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
ms.openlocfilehash: 643cdbf8aa0aed98dba7497fa0107d8d81583bba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922033"
---
# <span data-ttu-id="0c6f1-101">Update-AzCosmosDBAccountRegion</span><span class="sxs-lookup"><span data-stu-id="0c6f1-101">Update-AzCosmosDBAccountRegion</span></span>

## <span data-ttu-id="0c6f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c6f1-102">SYNOPSIS</span></span>
<span data-ttu-id="0c6f1-103">Frissítheti a 2010-es fiók régióit.</span><span class="sxs-lookup"><span data-stu-id="0c6f1-103">Update Regions of a CosmosDB Account.</span></span>

## <span data-ttu-id="0c6f1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0c6f1-104">SYNTAX</span></span>

### <span data-ttu-id="0c6f1-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0c6f1-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountRegion -ResourceGroupName <String> -Name <String> [-Location <String[]>]
 [-LocationObject <PSLocation[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c6f1-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c6f1-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c6f1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c6f1-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>]
 -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c6f1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0c6f1-108">DESCRIPTION</span></span>
<span data-ttu-id="0c6f1-109">Frissítheti a 2010-es fiók régióit.</span><span class="sxs-lookup"><span data-stu-id="0c6f1-109">Update Regions of a CosmosDB Account.</span></span> <span data-ttu-id="0c6f1-110">A hely meg lehet adni PSLocation típusú objektumként vagy feladatátvételi prioritás szerint rendezett Helynév karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="0c6f1-110">Location can be provided either as an object of type PSLocation or as strings of Location Name ordered by failover priority.</span></span>
<span data-ttu-id="0c6f1-111">A LocationObject paraméter az új hozzáadható helyeknek megfelelő új LocationObjects által hozzáfűzett aktuális helyek listáját (feladatátvételi prioritásokat is beleértve) vár.</span><span class="sxs-lookup"><span data-stu-id="0c6f1-111">LocationObject parameter expects the list of current locations (failover prioritiies included) appended by the new LocationObjects corresponding to new locations to be added.</span></span>
<span data-ttu-id="0c6f1-112">A Hely paraméter az aktuális hely (feladatátvételi prioritás szerint rendezett) és az új helyek listáját várja.</span><span class="sxs-lookup"><span data-stu-id="0c6f1-112">Location parameter expects the list of current location(ordered by failover priority) and the new locations.</span></span> <span data-ttu-id="0c6f1-113">Felhívjuk a figyelmét arra, hogy csak a Régiók kiegészítését támogatjuk.</span><span class="sxs-lookup"><span data-stu-id="0c6f1-113">Please note, we only support Addition of Regions.</span></span> <span data-ttu-id="0c6f1-114">Adja meg a Location (Hely) vagy a LocationObject (Helyobjektum) lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="0c6f1-114">Please provide either Location or LocationObject.</span></span>

## <span data-ttu-id="0c6f1-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0c6f1-115">EXAMPLES</span></span>

### <span data-ttu-id="0c6f1-116">1. példa</span><span class="sxs-lookup"><span data-stu-id="0c6f1-116">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountRegion -ResourceGroupName rg1 -Name dbname -Location "location1, location2"

Kind                          : GlobalDocumentDB
ProvisioningState             : Succeeded
DocumentEndpoint              : https://dbname.documents.azure.com:443/
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : False
EnableAutomaticFailover       : False
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Fluent.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {dbname-location1}
ReadLocations                 : {dbname-location2}
FailoverPolicies              : {dbname-location1, dbname-location2}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
Location                      : location1
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/rg1/providers/Microsoft.DocumentDB/databaseAccounts/dbname
Name                          : dbname
Type                          : Microsoft.DocumentDB/databaseAccounts
```

## <span data-ttu-id="0c6f1-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c6f1-117">PARAMETERS</span></span>

### <span data-ttu-id="0c6f1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c6f1-118">-AsJob</span></span>
<span data-ttu-id="0c6f1-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0c6f1-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c6f1-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c6f1-120">-Confirm</span></span>
<span data-ttu-id="0c6f1-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0c6f1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c6f1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c6f1-122">-DefaultProfile</span></span>
<span data-ttu-id="0c6f1-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c6f1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c6f1-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c6f1-124">-InputObject</span></span>
<span data-ttu-id="0c6f1-125">Az erőforrás Erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="0c6f1-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="0c6f1-126">-Location</span><span class="sxs-lookup"><span data-stu-id="0c6f1-126">-Location</span></span>
<span data-ttu-id="0c6f1-127">A hozzáadható hely neve.</span><span class="sxs-lookup"><span data-stu-id="0c6f1-127">Name of the location to be added.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6f1-128">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="0c6f1-128">-LocationObject</span></span>
<span data-ttu-id="0c6f1-129">Vegyen fel egy helyet aTans DB adatbázisfiókba.</span><span class="sxs-lookup"><span data-stu-id="0c6f1-129">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="0c6f1-130">PSLocation-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="0c6f1-130">Array of PSLocation objects.</span></span>

```yaml
Type: PSLocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6f1-131">-Name</span><span class="sxs-lookup"><span data-stu-id="0c6f1-131">-Name</span></span>
<span data-ttu-id="0c6f1-132">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="0c6f1-132">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0c6f1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c6f1-133">-ResourceGroupName</span></span>
<span data-ttu-id="0c6f1-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0c6f1-134">Name of resource group.</span></span>

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

### <span data-ttu-id="0c6f1-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c6f1-135">-ResourceId</span></span>
<span data-ttu-id="0c6f1-136">Az erőforrás Erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="0c6f1-136">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="0c6f1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c6f1-137">-WhatIf</span></span>
<span data-ttu-id="0c6f1-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0c6f1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c6f1-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0c6f1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c6f1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c6f1-140">CommonParameters</span></span>
<span data-ttu-id="0c6f1-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c6f1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c6f1-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c6f1-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c6f1-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c6f1-143">INPUTS</span></span>

### <span data-ttu-id="0c6f1-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="0c6f1-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="0c6f1-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c6f1-145">OUTPUTS</span></span>

### <span data-ttu-id="0c6f1-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="0c6f1-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="0c6f1-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0c6f1-147">NOTES</span></span>

## <span data-ttu-id="0c6f1-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c6f1-148">RELATED LINKS</span></span>
