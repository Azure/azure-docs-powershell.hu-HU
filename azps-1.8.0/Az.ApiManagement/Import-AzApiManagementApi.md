---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/import-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
ms.openlocfilehash: 690ebbfb1bb3cca6de8feb1f199068510e41f1d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665658"
---
# <span data-ttu-id="c4958-101">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c4958-101">Import-AzApiManagementApi</span></span>

## <span data-ttu-id="c4958-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c4958-102">SYNOPSIS</span></span>
<span data-ttu-id="c4958-103">API-t importál egy fájlból vagy URL-címről.</span><span class="sxs-lookup"><span data-stu-id="c4958-103">Imports an API from a file or a URL.</span></span>

## <span data-ttu-id="c4958-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c4958-104">SYNTAX</span></span>

### <span data-ttu-id="c4958-105">ImportFromLocalFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4958-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4958-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="c4958-106">ImportFromUrl</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4958-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c4958-107">DESCRIPTION</span></span>
<span data-ttu-id="c4958-108">Az **import-AzApiManagementApi** parancsmag egy Azure API-kezelési API-t importál egy fájlból vagy URL-címről a webalkalmazás-Leírás nyelve (WADL), a Web Services Description Language (WSDL) vagy a hencegés formátumában.</span><span class="sxs-lookup"><span data-stu-id="c4958-108">The **Import-AzApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="c4958-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c4958-109">EXAMPLES</span></span>

### <span data-ttu-id="c4958-110">Példa 1 API importálása WADL-fájlból</span><span class="sxs-lookup"><span data-stu-id="c4958-110">Example 1 Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="c4958-111">Ez a parancs az API-t a megadott WADL-fájlból importálja.</span><span class="sxs-lookup"><span data-stu-id="c4958-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="c4958-112">Példa 2 API-t egy hencegő fájlból importálja</span><span class="sxs-lookup"><span data-stu-id="c4958-112">Example 2 Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="c4958-113">A parancs az API-t a megadott hencegő fájlból importálja.</span><span class="sxs-lookup"><span data-stu-id="c4958-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="c4958-114">3. példa: API importálása WADL-hivatkozásból</span><span class="sxs-lookup"><span data-stu-id="c4958-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="c4958-115">Ez a parancs egy API-t importál a megadott WADL-hivatkozásból.</span><span class="sxs-lookup"><span data-stu-id="c4958-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="c4958-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c4958-116">PARAMETERS</span></span>

### <span data-ttu-id="c4958-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c4958-117">-ApiId</span></span>
<span data-ttu-id="c4958-118">Az importálandó API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4958-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="c4958-119">Ha nem adja meg ezt a paramétert, a rendszer azonosítót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c4958-119">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="c4958-120">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="c4958-120">-ApiRevision</span></span>
<span data-ttu-id="c4958-121">Az API-módosítás azonosítója</span><span class="sxs-lookup"><span data-stu-id="c4958-121">Identifier of API Revision.</span></span> <span data-ttu-id="c4958-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="c4958-122">This parameter is optional.</span></span> <span data-ttu-id="c4958-123">Ha nincs megadva, az Importálás a jelenleg aktív verzióra vagy egy új API-ra történik.</span><span class="sxs-lookup"><span data-stu-id="c4958-123">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="c4958-124">-ApiType</span><span class="sxs-lookup"><span data-stu-id="c4958-124">-ApiType</span></span>
<span data-ttu-id="c4958-125">Ez a paraméter nem kötelező a http alapértelmezett értékeként.</span><span class="sxs-lookup"><span data-stu-id="c4958-125">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="c4958-126">A SOAP beállítás csak akkor érvényes, ha WSDL-importálást hoz létre, és SOAP-áteresztési API-t hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c4958-126">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

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

### <span data-ttu-id="c4958-127">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c4958-127">-Context</span></span>
<span data-ttu-id="c4958-128">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="c4958-128">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4958-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4958-129">-DefaultProfile</span></span>
<span data-ttu-id="c4958-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4958-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4958-131">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="c4958-131">-Path</span></span>
<span data-ttu-id="c4958-132">A web API elérési útját adja meg az API nyilvános URL-címének utolsó részeként.</span><span class="sxs-lookup"><span data-stu-id="c4958-132">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="c4958-133">Ezt az URL-címet az API-felhasználók használják a kérések webszolgáltatás számára való elküldéséhez.</span><span class="sxs-lookup"><span data-stu-id="c4958-133">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="c4958-134">1 – 400 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="c4958-134">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="c4958-135">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="c4958-135">The default value is $Null.</span></span>

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

### <span data-ttu-id="c4958-136">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="c4958-136">-SpecificationFormat</span></span>
<span data-ttu-id="c4958-137">A specifikáció formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4958-137">Specifies the specification format.</span></span>
<span data-ttu-id="c4958-138">psdx_paramvalues Wadl, WSDL és hencegés.</span><span class="sxs-lookup"><span data-stu-id="c4958-138">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4958-139">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="c4958-139">-SpecificationPath</span></span>
<span data-ttu-id="c4958-140">A specifikáció fájlelérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4958-140">Specifies the specification file path.</span></span>

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

### <span data-ttu-id="c4958-141">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="c4958-141">-SpecificationUrl</span></span>
<span data-ttu-id="c4958-142">A specifikáció URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4958-142">Specifies the specification URL.</span></span>

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

### <span data-ttu-id="c4958-143">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="c4958-143">-WsdlEndpointName</span></span>
<span data-ttu-id="c4958-144">Az importálandó WSDL-végpont (port) helyi neve.</span><span class="sxs-lookup"><span data-stu-id="c4958-144">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="c4958-145">1 – 400 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="c4958-145">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="c4958-146">Ez a paraméter nem kötelező, és csak a WSDL importálásához szükséges.</span><span class="sxs-lookup"><span data-stu-id="c4958-146">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="c4958-147">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="c4958-147">Default value is $null.</span></span>

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

### <span data-ttu-id="c4958-148">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="c4958-148">-WsdlServiceName</span></span>
<span data-ttu-id="c4958-149">Az importálandó WSDL-szolgáltatás helyi neve.</span><span class="sxs-lookup"><span data-stu-id="c4958-149">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="c4958-150">1 – 400 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="c4958-150">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="c4958-151">Ez a paraméter nem kötelező, és csak a WSDL importálásához szükséges.</span><span class="sxs-lookup"><span data-stu-id="c4958-151">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="c4958-152">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="c4958-152">Default value is $null.</span></span>

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

### <span data-ttu-id="c4958-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4958-153">CommonParameters</span></span>
<span data-ttu-id="c4958-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c4958-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4958-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4958-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4958-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4958-156">INPUTS</span></span>

### <span data-ttu-id="c4958-157">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c4958-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c4958-158">System. String</span><span class="sxs-lookup"><span data-stu-id="c4958-158">System.String</span></span>

### <span data-ttu-id="c4958-159">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="c4958-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="c4958-160">System. nulla ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementApiType, Microsoft. Azure. PowerShell. parancsmagok. ApiManagement. ServiceManagement, Version = 1.0.0.0, = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c4958-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c4958-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4958-161">OUTPUTS</span></span>

### <span data-ttu-id="c4958-162">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c4958-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="c4958-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c4958-163">NOTES</span></span>

## <span data-ttu-id="c4958-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4958-164">RELATED LINKS</span></span>

[<span data-ttu-id="c4958-165">Exportálás – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c4958-165">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="c4958-166">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c4958-166">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="c4958-167">Új – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c4958-167">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="c4958-168">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c4958-168">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="c4958-169">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c4958-169">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


