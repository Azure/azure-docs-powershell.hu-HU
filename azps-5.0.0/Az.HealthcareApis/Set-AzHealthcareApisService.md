---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: a944982688dac8f9a28c10b3d26e71a8331451ad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187374"
---
# <span data-ttu-id="17baf-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="17baf-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="17baf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="17baf-102">SYNOPSIS</span></span>
<span data-ttu-id="17baf-103">Frissít egy meglévő healthcareApis-fhir szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="17baf-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="17baf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="17baf-104">SYNTAX</span></span>

### <span data-ttu-id="17baf-105">ServiceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="17baf-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>]
 [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17baf-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="17baf-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-Authority <String>] [-Audience <String>]
 [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>]
 [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential]
 [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>] [-EnableManagedIdentity]
 [-DisableManagedIdentity] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17baf-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17baf-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17baf-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="17baf-108">DESCRIPTION</span></span>
<span data-ttu-id="17baf-109">Frissít egy meglévő healthcareApis-fhir szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="17baf-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="17baf-110">Példák</span><span class="sxs-lookup"><span data-stu-id="17baf-110">EXAMPLES</span></span>

### <span data-ttu-id="17baf-111">1. példa: frissíti a MyService nevű meglévő healthcareapis-szolgáltatást az erőforráscsoport MyResourceGroup a cosmosdb OfferThroughput = 500.</span><span class="sxs-lookup"><span data-stu-id="17baf-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

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

### <span data-ttu-id="17baf-112">2. példa: frissíti a MyService nevű meglévő healthcareapis-szolgáltatást az erőforráscsoport MyResourceGroup a cosmosdb OfferThroughput = 500.</span><span class="sxs-lookup"><span data-stu-id="17baf-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

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

## <span data-ttu-id="17baf-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="17baf-113">PARAMETERS</span></span>

### <span data-ttu-id="17baf-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="17baf-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="17baf-115">Az Access-házirend objektum-azonosítóinak listája.</span><span class="sxs-lookup"><span data-stu-id="17baf-115">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="17baf-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="17baf-116">-AllowCorsCredential</span></span>
<span data-ttu-id="17baf-117">HealthcareApis FhirService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="17baf-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

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

### <span data-ttu-id="17baf-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17baf-118">-AsJob</span></span>
<span data-ttu-id="17baf-119">A parancsmagot feladatként futtathatja a háttérben.</span><span class="sxs-lookup"><span data-stu-id="17baf-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="17baf-120">-Közönség</span><span class="sxs-lookup"><span data-stu-id="17baf-120">-Audience</span></span>
<span data-ttu-id="17baf-121">HealthcareApis FhirService közönségnek.</span><span class="sxs-lookup"><span data-stu-id="17baf-121">HealthcareApis FhirService Audience.</span></span>

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

### <span data-ttu-id="17baf-122">-Authority (jogosultság)</span><span class="sxs-lookup"><span data-stu-id="17baf-122">-Authority</span></span>
<span data-ttu-id="17baf-123">HealthcareApis FhirService Authority.</span><span class="sxs-lookup"><span data-stu-id="17baf-123">HealthcareApis FhirService Authority.</span></span>

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

### <span data-ttu-id="17baf-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="17baf-124">-CorsHeader</span></span>
<span data-ttu-id="17baf-125">A CORS fejlécének HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="17baf-125">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="17baf-126">Adja meg azokat a HTTP-fejléceket, amelyek a kérés során használhatók.</span><span class="sxs-lookup"><span data-stu-id="17baf-126">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="17baf-127">Használja a \* tetszőleges fejlécet.</span><span class="sxs-lookup"><span data-stu-id="17baf-127">Use \* for any header.</span></span>

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

### <span data-ttu-id="17baf-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="17baf-128">-CorsMaxAge</span></span>
<span data-ttu-id="17baf-129">HealthcareApis Fhir szolgáltatás CORS Max Age.</span><span class="sxs-lookup"><span data-stu-id="17baf-129">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="17baf-130">Adja meg, hogy a kérésből mennyi ideig legyen gyorsítótárban lévő eredmény.</span><span class="sxs-lookup"><span data-stu-id="17baf-130">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="17baf-131">Példa: 600 10 percet jelent.</span><span class="sxs-lookup"><span data-stu-id="17baf-131">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="17baf-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="17baf-132">-CorsMethod</span></span>
<span data-ttu-id="17baf-133">HealthcareApis FhirService a CORS módszerek listáját.</span><span class="sxs-lookup"><span data-stu-id="17baf-133">HealthcareApis FhirService List of Cors Methods.</span></span>

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

### <span data-ttu-id="17baf-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="17baf-134">-CorsOrigin</span></span>
<span data-ttu-id="17baf-135">A CORS eredetének HealthcareApis FhirService listája.</span><span class="sxs-lookup"><span data-stu-id="17baf-135">HealthcareApis FhirService List of Cors Origins.</span></span> <span data-ttu-id="17baf-136">A HealthcareApis Fhir szolgáltatás CORS eredete.</span><span class="sxs-lookup"><span data-stu-id="17baf-136">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="17baf-137">Adja meg az API-t elérő származási webhelyek URL-címét, vagy használja a \*-ot bármely webhelyről való hozzáférés engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="17baf-137">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

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

### <span data-ttu-id="17baf-138">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="17baf-138">-CosmosOfferThroughput</span></span>
<span data-ttu-id="17baf-139">HealthcareApis FhirService CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="17baf-139">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="17baf-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17baf-140">-DefaultProfile</span></span>
<span data-ttu-id="17baf-141">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="17baf-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17baf-142">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="17baf-142">-DisableCorsCredential</span></span>
<span data-ttu-id="17baf-143">A HealthcareApis FhirService CorsCredentials nem engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="17baf-143">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

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

### <span data-ttu-id="17baf-144">-DisableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="17baf-144">-DisableManagedIdentity</span></span>
<span data-ttu-id="17baf-145">A felügyelt identitás letiltása</span><span class="sxs-lookup"><span data-stu-id="17baf-145">Disable Managed Identity.</span></span>

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

### <span data-ttu-id="17baf-146">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="17baf-146">-DisableSmartProxy</span></span>
<span data-ttu-id="17baf-147">HealthcareApis FhirService DisableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="17baf-147">HealthcareApis FhirService DisableSmartProxy.</span></span>

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

### <span data-ttu-id="17baf-148">-EnableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="17baf-148">-EnableManagedIdentity</span></span>
<span data-ttu-id="17baf-149">Felügyelt identitás engedélyezése</span><span class="sxs-lookup"><span data-stu-id="17baf-149">Enable Managed Identity.</span></span>

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

### <span data-ttu-id="17baf-150">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="17baf-150">-EnableSmartProxy</span></span>
<span data-ttu-id="17baf-151">HealthcareApis FhirService EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="17baf-151">HealthcareApis FhirService EnableSmartProxy.</span></span>

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

### <span data-ttu-id="17baf-152">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="17baf-152">-ExportStorageAccountName</span></span>
<span data-ttu-id="17baf-153">A HealthcareApis Fhir-szolgáltatása exportálja a tárolási fiók nevét.</span><span class="sxs-lookup"><span data-stu-id="17baf-153">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="17baf-154">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17baf-154">-InputObject</span></span>
<span data-ttu-id="17baf-155">HealthcareApis fhir szolgáltatás vezetékes a Get-AzHealthcareApisFhirService.</span><span class="sxs-lookup"><span data-stu-id="17baf-155">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

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

### <span data-ttu-id="17baf-156">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="17baf-156">-Name</span></span>
<span data-ttu-id="17baf-157">HealthcareApis szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="17baf-157">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="17baf-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17baf-158">-ResourceGroupName</span></span>
<span data-ttu-id="17baf-159">Az HealthcareApis szolgáltatás-erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="17baf-159">HealthcareApis Service Resource Group Name.</span></span>

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

### <span data-ttu-id="17baf-160">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17baf-160">-ResourceId</span></span>
<span data-ttu-id="17baf-161">HealthcareApis Fhir szolgáltatás ResourceId.</span><span class="sxs-lookup"><span data-stu-id="17baf-161">HealthcareApis Fhir Service ResourceId.</span></span>

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

### <span data-ttu-id="17baf-162">-Címke</span><span class="sxs-lookup"><span data-stu-id="17baf-162">-Tag</span></span>
<span data-ttu-id="17baf-163">HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="17baf-163">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="17baf-164">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="17baf-164">-Confirm</span></span>
<span data-ttu-id="17baf-165">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="17baf-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17baf-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17baf-166">-WhatIf</span></span>
<span data-ttu-id="17baf-167">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="17baf-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17baf-168">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="17baf-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17baf-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17baf-169">CommonParameters</span></span>
<span data-ttu-id="17baf-170">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="17baf-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17baf-171">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="17baf-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17baf-172">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="17baf-172">INPUTS</span></span>

### <span data-ttu-id="17baf-173">System. String</span><span class="sxs-lookup"><span data-stu-id="17baf-173">System.String</span></span>

### <span data-ttu-id="17baf-174">Microsoft. Azure. Command. HealthcareApisService. models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="17baf-174">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="17baf-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17baf-175">OUTPUTS</span></span>

### <span data-ttu-id="17baf-176">Microsoft. Azure. Command. HealthcareApisService. models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="17baf-176">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="17baf-177">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="17baf-177">NOTES</span></span>

## <span data-ttu-id="17baf-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17baf-178">RELATED LINKS</span></span>
