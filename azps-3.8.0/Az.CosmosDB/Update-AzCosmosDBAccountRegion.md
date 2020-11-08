---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
ms.openlocfilehash: dfc27ebad517a37fc2f78e99473d72fce568b56b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010546"
---
# <span data-ttu-id="2a966-101">Update-AzCosmosDBAccountRegion</span><span class="sxs-lookup"><span data-stu-id="2a966-101">Update-AzCosmosDBAccountRegion</span></span>

## <span data-ttu-id="2a966-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2a966-102">SYNOPSIS</span></span>
<span data-ttu-id="2a966-103">CosmosDB-fiók régióinak frissítése</span><span class="sxs-lookup"><span data-stu-id="2a966-103">Update Regions of a CosmosDB Account.</span></span>

## <span data-ttu-id="2a966-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2a966-104">SYNTAX</span></span>

### <span data-ttu-id="2a966-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2a966-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountRegion -ResourceGroupName <String> -Name <String> [-Location <String[]>]
 [-LocationObject <PSLocation[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a966-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a966-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a966-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a966-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>]
 -InputObject <PSDatabaseAccount> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a966-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2a966-108">DESCRIPTION</span></span>
<span data-ttu-id="2a966-109">CosmosDB-fiók régióinak frissítése</span><span class="sxs-lookup"><span data-stu-id="2a966-109">Update Regions of a CosmosDB Account.</span></span> <span data-ttu-id="2a966-110">A hely megadható objektumként a PSLocation típusa vagy a feladatátvételi prioritás által rendelt hely neve karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="2a966-110">Location can be provided either as an object of type PSLocation or as strings of Location Name ordered by failover priority.</span></span>
<span data-ttu-id="2a966-111">A LocationObject paraméter elvárja az új helyeknek megfelelő új LocationObjects (a feladatátvételi prioritiies is) az aktuális helyek listáját.</span><span class="sxs-lookup"><span data-stu-id="2a966-111">LocationObject parameter expects the list of current locations (failover prioritiies included) appended by the new LocationObjects corresponding to new locations to be added.</span></span>
<span data-ttu-id="2a966-112">A hely paraméter a jelenlegi hely (a feladatátvételi prioritás szerint rendezett) és az új helyek listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="2a966-112">Location parameter expects the list of current location(ordered by failover priority) and the new locations.</span></span> <span data-ttu-id="2a966-113">Felhívjuk a figyelmét arra, hogy csak a régiók hozzáadását támogatjuk.</span><span class="sxs-lookup"><span data-stu-id="2a966-113">Please note, we only support Addition of Regions.</span></span> <span data-ttu-id="2a966-114">Adjon meg egy helyet vagy egy LocationObject.</span><span class="sxs-lookup"><span data-stu-id="2a966-114">Please provide either Location or LocationObject.</span></span>

## <span data-ttu-id="2a966-115">Példák</span><span class="sxs-lookup"><span data-stu-id="2a966-115">EXAMPLES</span></span>

### <span data-ttu-id="2a966-116">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2a966-116">Example 1</span></span>
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

## <span data-ttu-id="2a966-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2a966-117">PARAMETERS</span></span>

### <span data-ttu-id="2a966-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a966-118">-AsJob</span></span>
<span data-ttu-id="2a966-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2a966-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a966-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2a966-120">-Confirm</span></span>
<span data-ttu-id="2a966-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2a966-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a966-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a966-122">-DefaultProfile</span></span>
<span data-ttu-id="2a966-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a966-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a966-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a966-124">-InputObject</span></span>
<span data-ttu-id="2a966-125">Az erőforrás ResourceId.</span><span class="sxs-lookup"><span data-stu-id="2a966-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="2a966-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="2a966-126">-Location</span></span>
<span data-ttu-id="2a966-127">A hozzáadni kívánt hely neve.</span><span class="sxs-lookup"><span data-stu-id="2a966-127">Name of the location to be added.</span></span>

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

### <span data-ttu-id="2a966-128">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="2a966-128">-LocationObject</span></span>
<span data-ttu-id="2a966-129">Adjon meg egy helyet a Cosmos DB adatbázis-fiókjához.</span><span class="sxs-lookup"><span data-stu-id="2a966-129">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="2a966-130">PSLocation-objektumok tömbje</span><span class="sxs-lookup"><span data-stu-id="2a966-130">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="2a966-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2a966-131">-Name</span></span>
<span data-ttu-id="2a966-132">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="2a966-132">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2a966-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a966-133">-ResourceGroupName</span></span>
<span data-ttu-id="2a966-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2a966-134">Name of resource group.</span></span>

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

### <span data-ttu-id="2a966-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a966-135">-ResourceId</span></span>
<span data-ttu-id="2a966-136">Az erőforrás ResourceId.</span><span class="sxs-lookup"><span data-stu-id="2a966-136">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="2a966-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a966-137">-WhatIf</span></span>
<span data-ttu-id="2a966-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2a966-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a966-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2a966-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a966-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a966-140">CommonParameters</span></span>
<span data-ttu-id="2a966-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2a966-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a966-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2a966-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a966-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a966-143">INPUTS</span></span>

### <span data-ttu-id="2a966-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="2a966-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="2a966-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a966-145">OUTPUTS</span></span>

### <span data-ttu-id="2a966-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="2a966-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="2a966-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2a966-147">NOTES</span></span>

## <span data-ttu-id="2a966-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a966-148">RELATED LINKS</span></span>
