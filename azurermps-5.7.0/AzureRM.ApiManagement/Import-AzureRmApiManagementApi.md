---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/import-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
ms.openlocfilehash: 5e00f3718b093f3112839ebb331fc96984a03038
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680207"
---
# <span data-ttu-id="1a827-101">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1a827-101">Import-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="1a827-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1a827-102">SYNOPSIS</span></span>
<span data-ttu-id="1a827-103">API-t importál egy fájlból vagy URL-címről.</span><span class="sxs-lookup"><span data-stu-id="1a827-103">Imports an API from a file or a URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a827-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1a827-104">SYNTAX</span></span>

### <span data-ttu-id="1a827-105">ImportFromLocalFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1a827-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a827-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="1a827-106">ImportFromUrl</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a827-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1a827-107">DESCRIPTION</span></span>
<span data-ttu-id="1a827-108">Az **import-AzureRmApiManagementApi** parancsmag egy Azure API-kezelési API-t importál egy fájlból vagy URL-címről a webalkalmazás-Leírás nyelve (WADL), a Web Services Description Language (WSDL) vagy a hencegés formátumában.</span><span class="sxs-lookup"><span data-stu-id="1a827-108">The **Import-AzureRmApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="1a827-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1a827-109">EXAMPLES</span></span>

### <span data-ttu-id="1a827-110">Példa 1 API importálása WADL-fájlból</span><span class="sxs-lookup"><span data-stu-id="1a827-110">Example 1 Import an API from a WADL file</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="1a827-111">Ez a parancs az API-t a megadott WADL-fájlból importálja.</span><span class="sxs-lookup"><span data-stu-id="1a827-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="1a827-112">Példa 2 API-t egy hencegő fájlból importálja</span><span class="sxs-lookup"><span data-stu-id="1a827-112">Example 2 Import an API from a Swagger file</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="1a827-113">A parancs az API-t a megadott hencegő fájlból importálja.</span><span class="sxs-lookup"><span data-stu-id="1a827-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="1a827-114">3. példa: API importálása WADL-hivatkozásból</span><span class="sxs-lookup"><span data-stu-id="1a827-114">Example 3: Import an API from a WADL link</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="1a827-115">Ez a parancs egy API-t importál a megadott WADL-hivatkozásból.</span><span class="sxs-lookup"><span data-stu-id="1a827-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="1a827-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1a827-116">PARAMETERS</span></span>

### <span data-ttu-id="1a827-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1a827-117">-ApiId</span></span>
<span data-ttu-id="1a827-118">Az importálandó API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1a827-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="1a827-119">Ha nem adja meg ezt a paramétert, a rendszer azonosítót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1a827-119">If you do not specify this parameter, an ID is generated for you.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a827-120">-ApiType</span><span class="sxs-lookup"><span data-stu-id="1a827-120">-ApiType</span></span>
<span data-ttu-id="1a827-121">Ez a paraméter nem kötelező a http alapértelmezett értékeként.</span><span class="sxs-lookup"><span data-stu-id="1a827-121">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="1a827-122">A SOAP beállítás csak akkor érvényes, ha WSDL-importálást hoz létre, és SOAP-áteresztési API-t hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1a827-122">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

```yaml
Type: PsApiManagementApiType
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a827-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="1a827-123">-Context</span></span>
<span data-ttu-id="1a827-124">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="1a827-124">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a827-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a827-125">-DefaultProfile</span></span>
<span data-ttu-id="1a827-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1a827-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a827-127">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="1a827-127">-Path</span></span>
<span data-ttu-id="1a827-128">A web API elérési útját adja meg az API nyilvános URL-címének utolsó részeként.</span><span class="sxs-lookup"><span data-stu-id="1a827-128">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="1a827-129">Ezt az URL-címet az API-felhasználók használják a kérések webszolgáltatás számára való elküldéséhez.</span><span class="sxs-lookup"><span data-stu-id="1a827-129">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="1a827-130">1 – 400 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="1a827-130">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="1a827-131">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="1a827-131">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a827-132">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="1a827-132">-SpecificationFormat</span></span>
<span data-ttu-id="1a827-133">A specifikáció formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1a827-133">Specifies the specification format.</span></span>
<span data-ttu-id="1a827-134">psdx_paramvalues Wadl, WSDL és hencegés.</span><span class="sxs-lookup"><span data-stu-id="1a827-134">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: PsApiManagementApiFormat
Parameter Sets: (All)
Aliases: 
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a827-135">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="1a827-135">-SpecificationPath</span></span>
<span data-ttu-id="1a827-136">A specifikáció fájlelérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1a827-136">Specifies the specification file path.</span></span>

```yaml
Type: String
Parameter Sets: ImportFromLocalFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a827-137">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="1a827-137">-SpecificationUrl</span></span>
<span data-ttu-id="1a827-138">A specifikáció URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1a827-138">Specifies the specification URL.</span></span>

```yaml
Type: String
Parameter Sets: ImportFromUrl
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a827-139">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="1a827-139">-WsdlEndpointName</span></span>
<span data-ttu-id="1a827-140">Az importálandó WSDL-végpont (port) helyi neve.</span><span class="sxs-lookup"><span data-stu-id="1a827-140">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="1a827-141">1 – 400 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="1a827-141">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="1a827-142">Ez a paraméter nem kötelező, és csak a WSDL importálásához szükséges.</span><span class="sxs-lookup"><span data-stu-id="1a827-142">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="1a827-143">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="1a827-143">Default value is $null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a827-144">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="1a827-144">-WsdlServiceName</span></span>
<span data-ttu-id="1a827-145">Az importálandó WSDL-szolgáltatás helyi neve.</span><span class="sxs-lookup"><span data-stu-id="1a827-145">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="1a827-146">1 – 400 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="1a827-146">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="1a827-147">Ez a paraméter nem kötelező, és csak a WSDL importálásához szükséges.</span><span class="sxs-lookup"><span data-stu-id="1a827-147">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="1a827-148">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="1a827-148">Default value is $null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a827-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a827-149">CommonParameters</span></span>
<span data-ttu-id="1a827-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1a827-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a827-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a827-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a827-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a827-152">INPUTS</span></span>

### <span data-ttu-id="1a827-153">Nincs</span><span class="sxs-lookup"><span data-stu-id="1a827-153">None</span></span>
<span data-ttu-id="1a827-154">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="1a827-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1a827-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a827-155">OUTPUTS</span></span>

### <span data-ttu-id="1a827-156">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1a827-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="1a827-157">Ez a parancsmag az importált API **PsApiManagementApi** -objektumként való értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="1a827-157">This cmdlet returns the imported API as a **PsApiManagementApi** object.</span></span>

## <span data-ttu-id="1a827-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1a827-158">NOTES</span></span>

## <span data-ttu-id="1a827-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1a827-159">RELATED LINKS</span></span>

[<span data-ttu-id="1a827-160">Exportálás – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1a827-160">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="1a827-161">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1a827-161">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="1a827-162">Új – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1a827-162">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="1a827-163">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1a827-163">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="1a827-164">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1a827-164">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


