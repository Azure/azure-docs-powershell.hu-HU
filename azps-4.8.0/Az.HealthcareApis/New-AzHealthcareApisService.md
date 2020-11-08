---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: f5f8f00a2ab73485b4da6ad6df17ecf526c360bb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184927"
---
# <span data-ttu-id="b4707-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="b4707-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="b4707-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4707-102">SYNOPSIS</span></span>
<span data-ttu-id="b4707-103">Egy szolgáltatási példány metaadatait hozza létre.</span><span class="sxs-lookup"><span data-stu-id="b4707-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="b4707-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4707-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-ExportStorageAccountName <String>] [-EnableSmartProxy] [-ManagedIdentity]
 [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4707-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4707-105">DESCRIPTION</span></span>
<span data-ttu-id="b4707-106">Egy szolgáltatási példány metaadatait hozza létre vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="b4707-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="b4707-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b4707-107">EXAMPLES</span></span>

### <span data-ttu-id="b4707-108">Példa 1: létrehoz egy új Azure healthcareapis fhir szolgáltatás nevű MyService az erőforráscsoport MyResourceGroup egy olyan helyen, westus2 a 400 cosmosdb</span><span class="sxs-lookup"><span data-stu-id="b4707-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
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

## <span data-ttu-id="b4707-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4707-109">PARAMETERS</span></span>

### <span data-ttu-id="b4707-110">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="b4707-110">-AccessPolicyObjectId</span></span>
<span data-ttu-id="b4707-111">Az Access-házirend objektum-azonosítóinak listája.</span><span class="sxs-lookup"><span data-stu-id="b4707-111">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="b4707-112">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="b4707-112">-AllowCorsCredential</span></span>
<span data-ttu-id="b4707-113">HealthcareApis Fhir szolgáltatás AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="b4707-113">HealthcareApis Fhir Service AllowCorsCredential.</span></span>

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

### <span data-ttu-id="b4707-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4707-114">-AsJob</span></span>
<span data-ttu-id="b4707-115">A parancsmagot feladatként futtathatja a háttérben.</span><span class="sxs-lookup"><span data-stu-id="b4707-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="b4707-116">-Közönség</span><span class="sxs-lookup"><span data-stu-id="b4707-116">-Audience</span></span>
<span data-ttu-id="b4707-117">A HealthcareApis Fhir szolgáltatás célközönsége.</span><span class="sxs-lookup"><span data-stu-id="b4707-117">HealthcareApis Fhir Service Audience.</span></span>

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

### <span data-ttu-id="b4707-118">-Authority (jogosultság)</span><span class="sxs-lookup"><span data-stu-id="b4707-118">-Authority</span></span>
<span data-ttu-id="b4707-119">HealthcareApis Fhir szolgáltató hatóság.</span><span class="sxs-lookup"><span data-stu-id="b4707-119">HealthcareApis Fhir Service Authority.</span></span>

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

### <span data-ttu-id="b4707-120">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="b4707-120">-CorsHeader</span></span>
<span data-ttu-id="b4707-121">A CORS fejlécének HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="b4707-121">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="b4707-122">Adja meg azokat a HTTP-fejléceket, amelyek a kérés során használhatók.</span><span class="sxs-lookup"><span data-stu-id="b4707-122">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="b4707-123">Használja a \* tetszőleges fejlécet.</span><span class="sxs-lookup"><span data-stu-id="b4707-123">Use \* for any header.</span></span>

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

### <span data-ttu-id="b4707-124">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="b4707-124">-CorsMaxAge</span></span>
<span data-ttu-id="b4707-125">HealthcareApis Fhir szolgáltatás CORS Max Age.</span><span class="sxs-lookup"><span data-stu-id="b4707-125">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="b4707-126">Adja meg, hogy a kérésből mennyi ideig legyen gyorsítótárban lévő eredmény.</span><span class="sxs-lookup"><span data-stu-id="b4707-126">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="b4707-127">Példa: 600 10 percet jelent.</span><span class="sxs-lookup"><span data-stu-id="b4707-127">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="b4707-128">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="b4707-128">-CorsMethod</span></span>
<span data-ttu-id="b4707-129">A CORS metódus HealthcareApis Fhir szolgáltatásának listája.</span><span class="sxs-lookup"><span data-stu-id="b4707-129">HealthcareApis Fhir Service List of Cors Method.</span></span>

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

### <span data-ttu-id="b4707-130">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="b4707-130">-CorsOrigin</span></span>
<span data-ttu-id="b4707-131">A HealthcareApis Fhir szolgáltatás CORS eredete.</span><span class="sxs-lookup"><span data-stu-id="b4707-131">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="b4707-132">Adja meg az API-t elérő származási webhelyek URL-címét, vagy használja a \*-ot bármely webhelyről való hozzáférés engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="b4707-132">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

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

### <span data-ttu-id="b4707-133">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="b4707-133">-CosmosOfferThroughput</span></span>
<span data-ttu-id="b4707-134">HealthcareApis Fhir szolgáltatás CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="b4707-134">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="b4707-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4707-135">-DefaultProfile</span></span>
<span data-ttu-id="b4707-136">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4707-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4707-137">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="b4707-137">-EnableSmartProxy</span></span>
<span data-ttu-id="b4707-138">HealthcareApis Fhir szolgáltatás EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="b4707-138">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="b4707-139">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b4707-139">-ExportStorageAccountName</span></span>
<span data-ttu-id="b4707-140">A HealthcareApis Fhir-szolgáltatása exportálja a tárolási fiók nevét.</span><span class="sxs-lookup"><span data-stu-id="b4707-140">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="b4707-141">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="b4707-141">-FhirVersion</span></span>
<span data-ttu-id="b4707-142">Fhir verziója.</span><span class="sxs-lookup"><span data-stu-id="b4707-142">Fhir Version.</span></span>

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

### <span data-ttu-id="b4707-143">-Kind</span><span class="sxs-lookup"><span data-stu-id="b4707-143">-Kind</span></span>
<span data-ttu-id="b4707-144">A HealthcareApis szolgáltatás típusa.</span><span class="sxs-lookup"><span data-stu-id="b4707-144">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="b4707-145">Az alapértelmezett érték a Fhir</span><span class="sxs-lookup"><span data-stu-id="b4707-145">The default value is Fhir</span></span>

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

### <span data-ttu-id="b4707-146">-Hely</span><span class="sxs-lookup"><span data-stu-id="b4707-146">-Location</span></span>
<span data-ttu-id="b4707-147">HealthcareApis szolgáltatás helye.</span><span class="sxs-lookup"><span data-stu-id="b4707-147">HealthcareApis Service Location.</span></span>

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

### <span data-ttu-id="b4707-148">-ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="b4707-148">-ManagedIdentity</span></span>
<span data-ttu-id="b4707-149">Felügyelt identitást használ?</span><span class="sxs-lookup"><span data-stu-id="b4707-149">Use Managed Identity?</span></span>

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

### <span data-ttu-id="b4707-150">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b4707-150">-Name</span></span>
<span data-ttu-id="b4707-151">HealthcareApis szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="b4707-151">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="b4707-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4707-152">-ResourceGroupName</span></span>
<span data-ttu-id="b4707-153">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="b4707-153">Resource Group Name.</span></span>

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

### <span data-ttu-id="b4707-154">-Címke</span><span class="sxs-lookup"><span data-stu-id="b4707-154">-Tag</span></span>
<span data-ttu-id="b4707-155">HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="b4707-155">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="b4707-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b4707-156">-Confirm</span></span>
<span data-ttu-id="b4707-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b4707-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4707-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4707-158">-WhatIf</span></span>
<span data-ttu-id="b4707-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b4707-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4707-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b4707-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4707-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4707-161">CommonParameters</span></span>
<span data-ttu-id="b4707-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4707-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4707-163">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b4707-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4707-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4707-164">INPUTS</span></span>

### <span data-ttu-id="b4707-165">System. String</span><span class="sxs-lookup"><span data-stu-id="b4707-165">System.String</span></span>

## <span data-ttu-id="b4707-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4707-166">OUTPUTS</span></span>

### <span data-ttu-id="b4707-167">Microsoft. Azure. Command. HealthcareApisService. models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="b4707-167">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="b4707-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4707-168">NOTES</span></span>

## <span data-ttu-id="b4707-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4707-169">RELATED LINKS</span></span>