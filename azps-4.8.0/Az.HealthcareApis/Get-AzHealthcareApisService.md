---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/get-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
ms.openlocfilehash: d1a6edc3365631f93d2bc3b7a0e153ec360c2611
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183378"
---
# <span data-ttu-id="6550f-101">Get-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="6550f-101">Get-AzHealthcareApisService</span></span>

## <span data-ttu-id="6550f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6550f-102">SYNOPSIS</span></span>
<span data-ttu-id="6550f-103">Letölthet egy szolgáltatási példány metaadatait.</span><span class="sxs-lookup"><span data-stu-id="6550f-103">Get the metadata of a service instance.</span></span>

## <span data-ttu-id="6550f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6550f-104">SYNTAX</span></span>

### <span data-ttu-id="6550f-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6550f-105">ListParameterSet (Default)</span></span>
```
Get-AzHealthcareApisService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6550f-106">ServiceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6550f-106">ServiceNameParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6550f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6550f-107">ResourceIdParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6550f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6550f-108">DESCRIPTION</span></span>
<span data-ttu-id="6550f-109">A megadott előfizetésben vagy erőforrás-csoportban létrehozott meglévő healthcareApis-fhir kapja.</span><span class="sxs-lookup"><span data-stu-id="6550f-109">Gets existing healthcareApis fhir service accounts created within the specified subscription or a resource group.</span></span>

## <span data-ttu-id="6550f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6550f-110">EXAMPLES</span></span>

### <span data-ttu-id="6550f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6550f-111">Example 1</span></span>
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

### <span data-ttu-id="6550f-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="6550f-112">Example 2</span></span>

<span data-ttu-id="6550f-113">A megadott erőforráscsoport metaadatait kapja meg a HealthcareApis-szolgáltatásokhoz.</span><span class="sxs-lookup"><span data-stu-id="6550f-113">Gets the metadata for all HealthcareApis services in the provided Resource Group.</span></span>

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

### <span data-ttu-id="6550f-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="6550f-114">Example 3</span></span>

<span data-ttu-id="6550f-115">A megadott előfizetéshez tartozó összes HealthcareApis szolgáltatás metaadatait kapja</span><span class="sxs-lookup"><span data-stu-id="6550f-115">Gets the metadata for all HealthcareApis services in the given subscription</span></span>

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

## <span data-ttu-id="6550f-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6550f-116">PARAMETERS</span></span>

### <span data-ttu-id="6550f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6550f-117">-DefaultProfile</span></span>
<span data-ttu-id="6550f-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6550f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6550f-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6550f-119">-Name</span></span>
<span data-ttu-id="6550f-120">HealthcareApis szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="6550f-120">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="6550f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6550f-121">-ResourceGroupName</span></span>
<span data-ttu-id="6550f-122">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="6550f-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="6550f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6550f-123">-ResourceId</span></span>
<span data-ttu-id="6550f-124">Erőforrás-azonosító neve</span><span class="sxs-lookup"><span data-stu-id="6550f-124">Resource Id Name.</span></span>

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

### <span data-ttu-id="6550f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6550f-125">CommonParameters</span></span>
<span data-ttu-id="6550f-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6550f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6550f-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6550f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6550f-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6550f-128">INPUTS</span></span>

### <span data-ttu-id="6550f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6550f-129">System.String</span></span>

## <span data-ttu-id="6550f-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6550f-130">OUTPUTS</span></span>

### <span data-ttu-id="6550f-131">Microsoft. Azure. Command. HealthcareApisService. models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="6550f-131">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="6550f-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6550f-132">NOTES</span></span>

## <span data-ttu-id="6550f-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6550f-133">RELATED LINKS</span></span>
