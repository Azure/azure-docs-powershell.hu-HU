---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: 33f1af70b0fef7e89ccb584ed3b69f32e2810690
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386831"
---
# <span data-ttu-id="25f20-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="25f20-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="25f20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25f20-102">SYNOPSIS</span></span>
<span data-ttu-id="25f20-103">Létrehozza egy szolgáltatáspéldány metaadatait.</span><span class="sxs-lookup"><span data-stu-id="25f20-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="25f20-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="25f20-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>] [-ExportStorageAccountName <String>]
 [-EnableSmartProxy] [-ManagedIdentity] [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25f20-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="25f20-105">DESCRIPTION</span></span>
<span data-ttu-id="25f20-106">Létrehozza vagy frissíti egy szolgáltatási példány metaadatait.</span><span class="sxs-lookup"><span data-stu-id="25f20-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="25f20-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="25f20-107">EXAMPLES</span></span>

### <span data-ttu-id="25f20-108">1. példa: Létrehozza a MyResourceGroup erőforráscsoport MyResourceGroup nevű új Azure healthcareapis fhir szolgáltatását egy westus2 helyen, ahol az átviteli sebesség = 400</span><span class="sxs-lookup"><span data-stu-id="25f20-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput 400

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

### <span data-ttu-id="25f20-109">2. példa: Létrehozza a MyResourceGroup erőforráscsoport MyResourceGroup nevű új Azure healthcareapis fhir szolgáltatását egy westus2 helyen, ahol az átviteli sebesség = 400 és a kulcstár kulcs uri "https:// \<my-keyvault> \<my-key> .vault.azure.net/keys/"</span><span class="sxs-lookup"><span data-stu-id="25f20-109">Example 2 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput 400 -CosmosKeyVaultKeyUri "https://<my-keyvault>.vault.azure.net/keys/<my-key>"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  : https://<my-keyvault>.vault.azure.net/keys/<my-key>
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

## <span data-ttu-id="25f20-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25f20-110">PARAMETERS</span></span>

### <span data-ttu-id="25f20-111">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="25f20-111">-AccessPolicyObjectId</span></span>
<span data-ttu-id="25f20-112">Access-házirendobjektum-iD-ek listája.</span><span class="sxs-lookup"><span data-stu-id="25f20-112">List of Access Policy Object IDs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f20-113">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="25f20-113">-AllowCorsCredential</span></span>
<span data-ttu-id="25f20-114">HealthcareApis Fhir Service AllowCorsCredentials.</span><span class="sxs-lookup"><span data-stu-id="25f20-114">HealthcareApis Fhir Service AllowCorsCredentials.</span></span>

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

### <span data-ttu-id="25f20-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25f20-115">-AsJob</span></span>
<span data-ttu-id="25f20-116">Futtassa a parancsmagot feladatként a háttérben.</span><span class="sxs-lookup"><span data-stu-id="25f20-116">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="25f20-117">-Audience</span><span class="sxs-lookup"><span data-stu-id="25f20-117">-Audience</span></span>
<span data-ttu-id="25f20-118">HealthcareApis Fhir Service Audience.</span><span class="sxs-lookup"><span data-stu-id="25f20-118">HealthcareApis Fhir Service Audience.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f20-119">-Authority</span><span class="sxs-lookup"><span data-stu-id="25f20-119">-Authority</span></span>
<span data-ttu-id="25f20-120">HealthcareApis Fhir Service Authority.</span><span class="sxs-lookup"><span data-stu-id="25f20-120">HealthcareApis Fhir Service Authority.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f20-121">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="25f20-121">-CorsHeader</span></span>
<span data-ttu-id="25f20-122">HealthcareApis Fhir Service List of Cors Header.</span><span class="sxs-lookup"><span data-stu-id="25f20-122">HealthcareApis Fhir Service List of Cors Header.</span></span>
<span data-ttu-id="25f20-123">Adja meg a kérés során használható HTTP-fejléceket.</span><span class="sxs-lookup"><span data-stu-id="25f20-123">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="25f20-124">Az élőfejhez használja a " \* " kódot.</span><span class="sxs-lookup"><span data-stu-id="25f20-124">Use " \* " for any header.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f20-125">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="25f20-125">-CorsMaxAge</span></span>
<span data-ttu-id="25f20-126">HealthcareApis Fhir Service Cors Max Age.</span><span class="sxs-lookup"><span data-stu-id="25f20-126">HealthcareApis Fhir Service Cors Max Age.</span></span>
<span data-ttu-id="25f20-127">Adja meg, hogy mennyi ideig legyen gyorsítótárazva egy kérés eredménye másodpercek alatt.</span><span class="sxs-lookup"><span data-stu-id="25f20-127">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="25f20-128">Példa: A 600 jelentése 10 perc.</span><span class="sxs-lookup"><span data-stu-id="25f20-128">Example: 600 means 10 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f20-129">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="25f20-129">-CorsMethod</span></span>
<span data-ttu-id="25f20-130">HealthcareApis Fhir Service List of Cors Method.</span><span class="sxs-lookup"><span data-stu-id="25f20-130">HealthcareApis Fhir Service List of Cors Method.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f20-131">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="25f20-131">-CorsOrigin</span></span>
<span data-ttu-id="25f20-132">HealthcareApis Fhir Service List of Cors Origin.</span><span class="sxs-lookup"><span data-stu-id="25f20-132">HealthcareApis Fhir Service List of Cors Origin.</span></span>
<span data-ttu-id="25f20-133">Adja meg az API-hoz hozzáférő forráswebhelyek URL-címeit, vagy a " \* " használatával engedélyezze a hozzáférést bármely webhelyről.</span><span class="sxs-lookup"><span data-stu-id="25f20-133">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f20-134">-SkeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="25f20-134">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="25f20-135">HealthcareApis Fhir ServiceLangsKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="25f20-135">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="25f20-136">A háttéradatbázis ügyfél által kezelt kulcsának URI-ja.</span><span class="sxs-lookup"><span data-stu-id="25f20-136">The URI of the customer-managed key for the backing database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f20-137">-SofferThroughput</span><span class="sxs-lookup"><span data-stu-id="25f20-137">-CosmosOfferThroughput</span></span>
<span data-ttu-id="25f20-138">HealthcareApis Fhir ServiceLangsOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="25f20-138">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f20-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25f20-139">-DefaultProfile</span></span>
<span data-ttu-id="25f20-140">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25f20-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25f20-141">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="25f20-141">-EnableSmartProxy</span></span>
<span data-ttu-id="25f20-142">HealthcareApis Fhir Service EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="25f20-142">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="25f20-143">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="25f20-143">-ExportStorageAccountName</span></span>
<span data-ttu-id="25f20-144">HealthcareApis Fhir Service Export Storage Account Name.</span><span class="sxs-lookup"><span data-stu-id="25f20-144">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f20-145">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="25f20-145">-FhirVersion</span></span>
<span data-ttu-id="25f20-146">Fhir verzió.</span><span class="sxs-lookup"><span data-stu-id="25f20-146">Fhir Version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f20-147">-Kind</span><span class="sxs-lookup"><span data-stu-id="25f20-147">-Kind</span></span>
<span data-ttu-id="25f20-148">Az HealthcareApis szolgáltatás fajtája.</span><span class="sxs-lookup"><span data-stu-id="25f20-148">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="25f20-149">Az alapértelmezett érték a Hir</span><span class="sxs-lookup"><span data-stu-id="25f20-149">The default value is Fhir</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25f20-150">-Location</span><span class="sxs-lookup"><span data-stu-id="25f20-150">-Location</span></span>
<span data-ttu-id="25f20-151">HealthcareApis szolgáltatás helye.</span><span class="sxs-lookup"><span data-stu-id="25f20-151">HealthcareApis Service Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25f20-152">-ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="25f20-152">-ManagedIdentity</span></span>
<span data-ttu-id="25f20-153">Felügyelt identitást használ?</span><span class="sxs-lookup"><span data-stu-id="25f20-153">Use Managed Identity?</span></span>

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

### <span data-ttu-id="25f20-154">-Name</span><span class="sxs-lookup"><span data-stu-id="25f20-154">-Name</span></span>
<span data-ttu-id="25f20-155">HealthcareApis szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="25f20-155">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25f20-156">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="25f20-156">-PublicNetworkAccess</span></span>
<span data-ttu-id="25f20-157">A Felső szolgáltatás hálózati hozzáférési típusa.</span><span class="sxs-lookup"><span data-stu-id="25f20-157">The network access type for Fhir service.</span></span> <span data-ttu-id="25f20-158">Gyakran `Enabled` vagy `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="25f20-158">Commonly `Enabled` or `Disabled`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f20-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25f20-159">-ResourceGroupName</span></span>
<span data-ttu-id="25f20-160">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="25f20-160">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25f20-161">-Tag</span><span class="sxs-lookup"><span data-stu-id="25f20-161">-Tag</span></span>
<span data-ttu-id="25f20-162">HealthcareApis Fhir Service Account Tags.</span><span class="sxs-lookup"><span data-stu-id="25f20-162">HealthcareApis Fhir Service Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f20-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25f20-163">-Confirm</span></span>
<span data-ttu-id="25f20-164">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="25f20-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25f20-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25f20-165">-WhatIf</span></span>
<span data-ttu-id="25f20-166">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="25f20-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25f20-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="25f20-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25f20-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25f20-168">CommonParameters</span></span>
<span data-ttu-id="25f20-169">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25f20-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25f20-170">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25f20-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25f20-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25f20-171">INPUTS</span></span>

### <span data-ttu-id="25f20-172">System.String</span><span class="sxs-lookup"><span data-stu-id="25f20-172">System.String</span></span>

## <span data-ttu-id="25f20-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25f20-173">OUTPUTS</span></span>

### <span data-ttu-id="25f20-174">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="25f20-174">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="25f20-175">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="25f20-175">NOTES</span></span>

## <span data-ttu-id="25f20-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25f20-176">RELATED LINKS</span></span>
