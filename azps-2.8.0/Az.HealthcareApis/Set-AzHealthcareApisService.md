---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: 36632398d95acdd16d2a7b41c09bed7172391639
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666310"
---
# <span data-ttu-id="182c2-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="182c2-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="182c2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="182c2-102">SYNOPSIS</span></span>
<span data-ttu-id="182c2-103">Frissít egy meglévő healthcareApis-fhir szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="182c2-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="182c2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="182c2-104">SYNTAX</span></span>

### <span data-ttu-id="182c2-105">ServiceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="182c2-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-AccessPolicyObjectId <String[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="182c2-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="182c2-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-Authority <String>] [-Audience <String>]
 [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>]
 [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential]
 [-AccessPolicyObjectId <String[]>] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="182c2-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="182c2-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="182c2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="182c2-108">DESCRIPTION</span></span>
<span data-ttu-id="182c2-109">Frissít egy meglévő healthcareApis-fhir szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="182c2-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="182c2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="182c2-110">EXAMPLES</span></span>

### <span data-ttu-id="182c2-111">1. példa: frissíti a MyService nevű meglévő healthcareapis-szolgáltatást az erőforráscsoport MyResourceGroup a cosmosdb OfferThroughput = 500.</span><span class="sxs-lookup"><span data-stu-id="182c2-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

```powershell
PS C:\> Set-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -CosmosOfferThroughput 500

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 500
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

### <span data-ttu-id="182c2-112">2. példa: frissíti a MyService nevű meglévő healthcareapis-szolgáltatást az erőforráscsoport MyResourceGroup a cosmosdb OfferThroughput = 500.</span><span class="sxs-lookup"><span data-stu-id="182c2-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService"
PS C:\> Set-AzHealthcareApisService -ResourceId $ResourceId  -CosmosOfferThroughput 500

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 500
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

## <span data-ttu-id="182c2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="182c2-113">PARAMETERS</span></span>

### <span data-ttu-id="182c2-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="182c2-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="182c2-115">Az Access-házirend objektum-azonosítóinak listája.</span><span class="sxs-lookup"><span data-stu-id="182c2-115">List of Access Policy Object IDs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="182c2-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="182c2-116">-AllowCorsCredential</span></span>
<span data-ttu-id="182c2-117">HealthcareApis FhirService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="182c2-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="182c2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="182c2-118">-AsJob</span></span>
<span data-ttu-id="182c2-119">A parancsmagot feladatként futtathatja a háttérben.</span><span class="sxs-lookup"><span data-stu-id="182c2-119">Run cmdlet as a job in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="182c2-120">-Közönség</span><span class="sxs-lookup"><span data-stu-id="182c2-120">-Audience</span></span>
<span data-ttu-id="182c2-121">HealthcareApis FhirService közönségnek.</span><span class="sxs-lookup"><span data-stu-id="182c2-121">HealthcareApis FhirService Audience.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="182c2-122">-Authority (jogosultság)</span><span class="sxs-lookup"><span data-stu-id="182c2-122">-Authority</span></span>
<span data-ttu-id="182c2-123">HealthcareApis FhirService Authority.</span><span class="sxs-lookup"><span data-stu-id="182c2-123">HealthcareApis FhirService Authority.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="182c2-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="182c2-124">-CorsHeader</span></span>
<span data-ttu-id="182c2-125">A CORS fejlécének HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="182c2-125">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="182c2-126">Adja meg azokat a HTTP-fejléceket, amelyek a kérés során használhatók.</span><span class="sxs-lookup"><span data-stu-id="182c2-126">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="182c2-127">Használja a \* tetszőleges fejlécet.</span><span class="sxs-lookup"><span data-stu-id="182c2-127">Use \* for any header.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="182c2-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="182c2-128">-CorsMaxAge</span></span>
<span data-ttu-id="182c2-129">HealthcareApis Fhir szolgáltatás CORS Max Age.</span><span class="sxs-lookup"><span data-stu-id="182c2-129">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="182c2-130">Adja meg, hogy a kérésből mennyi ideig legyen gyorsítótárban lévő eredmény.</span><span class="sxs-lookup"><span data-stu-id="182c2-130">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="182c2-131">Példa: 600 10 percet jelent.</span><span class="sxs-lookup"><span data-stu-id="182c2-131">Example: 600 means 10 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="182c2-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="182c2-132">-CorsMethod</span></span>
<span data-ttu-id="182c2-133">HealthcareApis FhirService a CORS módszerek listáját.</span><span class="sxs-lookup"><span data-stu-id="182c2-133">HealthcareApis FhirService List of Cors Methods.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:
Accepted values: DELETE, GET, OPTIONS, PATCH, POST, PUT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="182c2-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="182c2-134">-CorsOrigin</span></span>
<span data-ttu-id="182c2-135">A CORS eredetének HealthcareApis FhirService listája.</span><span class="sxs-lookup"><span data-stu-id="182c2-135">HealthcareApis FhirService List of Cors Origins.</span></span> <span data-ttu-id="182c2-136">A HealthcareApis Fhir szolgáltatás CORS eredete.</span><span class="sxs-lookup"><span data-stu-id="182c2-136">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="182c2-137">Adja meg az API-t elérő származási webhelyek URL-címét, vagy használja a \*-ot bármely webhelyről való hozzáférés engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="182c2-137">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="182c2-138">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="182c2-138">-CosmosOfferThroughput</span></span>
<span data-ttu-id="182c2-139">HealthcareApis FhirService CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="182c2-139">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="182c2-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="182c2-140">-DefaultProfile</span></span>
<span data-ttu-id="182c2-141">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="182c2-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="182c2-142">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="182c2-142">-DisableCorsCredential</span></span>
<span data-ttu-id="182c2-143">A HealthcareApis FhirService CorsCredentials nem engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="182c2-143">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="182c2-144">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="182c2-144">-DisableSmartProxy</span></span>
<span data-ttu-id="182c2-145">HealthcareApis FhirService DisableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="182c2-145">HealthcareApis FhirService DisableSmartProxy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="182c2-146">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="182c2-146">-EnableSmartProxy</span></span>
<span data-ttu-id="182c2-147">HealthcareApis FhirService EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="182c2-147">HealthcareApis FhirService EnableSmartProxy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="182c2-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="182c2-148">-InputObject</span></span>
<span data-ttu-id="182c2-149">HealthcareApis fhir szolgáltatás vezetékes a Get-AzHealthcareApisFhirService.</span><span class="sxs-lookup"><span data-stu-id="182c2-149">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="182c2-150">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="182c2-150">-Name</span></span>
<span data-ttu-id="182c2-151">HealthcareApis szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="182c2-151">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="182c2-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="182c2-152">-ResourceGroupName</span></span>
<span data-ttu-id="182c2-153">Az HealthcareApis szolgáltatás-erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="182c2-153">HealthcareApis Service Resource Group Name.</span></span>

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

### <span data-ttu-id="182c2-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="182c2-154">-ResourceId</span></span>
<span data-ttu-id="182c2-155">HealthcareApis Fhir szolgáltatás ResourceId.</span><span class="sxs-lookup"><span data-stu-id="182c2-155">HealthcareApis Fhir Service ResourceId.</span></span>

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

### <span data-ttu-id="182c2-156">-Címke</span><span class="sxs-lookup"><span data-stu-id="182c2-156">-Tag</span></span>
<span data-ttu-id="182c2-157">HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="182c2-157">HealthcareApis Fhir Service Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="182c2-158">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="182c2-158">-Confirm</span></span>
<span data-ttu-id="182c2-159">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="182c2-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="182c2-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="182c2-160">-WhatIf</span></span>
<span data-ttu-id="182c2-161">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="182c2-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="182c2-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="182c2-162">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="182c2-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="182c2-163">CommonParameters</span></span>
<span data-ttu-id="182c2-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="182c2-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="182c2-165">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="182c2-165">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="182c2-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="182c2-166">INPUTS</span></span>

### <span data-ttu-id="182c2-167">System. String</span><span class="sxs-lookup"><span data-stu-id="182c2-167">System.String</span></span>

### <span data-ttu-id="182c2-168">Microsoft. Azure. Command. HealthcareApisService. models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="182c2-168">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="182c2-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="182c2-169">OUTPUTS</span></span>

### <span data-ttu-id="182c2-170">Microsoft. Azure. Command. HealthcareApisService. models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="182c2-170">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="182c2-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="182c2-171">NOTES</span></span>

## <span data-ttu-id="182c2-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="182c2-172">RELATED LINKS</span></span>
