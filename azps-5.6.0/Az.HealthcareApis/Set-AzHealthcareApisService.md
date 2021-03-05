---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: 2ff0f9f03524368e01b6edbcad5b8db8fef4fb21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013158"
---
# <span data-ttu-id="5a268-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="5a268-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="5a268-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a268-102">SYNOPSIS</span></span>
<span data-ttu-id="5a268-103">Egy meglévő egészségügyiApis egészségügyi szolgáltatás frissítése.</span><span class="sxs-lookup"><span data-stu-id="5a268-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="5a268-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5a268-104">SYNTAX</span></span>

### <span data-ttu-id="5a268-105">ServiceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5a268-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-CosmosKeyVaultKeyUri <String>] [-Authority <String>] [-Audience <String>] [-EnableSmartProxy]
 [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>] [-CorsMethod <String[]>]
 [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential] [-ExportStorageAccountName <String>]
 [-AccessPolicyObjectId <String[]>] [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>]
 [-AsJob] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a268-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a268-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>]
 [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a268-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a268-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a268-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5a268-108">DESCRIPTION</span></span>
<span data-ttu-id="5a268-109">Egy meglévő egészségügyiApis egészségügyi szolgáltatás frissítése.</span><span class="sxs-lookup"><span data-stu-id="5a268-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="5a268-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5a268-110">EXAMPLES</span></span>

### <span data-ttu-id="5a268-111">1. példa: Frissíti a MyResourceGroup erőforráscsoport MyResourceGroup nevű meglévő egészségügyi szolgáltatását az 500-as értékekkel.</span><span class="sxs-lookup"><span data-stu-id="5a268-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

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
CosmosKeyVaultKeyUri    : 
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

### <span data-ttu-id="5a268-112">2. példa: Frissíti a MyResourceGroup erőforráscsoport MyResourceGroup nevű meglévő egészségügyi szolgáltatását az 500 és a kulcskulcs uri "https:// \<my-keyvault> .vault.azure.net/keys/" értékével. \<my-key></span><span class="sxs-lookup"><span data-stu-id="5a268-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>

```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService"
PS C:\> Set-AzHealthcareApisService -ResourceId $ResourceId  -CosmosOfferThroughput 500 -CosmosKeyVaultKeyUri "https://<my-keyvault>.vault.azure.net/keys/<my-key>"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosKeyVaultKeyUri    : https://<my-keyvault>.vault.azure.net/keys/<my-key>
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

## <span data-ttu-id="5a268-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a268-113">PARAMETERS</span></span>

### <span data-ttu-id="5a268-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="5a268-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="5a268-115">Access-házirendobjektum-iD-ek listája.</span><span class="sxs-lookup"><span data-stu-id="5a268-115">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="5a268-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="5a268-116">-AllowCorsCredential</span></span>
<span data-ttu-id="5a268-117">HealthcareApis FhirService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="5a268-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

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

### <span data-ttu-id="5a268-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a268-118">-AsJob</span></span>
<span data-ttu-id="5a268-119">Futtassa a parancsmagot feladatként a háttérben.</span><span class="sxs-lookup"><span data-stu-id="5a268-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="5a268-120">-Audience</span><span class="sxs-lookup"><span data-stu-id="5a268-120">-Audience</span></span>
<span data-ttu-id="5a268-121">HealthcareApis FhirService Audience.</span><span class="sxs-lookup"><span data-stu-id="5a268-121">HealthcareApis FhirService Audience.</span></span>

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

### <span data-ttu-id="5a268-122">-Authority</span><span class="sxs-lookup"><span data-stu-id="5a268-122">-Authority</span></span>
<span data-ttu-id="5a268-123">HealthcareApis FhirService Authority.</span><span class="sxs-lookup"><span data-stu-id="5a268-123">HealthcareApis FhirService Authority.</span></span>

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

### <span data-ttu-id="5a268-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="5a268-124">-CorsHeader</span></span>
<span data-ttu-id="5a268-125">HealthcareApis FhirService List of Cors Headers.</span><span class="sxs-lookup"><span data-stu-id="5a268-125">HealthcareApis FhirService List of Cors Headers.</span></span>
<span data-ttu-id="5a268-126">Adja meg a kérés során használható HTTP-fejléceket.</span><span class="sxs-lookup"><span data-stu-id="5a268-126">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="5a268-127">Az élőfejhez használja a " \* " kódot.</span><span class="sxs-lookup"><span data-stu-id="5a268-127">Use " \* " for any header.</span></span>

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

### <span data-ttu-id="5a268-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="5a268-128">-CorsMaxAge</span></span>
<span data-ttu-id="5a268-129">HealthcareApis FhirService Cors Max Age.</span><span class="sxs-lookup"><span data-stu-id="5a268-129">HealthcareApis FhirService Cors Max Age.</span></span>
<span data-ttu-id="5a268-130">Adja meg, hogy mennyi ideig legyen gyorsítótárazva egy kérés eredménye másodpercek alatt.</span><span class="sxs-lookup"><span data-stu-id="5a268-130">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="5a268-131">Példa: A 600 jelentése 10 perc.</span><span class="sxs-lookup"><span data-stu-id="5a268-131">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="5a268-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="5a268-132">-CorsMethod</span></span>
<span data-ttu-id="5a268-133">HealthcareApis FhirService List of Cors Methods.</span><span class="sxs-lookup"><span data-stu-id="5a268-133">HealthcareApis FhirService List of Cors Methods.</span></span>

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

### <span data-ttu-id="5a268-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="5a268-134">-CorsOrigin</span></span>
<span data-ttu-id="5a268-135">HealthcareApis FhirService List of Cors Origins.</span><span class="sxs-lookup"><span data-stu-id="5a268-135">HealthcareApis FhirService List of Cors Origins.</span></span>
<span data-ttu-id="5a268-136">Adja meg az API-hoz hozzáférő forráswebhelyek URL-címeit, vagy a " \* " használatával engedélyezze a hozzáférést bármely webhelyről.</span><span class="sxs-lookup"><span data-stu-id="5a268-136">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

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

### <span data-ttu-id="5a268-137">-SkeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="5a268-137">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="5a268-138">HealthcareApis Fhir ServiceLangsKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="5a268-138">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="5a268-139">A háttéradatbázis ügyfél által kezelt kulcsának URI-ja.</span><span class="sxs-lookup"><span data-stu-id="5a268-139">The URI of the customer-managed key for the backing database.</span></span>

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

### <span data-ttu-id="5a268-140">-SofferThroughput</span><span class="sxs-lookup"><span data-stu-id="5a268-140">-CosmosOfferThroughput</span></span>
<span data-ttu-id="5a268-141">HealthcareApis FhirService SOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="5a268-141">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="5a268-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a268-142">-DefaultProfile</span></span>
<span data-ttu-id="5a268-143">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a268-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a268-144">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="5a268-144">-DisableCorsCredential</span></span>
<span data-ttu-id="5a268-145">HealthcareApis FhirService CorsCredentials Not Allowed.</span><span class="sxs-lookup"><span data-stu-id="5a268-145">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

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

### <span data-ttu-id="5a268-146">-DisableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="5a268-146">-DisableManagedIdentity</span></span>
<span data-ttu-id="5a268-147">Tiltsa le a Felügyelt identitást.</span><span class="sxs-lookup"><span data-stu-id="5a268-147">Disable Managed Identity.</span></span>

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

### <span data-ttu-id="5a268-148">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="5a268-148">-DisableSmartProxy</span></span>
<span data-ttu-id="5a268-149">HealthcareApis FhirService DisableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="5a268-149">HealthcareApis FhirService DisableSmartProxy.</span></span>

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

### <span data-ttu-id="5a268-150">-EnableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="5a268-150">-EnableManagedIdentity</span></span>
<span data-ttu-id="5a268-151">Felügyelt identitás engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="5a268-151">Enable Managed Identity.</span></span>

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

### <span data-ttu-id="5a268-152">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="5a268-152">-EnableSmartProxy</span></span>
<span data-ttu-id="5a268-153">HealthcareApis FhirService EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="5a268-153">HealthcareApis FhirService EnableSmartProxy.</span></span>

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

### <span data-ttu-id="5a268-154">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5a268-154">-ExportStorageAccountName</span></span>
<span data-ttu-id="5a268-155">HealthcareApis Fhir Service Export Storage Account Name.</span><span class="sxs-lookup"><span data-stu-id="5a268-155">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="5a268-156">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a268-156">-InputObject</span></span>
<span data-ttu-id="5a268-157">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span><span class="sxs-lookup"><span data-stu-id="5a268-157">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

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

### <span data-ttu-id="5a268-158">-Name</span><span class="sxs-lookup"><span data-stu-id="5a268-158">-Name</span></span>
<span data-ttu-id="5a268-159">HealthcareApis szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="5a268-159">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="5a268-160">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="5a268-160">-PublicNetworkAccess</span></span>
<span data-ttu-id="5a268-161">A Felső szolgáltatás hálózati hozzáférési típusa.</span><span class="sxs-lookup"><span data-stu-id="5a268-161">The network access type for Fhir service.</span></span> <span data-ttu-id="5a268-162">Gyakran `Enabled` vagy `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="5a268-162">Commonly `Enabled` or `Disabled`.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a268-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a268-163">-ResourceGroupName</span></span>
<span data-ttu-id="5a268-164">HealthcareApis Service Resource Group Name (Egészségügyi szolgáltatáserőforrás-csoport neve).</span><span class="sxs-lookup"><span data-stu-id="5a268-164">HealthcareApis Service Resource Group Name.</span></span>

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

### <span data-ttu-id="5a268-165">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a268-165">-ResourceId</span></span>
<span data-ttu-id="5a268-166">HealthcareApis Fhir Service ResourceId.</span><span class="sxs-lookup"><span data-stu-id="5a268-166">HealthcareApis Fhir Service ResourceId.</span></span>

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

### <span data-ttu-id="5a268-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="5a268-167">-Tag</span></span>
<span data-ttu-id="5a268-168">HealthcareApis Fhir Service Account Tags.</span><span class="sxs-lookup"><span data-stu-id="5a268-168">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="5a268-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a268-169">-Confirm</span></span>
<span data-ttu-id="5a268-170">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5a268-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a268-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a268-171">-WhatIf</span></span>
<span data-ttu-id="5a268-172">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5a268-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a268-173">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5a268-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a268-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a268-174">CommonParameters</span></span>
<span data-ttu-id="5a268-175">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a268-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a268-176">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a268-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a268-177">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a268-177">INPUTS</span></span>

### <span data-ttu-id="5a268-178">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="5a268-178">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

### <span data-ttu-id="5a268-179">System.String</span><span class="sxs-lookup"><span data-stu-id="5a268-179">System.String</span></span>

## <span data-ttu-id="5a268-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a268-180">OUTPUTS</span></span>

### <span data-ttu-id="5a268-181">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="5a268-181">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="5a268-182">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5a268-182">NOTES</span></span>

## <span data-ttu-id="5a268-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a268-183">RELATED LINKS</span></span>
