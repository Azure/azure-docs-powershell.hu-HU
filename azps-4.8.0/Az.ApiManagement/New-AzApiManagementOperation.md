---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
ms.openlocfilehash: 3cba96c2b68a3045448aa6f6f6ccd011964c6e16
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017993"
---
# <span data-ttu-id="c0e48-101">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="c0e48-101">New-AzApiManagementOperation</span></span>

## <span data-ttu-id="c0e48-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0e48-102">SYNOPSIS</span></span>
<span data-ttu-id="c0e48-103">API-kezelési műveletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c0e48-103">Creates an API management operation.</span></span>

## <span data-ttu-id="c0e48-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0e48-104">SYNTAX</span></span>

```
New-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-OperationId <String>] -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0e48-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0e48-105">DESCRIPTION</span></span>
<span data-ttu-id="c0e48-106">A **New-AzApiManagementOperation** parancsmag API-műveletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c0e48-106">The **New-AzApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="c0e48-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c0e48-107">EXAMPLES</span></span>

### <span data-ttu-id="c0e48-108">Példa 1: API-kezelési művelet létrehozása</span><span class="sxs-lookup"><span data-stu-id="c0e48-108">Example 1: Create an API management operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="c0e48-109">Ez a parancs API-kezelési műveletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c0e48-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="c0e48-110">2. példa: API-kezelési művelet létrehozása a kérés és válasz részleteivel</span><span class="sxs-lookup"><span data-stu-id="c0e48-110">Example 2: Create an API management operation with request and response details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$RID = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$RID.Name = "RID"
$RID.Description = "Resource identifier"
$RID.Type = "string"
$Query = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$Query.Name = "query"
$Query.Description = "Query string"
$Query.Type = 'string'
$Request = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
$Request.Description = "Create/update resource request"
$DummyQp = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$DummyQp.Name = 'dummy'
$DummyQp.Type = 'string'
$DummyQp.Required = $FALSE
$Request.QueryParameters = @($DummyQp)
$Header = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$Header.Name = 'x-custom-header'
$Header.Type = 'string'
$Request.Headers = @($Header)
$RequestRepresentation = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRepresentation
$RequestRepresentation.ContentType = 'application/json'
$RequestRepresentation.Sample = '{ "propName": "propValue" }'
$Request.Representations = @($requestRepresentation)
$Response = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse
$Response.StatusCode = 204
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "01234567890" -Name 'Create/update resource' -Method 'PUT' -UrlTemplate '/resource/{rid}?q={query}' -Description "Use this operation to create new or update existing resource" -TemplateParameters @($rid, $query) -Request $Request -Responses @($response)
```

<span data-ttu-id="c0e48-111">Ez a példa API-kezelési műveletet hoz létre a kérés és válasz részleteivel.</span><span class="sxs-lookup"><span data-stu-id="c0e48-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="c0e48-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0e48-112">PARAMETERS</span></span>

### <span data-ttu-id="c0e48-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c0e48-113">-ApiId</span></span>
<span data-ttu-id="c0e48-114">Az API-kezelési művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0e48-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="c0e48-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="c0e48-115">-ApiRevision</span></span>
<span data-ttu-id="c0e48-116">Az API-módosítás azonosítója</span><span class="sxs-lookup"><span data-stu-id="c0e48-116">Identifier of API Revision.</span></span> <span data-ttu-id="c0e48-117">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="c0e48-117">This parameter is optional.</span></span> <span data-ttu-id="c0e48-118">Ha nem adja meg, akkor a művelet a jelenleg aktív API-verzióhoz lesz csatolva.</span><span class="sxs-lookup"><span data-stu-id="c0e48-118">If not specified, the operation will be attached to the currently active api revision.</span></span>

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

### <span data-ttu-id="c0e48-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c0e48-119">-Context</span></span>
<span data-ttu-id="c0e48-120">A **PsApiManagementContext** objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0e48-120">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c0e48-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0e48-121">-DefaultProfile</span></span>
<span data-ttu-id="c0e48-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0e48-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0e48-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="c0e48-123">-Description</span></span>
<span data-ttu-id="c0e48-124">Az új API-művelet leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0e48-124">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="c0e48-125">-Módszer</span><span class="sxs-lookup"><span data-stu-id="c0e48-125">-Method</span></span>
<span data-ttu-id="c0e48-126">Az új API-kezelési művelet HTTP-metódusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0e48-126">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="c0e48-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c0e48-127">-Name</span></span>
<span data-ttu-id="c0e48-128">Az új API-kezelési művelet megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0e48-128">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="c0e48-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="c0e48-129">-OperationId</span></span>
<span data-ttu-id="c0e48-130">Az API-kezelési művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0e48-130">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="c0e48-131">-Request (kérés)</span><span class="sxs-lookup"><span data-stu-id="c0e48-131">-Request</span></span>
<span data-ttu-id="c0e48-132">Az API-kezelési művelet részleteit adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0e48-132">Specifies the details of the API management operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0e48-133">– Válaszok</span><span class="sxs-lookup"><span data-stu-id="c0e48-133">-Responses</span></span>
<span data-ttu-id="c0e48-134">A lehetséges API-kezelési műveletek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0e48-134">Specifies an array of possible API management operation responses.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0e48-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="c0e48-135">-TemplateParameters</span></span>
<span data-ttu-id="c0e48-136">Az *UrlTemplate* paraméterben megadott paraméterek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0e48-136">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="c0e48-137">Ha nem adja meg ezt a paramétert, akkor a *UrlTemplate* alapuló alapértelmezett érték jön létre.</span><span class="sxs-lookup"><span data-stu-id="c0e48-137">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0e48-138">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="c0e48-138">-UrlTemplate</span></span>
<span data-ttu-id="c0e48-139">Az URL-sablon megadása</span><span class="sxs-lookup"><span data-stu-id="c0e48-139">Specifies the URL template.</span></span>

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

### <span data-ttu-id="c0e48-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0e48-140">CommonParameters</span></span>
<span data-ttu-id="c0e48-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0e48-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0e48-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c0e48-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0e48-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0e48-143">INPUTS</span></span>

### <span data-ttu-id="c0e48-144">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c0e48-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c0e48-145">System. String</span><span class="sxs-lookup"><span data-stu-id="c0e48-145">System.String</span></span>

### <span data-ttu-id="c0e48-146">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementParameter []</span><span class="sxs-lookup"><span data-stu-id="c0e48-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="c0e48-147">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="c0e48-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="c0e48-148">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementResponse []</span><span class="sxs-lookup"><span data-stu-id="c0e48-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

## <span data-ttu-id="c0e48-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0e48-149">OUTPUTS</span></span>

### <span data-ttu-id="c0e48-150">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="c0e48-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="c0e48-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0e48-151">NOTES</span></span>

## <span data-ttu-id="c0e48-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0e48-152">RELATED LINKS</span></span>

[<span data-ttu-id="c0e48-153">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="c0e48-153">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="c0e48-154">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="c0e48-154">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="c0e48-155">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="c0e48-155">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


