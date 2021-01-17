---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
ms.openlocfilehash: 5c6dffe65022fa0282ab53bb04efe651ec123c2d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331625"
---
# <span data-ttu-id="096aa-101">Get-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="096aa-101">Get-AzCosmosDBAccount</span></span>

## <span data-ttu-id="096aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="096aa-102">SYNOPSIS</span></span>
<span data-ttu-id="096aa-103">Szerezze be a CossDB-fiókot.</span><span class="sxs-lookup"><span data-stu-id="096aa-103">Get CosmosDB Account.</span></span>

## <span data-ttu-id="096aa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="096aa-104">SYNTAX</span></span>

### <span data-ttu-id="096aa-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="096aa-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="096aa-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="096aa-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="096aa-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="096aa-107">DESCRIPTION</span></span>
<span data-ttu-id="096aa-108">A **Get-AzCosmosDBAccount** parancsmag lekérte egy adott ResourceGroupName-fiók összes meglévő, ABB-fiókjainak listáját, és egy adott ResourceGroupName és AccountName fiókhoz egyetlen KülönBB-fiókot kap.</span><span class="sxs-lookup"><span data-stu-id="096aa-108">The **Get-AzCosmosDBAccount** cmdlet gets the list of all existing CosmosDB accounts for a given ResourceGroupName and gets a single CosmosDB account for a given ResourceGroupName and AccountName.</span></span>

## <span data-ttu-id="096aa-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="096aa-109">EXAMPLES</span></span>

### <span data-ttu-id="096aa-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="096aa-110">Example 1</span></span>
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

<span data-ttu-id="096aa-111">Szerezze be a CossDB adatbázisfiókot azAccountName nevű névvel az ResourceGroup resourceGroupName erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="096aa-111">Get CosmosDB database account with name databaseAccountName in ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="096aa-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="096aa-112">PARAMETERS</span></span>

### <span data-ttu-id="096aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="096aa-113">-DefaultProfile</span></span>
<span data-ttu-id="096aa-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="096aa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="096aa-115">-Name</span><span class="sxs-lookup"><span data-stu-id="096aa-115">-Name</span></span>
<span data-ttu-id="096aa-116">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="096aa-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="096aa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="096aa-117">-ResourceGroupName</span></span>
<span data-ttu-id="096aa-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="096aa-118">Name of resource group.</span></span>

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

### <span data-ttu-id="096aa-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="096aa-119">-ResourceId</span></span>
<span data-ttu-id="096aa-120">Az erőforrás Erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="096aa-120">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="096aa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="096aa-121">CommonParameters</span></span>
<span data-ttu-id="096aa-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="096aa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="096aa-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="096aa-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="096aa-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="096aa-124">INPUTS</span></span>

### <span data-ttu-id="096aa-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="096aa-125">None</span></span>

## <span data-ttu-id="096aa-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="096aa-126">OUTPUTS</span></span>

### <span data-ttu-id="096aa-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="096aa-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="096aa-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="096aa-128">NOTES</span></span>

## <span data-ttu-id="096aa-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="096aa-129">RELATED LINKS</span></span>
