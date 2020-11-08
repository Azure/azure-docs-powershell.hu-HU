---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
ms.openlocfilehash: 5c6dffe65022fa0282ab53bb04efe651ec123c2d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182879"
---
# <span data-ttu-id="e14bc-101">Get-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="e14bc-101">Get-AzCosmosDBAccount</span></span>

## <span data-ttu-id="e14bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e14bc-102">SYNOPSIS</span></span>
<span data-ttu-id="e14bc-103">CosmosDB-fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="e14bc-103">Get CosmosDB Account.</span></span>

## <span data-ttu-id="e14bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e14bc-104">SYNTAX</span></span>

### <span data-ttu-id="e14bc-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e14bc-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e14bc-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e14bc-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e14bc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e14bc-107">DESCRIPTION</span></span>
<span data-ttu-id="e14bc-108">A **Get-AzCosmosDBAccount parancsmag beolvassa** az adott ResourceGroupName tartozó összes létező CosmosDB-fiókot, és egyetlen CosmosDB-fiókot kap egy adott ResourceGroupName és accountname.</span><span class="sxs-lookup"><span data-stu-id="e14bc-108">The **Get-AzCosmosDBAccount** cmdlet gets the list of all existing CosmosDB accounts for a given ResourceGroupName and gets a single CosmosDB account for a given ResourceGroupName and AccountName.</span></span>

## <span data-ttu-id="e14bc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e14bc-109">EXAMPLES</span></span>

### <span data-ttu-id="e14bc-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e14bc-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBAccount -ResourceGroupName {resourceGroupName} -Name {databaseAccountName}


Id                            : /subscriptions/{subscriptionid}/resourceGroups/{resourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{databaseAccountName}
Name                          : {databaseAccountName}
FailoverPolicies              : {databaseAccountName-region1}
ReadLocations                 : {databaseAccountName-region1}
WriteLocations                : {databaseAccountName-region1}
Capabilities                  : {}
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Models.ConsistencyPolicy
EnableAutomaticFailover       : False
IsVirtualNetworkFilterEnabled : False
IpRangeFilter                 :
DatabaseAccountOfferType      : Standard
DocumentEndpoint              : https://databaseAccountName.documents.azure.com:443/
ProvisioningState             : Succeeded
Kind                          : GlobalDocumentDB
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
```

<span data-ttu-id="e14bc-111">Szerezzen be CosmosDB-adatbázis-fiókot a databaseAccountName nevű ResourceGroup resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="e14bc-111">Get CosmosDB database account with name databaseAccountName in ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="e14bc-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e14bc-112">PARAMETERS</span></span>

### <span data-ttu-id="e14bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e14bc-113">-DefaultProfile</span></span>
<span data-ttu-id="e14bc-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e14bc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e14bc-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e14bc-115">-Name</span></span>
<span data-ttu-id="e14bc-116">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="e14bc-116">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e14bc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e14bc-117">-ResourceGroupName</span></span>
<span data-ttu-id="e14bc-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e14bc-118">Name of resource group.</span></span>

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

### <span data-ttu-id="e14bc-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e14bc-119">-ResourceId</span></span>
<span data-ttu-id="e14bc-120">Az erőforrás ResourceId.</span><span class="sxs-lookup"><span data-stu-id="e14bc-120">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="e14bc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e14bc-121">CommonParameters</span></span>
<span data-ttu-id="e14bc-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e14bc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e14bc-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e14bc-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e14bc-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e14bc-124">INPUTS</span></span>

### <span data-ttu-id="e14bc-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="e14bc-125">None</span></span>

## <span data-ttu-id="e14bc-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e14bc-126">OUTPUTS</span></span>

### <span data-ttu-id="e14bc-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e14bc-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e14bc-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e14bc-128">NOTES</span></span>

## <span data-ttu-id="e14bc-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e14bc-129">RELATED LINKS</span></span>
