---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/import-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
ms.openlocfilehash: 5a9141cf0f609eedd35c25f6fd3d7977201e58c9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478881"
---
# <span data-ttu-id="4b1f9-101">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4b1f9-101">Import-AzApiManagementApi</span></span>

## <span data-ttu-id="4b1f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b1f9-102">SYNOPSIS</span></span>
<span data-ttu-id="4b1f9-103">API-t importál egy fájlból vagy URL-címből.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-103">Imports an API from a file or a URL.</span></span>

## <span data-ttu-id="4b1f9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4b1f9-104">SYNTAX</span></span>

### <span data-ttu-id="4b1f9-105">ImportFromLocalFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4b1f9-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b1f9-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="4b1f9-106">ImportFromUrl</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b1f9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4b1f9-107">DESCRIPTION</span></span>
<span data-ttu-id="4b1f9-108">Az **Import-AzApiManagementApi** parancsmag importálja az Azure API Felügyeleti API-t egy fájlból vagy egy URL-címből a webalkalmazás leírásának nyelve (WADL), a webszolgáltatások leírási nyelve (WSDL) vagy a Swagger formátumban.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-108">The **Import-AzApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="4b1f9-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4b1f9-109">EXAMPLES</span></span>

### <span data-ttu-id="4b1f9-110">1. példa: API importálása WADL-fájlból</span><span class="sxs-lookup"><span data-stu-id="4b1f9-110">Example 1: Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="4b1f9-111">Ez a parancs egy API-t importál a megadott WADL-fájlból.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="4b1f9-112">2. példa: API importálása Swagger-fájlból</span><span class="sxs-lookup"><span data-stu-id="4b1f9-112">Example 2: Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="4b1f9-113">Ez a parancs egy API-t importál a megadott Swagger-fájlból.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="4b1f9-114">3. példa: API importálása WADL-hivatkozásból</span><span class="sxs-lookup"><span data-stu-id="4b1f9-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="4b1f9-115">Ez a parancs egy API-t importál a megadott WADL-csatolásból.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-115">This command imports an API from the specified WADL link.</span></span>

### <span data-ttu-id="4b1f9-116">4. példa: API importálása Open Api-hivatkozásból</span><span class="sxs-lookup"><span data-stu-id="4b1f9-116">Example 4: Import an API from a Open Api Link</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Import-AzApiManagementApi -Context $context -SpecificationFormat OpenApi -SpecificationUrl https://raw.githubusercontent.com/OAI/OpenAPI-Specification/master/examples/v3.0/petstore.yaml -Path "petstore30"

ApiId                         : af3f57bab399455aa875d7050654e9d1
Name                          : Swagger Petstore
Description                   :
ServiceUrl                    : http://petstore.swagger.io/v1
Path                          : petstore30
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    :
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          :
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               :
Id                            : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apis/af3f57bab399455aa875d7050654e9d1     
ResourceGroupName             : Api-Default-West-US
ServiceName                   : contoso
```

<span data-ttu-id="4b1f9-117">Ez a parancs egy API-t importál a megadott Open 3.0 specifikációkapcsolatból.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-117">This command imports an API from the specified Open 3.0 specification link.</span></span>

### <span data-ttu-id="4b1f9-118">5. példa: API importálása Open Api-hivatkozásból ApiVersion-készletbe</span><span class="sxs-lookup"><span data-stu-id="4b1f9-118">Example 5:  Import an API from a Open Api Link into a ApiVersion Set</span></span>

```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Import-AzApiManagementApi -Context $context -SpecificationPath "C:\contoso\specifications\uspto.yml" -SpecificationFormat OpenApi -Path uspostal -ApiVersionSetId 0d50e2cf-aaeb-4ea3-8a58-db9ec079c6cd -ApiVersion v2

ApiId                         : 6c3f20c66e5745b19229d06cd865948f
Name                          : USPTO Data Set API
Description                   : The Data Set API (DSAPI) allows the public users to discover and search USPTO exported data sets. This is a generic API that allows USPTO users to make any CSV based data files
                                searchable through API. With the help of GET call, it returns the list of data fields that are searchable. With the help of POST call, data can be fetched based on the filters on the    
                                field names. Please note that POST call is used to search the actual data. The reason for the POST call is that it allows users to specify any complex search criteria without worry      
                                about the GET size limitations as well as encoding of the input parameters.
ServiceUrl                    : https://developer.uspto.gov/ds-api
Path                          : uspostal
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    : v2
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          :
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apiVersionSets/0d50e2cf-aaeb-4ea3-8a58-db9ec079c6cd
Id                            : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apis/6c3f20c66e5745b19229d06cd865948f    
ResourceGroupName             : Api-Default-East-US
ServiceName                   : contoso
```

<span data-ttu-id="4b1f9-119">Ez a parancs importál egy API-t a megadott Open 3.0 specifikációs dokumentumból, és létrehoz egy új ApiVersiont.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-119">This command imports an API from the specified Open 3.0 specification document and create a new ApiVersion.</span></span>

## <span data-ttu-id="4b1f9-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b1f9-120">PARAMETERS</span></span>

### <span data-ttu-id="4b1f9-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4b1f9-121">-ApiId</span></span>
<span data-ttu-id="4b1f9-122">Megadja az importálni megfelelő API azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-122">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="4b1f9-123">Ha nem adja meg ezt a paramétert, a rendszer létrehoz egy azonosítót.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-123">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="4b1f9-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="4b1f9-124">-ApiRevision</span></span>
<span data-ttu-id="4b1f9-125">Az API-változat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-125">Identifier of API Revision.</span></span> <span data-ttu-id="4b1f9-126">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-126">This parameter is optional.</span></span> <span data-ttu-id="4b1f9-127">Ha nincs megadva, az importálás az aktuálisan aktív változatra vagy egy új api-ra történik.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-127">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="4b1f9-128">-ApiType</span><span class="sxs-lookup"><span data-stu-id="4b1f9-128">-ApiType</span></span>
<span data-ttu-id="4b1f9-129">Ez a paraméter nem kötelező a Http alapértelmezett értékkel.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-129">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="4b1f9-130">A Soap beállítás csak WSDL importáló esetén alkalmazható, és SOAP Átadó API-t hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-130">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b1f9-131">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4b1f9-131">-ApiVersion</span></span>
<span data-ttu-id="4b1f9-132">A létrehozni szükséges Api API-verziója.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-132">Api Version of the Api to create.</span></span> <span data-ttu-id="4b1f9-133">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="4b1f9-134">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="4b1f9-134">-ApiVersionSetId</span></span>
<span data-ttu-id="4b1f9-135">A kapcsolódó Api-verziókészlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-135">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="4b1f9-136">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="4b1f9-137">-Környezet</span><span class="sxs-lookup"><span data-stu-id="4b1f9-137">-Context</span></span>
<span data-ttu-id="4b1f9-138">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-138">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b1f9-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b1f9-139">-DefaultProfile</span></span>
<span data-ttu-id="4b1f9-140">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b1f9-141">-Path</span><span class="sxs-lookup"><span data-stu-id="4b1f9-141">-Path</span></span>
<span data-ttu-id="4b1f9-142">Egy webes API-elérési utat ad meg az API nyilvános URL-címének utolsó részeként.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-142">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="4b1f9-143">Ezt az URL-címet használják az API-t használó ügyfelek arra, hogy kéréseket küldenek a webszolgáltatásnak.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-143">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="4b1f9-144">1–400 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-144">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="4b1f9-145">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-145">The default value is $Null.</span></span>

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

### <span data-ttu-id="4b1f9-146">-Protocol</span><span class="sxs-lookup"><span data-stu-id="4b1f9-146">-Protocol</span></span>
<span data-ttu-id="4b1f9-147">Web API-protokollok (http, https).</span><span class="sxs-lookup"><span data-stu-id="4b1f9-147">Web API protocols (http, https).</span></span> <span data-ttu-id="4b1f9-148">Protokollok, amelyeken keresztül az API elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-148">Protocols over which API is made available.</span></span> <span data-ttu-id="4b1f9-149">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-149">This parameter is optional.</span></span> <span data-ttu-id="4b1f9-150">Ha fel van adva, az felülírja a specifikációs dokumentumban megadott protokollokat.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-150">If provided it will override the protocols specified in the specifications document.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b1f9-151">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="4b1f9-151">-ServiceUrl</span></span>
<span data-ttu-id="4b1f9-152">A webszolgáltatás API-t kitűnő URL-címe.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-152">A URL of the web service exposing the API.</span></span> <span data-ttu-id="4b1f9-153">Ezt az URL-címet csak az Azure API Management fogja használni, és nem teszi nyilvánosra.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-153">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="4b1f9-154">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-154">This parameter is optional.</span></span> <span data-ttu-id="4b1f9-155">Ha fel van adva, az felülírja a Specifikációk dokumentumban megadott ServiceUrl szabványt.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-155">If provided it will override the ServiceUrl specified in the Specifications document.</span></span>

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

### <span data-ttu-id="4b1f9-156">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="4b1f9-156">-SpecificationFormat</span></span>
<span data-ttu-id="4b1f9-157">A specifikáció formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-157">Specifies the specification format.</span></span>
<span data-ttu-id="4b1f9-158">psdx_paramvalues Wadl, Wsdl és Swagger.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-158">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi, OpenApiJson

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b1f9-159">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="4b1f9-159">-SpecificationPath</span></span>
<span data-ttu-id="4b1f9-160">A specifikáció fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-160">Specifies the specification file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromLocalFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b1f9-161">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="4b1f9-161">-SpecificationUrl</span></span>
<span data-ttu-id="4b1f9-162">A specifikáció URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-162">Specifies the specification URL.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b1f9-163">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="4b1f9-163">-WsdlEndpointName</span></span>
<span data-ttu-id="4b1f9-164">Az importálni szánt WSDL-végpont (port) helyi neve.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-164">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="4b1f9-165">1–400 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-165">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="4b1f9-166">Ez a paraméter nem kötelező, és csak a Wsdl importálásához szükséges.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-166">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="4b1f9-167">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-167">Default value is $null.</span></span>

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

### <span data-ttu-id="4b1f9-168">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="4b1f9-168">-WsdlServiceName</span></span>
<span data-ttu-id="4b1f9-169">Az importálni szánt WSDL-szolgáltatás helyi neve.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-169">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="4b1f9-170">1–400 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-170">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="4b1f9-171">Ez a paraméter nem kötelező, és csak a Wsdl importálásához szükséges.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-171">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="4b1f9-172">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-172">Default value is $null.</span></span>

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

### <span data-ttu-id="4b1f9-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b1f9-173">CommonParameters</span></span>
<span data-ttu-id="4b1f9-174">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b1f9-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b1f9-175">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b1f9-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b1f9-176">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b1f9-176">INPUTS</span></span>

### <span data-ttu-id="4b1f9-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4b1f9-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4b1f9-178">System.String</span><span class="sxs-lookup"><span data-stu-id="4b1f9-178">System.String</span></span>

### <span data-ttu-id="4b1f9-179">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="4b1f9-179">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="4b1f9-180">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="4b1f9-180">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4b1f9-181">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b1f9-181">OUTPUTS</span></span>

### <span data-ttu-id="4b1f9-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4b1f9-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="4b1f9-183">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4b1f9-183">NOTES</span></span>

## <span data-ttu-id="4b1f9-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b1f9-184">RELATED LINKS</span></span>

[<span data-ttu-id="4b1f9-185">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4b1f9-185">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="4b1f9-186">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4b1f9-186">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="4b1f9-187">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4b1f9-187">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="4b1f9-188">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4b1f9-188">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="4b1f9-189">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4b1f9-189">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


