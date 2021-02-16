---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/get-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
ms.openlocfilehash: 6d9c099457c25831d0ce97786b8d710cf4c0dc98
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167379"
---
# <span data-ttu-id="f3eb4-101">Get-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="f3eb4-101">Get-AzHealthcareApisService</span></span>

## <span data-ttu-id="f3eb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="f3eb4-103">Szolgáltatáspéldány metaadatainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="f3eb4-103">Get the metadata of a service instance.</span></span>

## <span data-ttu-id="f3eb4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f3eb4-104">SYNTAX</span></span>

### <span data-ttu-id="f3eb4-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f3eb4-105">ListParameterSet (Default)</span></span>
```
Get-AzHealthcareApisService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3eb4-106">ServiceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3eb4-106">ServiceNameParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3eb4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3eb4-107">ResourceIdParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3eb4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f3eb4-108">DESCRIPTION</span></span>
<span data-ttu-id="f3eb4-109">A megadott előfizetésen vagy erőforráscsoporton belül létrehozott egészségügyiApis-szolgáltatásfiókokat kap.</span><span class="sxs-lookup"><span data-stu-id="f3eb4-109">Gets existing healthcareApis fhir service accounts created within the specified subscription or a resource group.</span></span>

## <span data-ttu-id="f3eb4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f3eb4-110">EXAMPLES</span></span>

### <span data-ttu-id="f3eb4-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="f3eb4-111">Example 1</span></span>
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

### <span data-ttu-id="f3eb4-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="f3eb4-112">Example 2</span></span>

<span data-ttu-id="f3eb4-113">A megadott erőforráscsoport összes HealthcareApis szolgáltatásának metaadatait beveszi.</span><span class="sxs-lookup"><span data-stu-id="f3eb4-113">Gets the metadata for all HealthcareApis services in the provided Resource Group.</span></span>

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

### <span data-ttu-id="f3eb4-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="f3eb4-114">Example 3</span></span>

<span data-ttu-id="f3eb4-115">A HealthcareApis összes szolgáltatásának metaadatait beveszi az adott előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="f3eb4-115">Gets the metadata for all HealthcareApis services in the given subscription</span></span>

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

## <span data-ttu-id="f3eb4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3eb4-116">PARAMETERS</span></span>

### <span data-ttu-id="f3eb4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3eb4-117">-DefaultProfile</span></span>
<span data-ttu-id="f3eb4-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3eb4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3eb4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f3eb4-119">-Name</span></span>
<span data-ttu-id="f3eb4-120">HealthcareApis szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="f3eb4-120">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="f3eb4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3eb4-121">-ResourceGroupName</span></span>
<span data-ttu-id="f3eb4-122">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f3eb4-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="f3eb4-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3eb4-123">-ResourceId</span></span>
<span data-ttu-id="f3eb4-124">Erőforrás-azonosító neve.</span><span class="sxs-lookup"><span data-stu-id="f3eb4-124">Resource Id Name.</span></span>

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

### <span data-ttu-id="f3eb4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3eb4-125">CommonParameters</span></span>
<span data-ttu-id="f3eb4-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3eb4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3eb4-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3eb4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3eb4-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3eb4-128">INPUTS</span></span>

### <span data-ttu-id="f3eb4-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f3eb4-129">System.String</span></span>

## <span data-ttu-id="f3eb4-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3eb4-130">OUTPUTS</span></span>

### <span data-ttu-id="f3eb4-131">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="f3eb4-131">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="f3eb4-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f3eb4-132">NOTES</span></span>

## <span data-ttu-id="f3eb4-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3eb4-133">RELATED LINKS</span></span>
