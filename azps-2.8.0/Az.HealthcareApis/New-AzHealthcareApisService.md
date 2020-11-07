---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: 374b443157bf6ef36f39d3ee0dba34ae59419931
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666311"
---
# <span data-ttu-id="d0a43-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="d0a43-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="d0a43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d0a43-102">SYNOPSIS</span></span>
<span data-ttu-id="d0a43-103">Egy szolgáltatási példány metaadatait hozza létre.</span><span class="sxs-lookup"><span data-stu-id="d0a43-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="d0a43-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d0a43-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-EnableSmartProxy] [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0a43-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d0a43-105">DESCRIPTION</span></span>
<span data-ttu-id="d0a43-106">Egy szolgáltatási példány metaadatait hozza létre vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="d0a43-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="d0a43-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d0a43-107">EXAMPLES</span></span>

### <span data-ttu-id="d0a43-108">Példa 1: létrehoz egy új Azure healthcareapis fhir szolgáltatás nevű MyService az erőforráscsoport MyResourceGroup egy olyan helyen, westus2 a 400 cosmosdb</span><span class="sxs-lookup"><span data-stu-id="d0a43-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput  400

ResourceGroupName Name Location        Kind   CosmosOfferThroughput
----------------- ----------- -------------------------------
MyResourceGroup   MyService   westus2    fhir-R4   400

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

## <span data-ttu-id="d0a43-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d0a43-109">PARAMETERS</span></span>

### <span data-ttu-id="d0a43-110">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="d0a43-110">-AccessPolicyObjectId</span></span>
<span data-ttu-id="d0a43-111">Az Access-házirend objektum-azonosítóinak listája.</span><span class="sxs-lookup"><span data-stu-id="d0a43-111">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="d0a43-112">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="d0a43-112">-AllowCorsCredential</span></span>
<span data-ttu-id="d0a43-113">HealthcareApis Fhir szolgáltatás AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="d0a43-113">HealthcareApis Fhir Service AllowCorsCredential.</span></span>

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

### <span data-ttu-id="d0a43-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0a43-114">-AsJob</span></span>
<span data-ttu-id="d0a43-115">A parancsmagot feladatként futtathatja a háttérben.</span><span class="sxs-lookup"><span data-stu-id="d0a43-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="d0a43-116">-Közönség</span><span class="sxs-lookup"><span data-stu-id="d0a43-116">-Audience</span></span>
<span data-ttu-id="d0a43-117">A HealthcareApis Fhir szolgáltatás célközönsége.</span><span class="sxs-lookup"><span data-stu-id="d0a43-117">HealthcareApis Fhir Service Audience.</span></span>

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

### <span data-ttu-id="d0a43-118">-Authority (jogosultság)</span><span class="sxs-lookup"><span data-stu-id="d0a43-118">-Authority</span></span>
<span data-ttu-id="d0a43-119">HealthcareApis Fhir szolgáltató hatóság.</span><span class="sxs-lookup"><span data-stu-id="d0a43-119">HealthcareApis Fhir Service Authority.</span></span>

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

### <span data-ttu-id="d0a43-120">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="d0a43-120">-CorsHeader</span></span>
<span data-ttu-id="d0a43-121">A CORS fejlécének HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="d0a43-121">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="d0a43-122">Adja meg azokat a HTTP-fejléceket, amelyek a kérés során használhatók.</span><span class="sxs-lookup"><span data-stu-id="d0a43-122">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="d0a43-123">Használja a \* tetszőleges fejlécet.</span><span class="sxs-lookup"><span data-stu-id="d0a43-123">Use \* for any header.</span></span>

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

### <span data-ttu-id="d0a43-124">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="d0a43-124">-CorsMaxAge</span></span>
<span data-ttu-id="d0a43-125">HealthcareApis Fhir szolgáltatás CORS Max Age.</span><span class="sxs-lookup"><span data-stu-id="d0a43-125">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="d0a43-126">Adja meg, hogy a kérésből mennyi ideig legyen gyorsítótárban lévő eredmény.</span><span class="sxs-lookup"><span data-stu-id="d0a43-126">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="d0a43-127">Példa: 600 10 percet jelent.</span><span class="sxs-lookup"><span data-stu-id="d0a43-127">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="d0a43-128">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="d0a43-128">-CorsMethod</span></span>
<span data-ttu-id="d0a43-129">A CORS metódus HealthcareApis Fhir szolgáltatásának listája.</span><span class="sxs-lookup"><span data-stu-id="d0a43-129">HealthcareApis Fhir Service List of Cors Method.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: DELETE, GET, OPTIONS, PATCH, POST, PUT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a43-130">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="d0a43-130">-CorsOrigin</span></span>
<span data-ttu-id="d0a43-131">A HealthcareApis Fhir szolgáltatás CORS eredete.</span><span class="sxs-lookup"><span data-stu-id="d0a43-131">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="d0a43-132">Adja meg az API-t elérő származási webhelyek URL-címét, vagy használja a \*-ot bármely webhelyről való hozzáférés engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="d0a43-132">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

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

### <span data-ttu-id="d0a43-133">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="d0a43-133">-CosmosOfferThroughput</span></span>
<span data-ttu-id="d0a43-134">HealthcareApis Fhir szolgáltatás CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="d0a43-134">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="d0a43-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0a43-135">-DefaultProfile</span></span>
<span data-ttu-id="d0a43-136">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0a43-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0a43-137">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="d0a43-137">-EnableSmartProxy</span></span>
<span data-ttu-id="d0a43-138">HealthcareApis Fhir szolgáltatás EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="d0a43-138">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="d0a43-139">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="d0a43-139">-FhirVersion</span></span>
<span data-ttu-id="d0a43-140">Fhir verziója.</span><span class="sxs-lookup"><span data-stu-id="d0a43-140">Fhir Version.</span></span>

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

### <span data-ttu-id="d0a43-141">-Kind</span><span class="sxs-lookup"><span data-stu-id="d0a43-141">-Kind</span></span>
<span data-ttu-id="d0a43-142">A HealthcareApis szolgáltatás típusa.</span><span class="sxs-lookup"><span data-stu-id="d0a43-142">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="d0a43-143">Az alapértelmezett érték a Fhir</span><span class="sxs-lookup"><span data-stu-id="d0a43-143">The default value is Fhir</span></span>

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

### <span data-ttu-id="d0a43-144">-Hely</span><span class="sxs-lookup"><span data-stu-id="d0a43-144">-Location</span></span>
<span data-ttu-id="d0a43-145">HealthcareApis szolgáltatás helye.</span><span class="sxs-lookup"><span data-stu-id="d0a43-145">HealthcareApis Service Location.</span></span>

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

### <span data-ttu-id="d0a43-146">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d0a43-146">-Name</span></span>
<span data-ttu-id="d0a43-147">HealthcareApis szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="d0a43-147">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="d0a43-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0a43-148">-ResourceGroupName</span></span>
<span data-ttu-id="d0a43-149">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d0a43-149">Resource Group Name.</span></span>

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

### <span data-ttu-id="d0a43-150">-Címke</span><span class="sxs-lookup"><span data-stu-id="d0a43-150">-Tag</span></span>
<span data-ttu-id="d0a43-151">HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="d0a43-151">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="d0a43-152">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d0a43-152">-Confirm</span></span>
<span data-ttu-id="d0a43-153">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d0a43-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0a43-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0a43-154">-WhatIf</span></span>
<span data-ttu-id="d0a43-155">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d0a43-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0a43-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d0a43-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0a43-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0a43-157">CommonParameters</span></span>
<span data-ttu-id="d0a43-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d0a43-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0a43-159">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d0a43-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0a43-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0a43-160">INPUTS</span></span>

### <span data-ttu-id="d0a43-161">System. String</span><span class="sxs-lookup"><span data-stu-id="d0a43-161">System.String</span></span>

## <span data-ttu-id="d0a43-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0a43-162">OUTPUTS</span></span>

### <span data-ttu-id="d0a43-163">Microsoft. Azure. Command. HealthcareApisService. models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="d0a43-163">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="d0a43-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d0a43-164">NOTES</span></span>

## <span data-ttu-id="d0a43-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0a43-165">RELATED LINKS</span></span>
