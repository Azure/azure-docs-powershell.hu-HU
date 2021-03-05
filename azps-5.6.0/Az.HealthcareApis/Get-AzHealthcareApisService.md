---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/powershell/module/az.healthcareapis/get-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
ms.openlocfilehash: ca41e87c0f17ef62033cab0966296a307f90a457
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013190"
---
# <span data-ttu-id="507a3-101">Get-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="507a3-101">Get-AzHealthcareApisService</span></span>

## <span data-ttu-id="507a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="507a3-102">SYNOPSIS</span></span>
<span data-ttu-id="507a3-103">Szolgáltatáspéldány metaadatainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="507a3-103">Get the metadata of a service instance.</span></span>

## <span data-ttu-id="507a3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="507a3-104">SYNTAX</span></span>

### <span data-ttu-id="507a3-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="507a3-105">ListParameterSet (Default)</span></span>
```
Get-AzHealthcareApisService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="507a3-106">ServiceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="507a3-106">ServiceNameParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="507a3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="507a3-107">ResourceIdParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="507a3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="507a3-108">DESCRIPTION</span></span>
<span data-ttu-id="507a3-109">Beszerzi a meglévő egészségügyiApis-szolgáltatásfiókokat, amelyek a megadott előfizetésen vagy erőforráscsoporton belül jött létre.</span><span class="sxs-lookup"><span data-stu-id="507a3-109">Gets existing healthcareApis fhir service accounts created within the specified subscription or a resource group.</span></span>

## <span data-ttu-id="507a3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="507a3-110">EXAMPLES</span></span>

### <span data-ttu-id="507a3-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="507a3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -Name "MyService" -ResourceGroupName "MyResourceGroup"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  :
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="507a3-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="507a3-112">Example 2</span></span>

<span data-ttu-id="507a3-113">A megadott erőforráscsoport összes HealthcareApis szolgáltatásának metaadatait beveszi.</span><span class="sxs-lookup"><span data-stu-id="507a3-113">Gets the metadata for all HealthcareApis services in the provided Resource Group.</span></span>

```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName "MyResourceGroup"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db48
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  :
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  :
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService1
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService1
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="507a3-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="507a3-114">Example 3</span></span>

<span data-ttu-id="507a3-115">A HealthcareApis összes szolgáltatásának metaadatait beveszi az adott előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="507a3-115">Gets the metadata for all HealthcareApis services in the given subscription</span></span>

```powershell
PS C:\> Get-AzHealthcareApisService

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db48
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  :
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  :
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService1
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService1
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

## <span data-ttu-id="507a3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="507a3-116">PARAMETERS</span></span>

### <span data-ttu-id="507a3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="507a3-117">-DefaultProfile</span></span>
<span data-ttu-id="507a3-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="507a3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="507a3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="507a3-119">-Name</span></span>
<span data-ttu-id="507a3-120">HealthcareApis szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="507a3-120">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases: HealthcareApisName, FhirServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507a3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="507a3-121">-ResourceGroupName</span></span>
<span data-ttu-id="507a3-122">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="507a3-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507a3-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="507a3-123">-ResourceId</span></span>
<span data-ttu-id="507a3-124">Erőforrás-azonosító neve.</span><span class="sxs-lookup"><span data-stu-id="507a3-124">Resource Id Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="507a3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="507a3-125">CommonParameters</span></span>
<span data-ttu-id="507a3-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="507a3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="507a3-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="507a3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="507a3-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="507a3-128">INPUTS</span></span>

### <span data-ttu-id="507a3-129">System.String</span><span class="sxs-lookup"><span data-stu-id="507a3-129">System.String</span></span>

## <span data-ttu-id="507a3-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="507a3-130">OUTPUTS</span></span>

### <span data-ttu-id="507a3-131">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="507a3-131">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="507a3-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="507a3-132">NOTES</span></span>

## <span data-ttu-id="507a3-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="507a3-133">RELATED LINKS</span></span>
