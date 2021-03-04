---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
ms.openlocfilehash: 44eb7ef52782f6a00a81385f7b1a87b0292bec33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922545"
---
# <span data-ttu-id="82113-101">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="82113-101">New-AzApiManagementOperation</span></span>

## <span data-ttu-id="82113-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82113-102">SYNOPSIS</span></span>
<span data-ttu-id="82113-103">API-kezelési műveletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="82113-103">Creates an API management operation.</span></span>

## <span data-ttu-id="82113-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="82113-104">SYNTAX</span></span>

```
New-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-OperationId <String>] -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82113-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="82113-105">DESCRIPTION</span></span>
<span data-ttu-id="82113-106">A **New-AzApiManagementOperation parancsmag API-műveletet** hoz létre.</span><span class="sxs-lookup"><span data-stu-id="82113-106">The **New-AzApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="82113-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="82113-107">EXAMPLES</span></span>

### <span data-ttu-id="82113-108">1. példa: API-kezelési művelet létrehozása</span><span class="sxs-lookup"><span data-stu-id="82113-108">Example 1: Create an API management operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="82113-109">Ez a parancs API-kezelési műveletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="82113-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="82113-110">2. példa: API-kezelési művelet létrehozása a kérelem és a válasz részleteivel</span><span class="sxs-lookup"><span data-stu-id="82113-110">Example 2: Create an API management operation with request and response details</span></span>
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

<span data-ttu-id="82113-111">Ez a példa létrehoz egy API-kezelési műveletet a kérelem és a válasz részleteivel.</span><span class="sxs-lookup"><span data-stu-id="82113-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="82113-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82113-112">PARAMETERS</span></span>

### <span data-ttu-id="82113-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="82113-113">-ApiId</span></span>
<span data-ttu-id="82113-114">Az API-kezelési művelet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="82113-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="82113-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="82113-115">-ApiRevision</span></span>
<span data-ttu-id="82113-116">Az API-változat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="82113-116">Identifier of API Revision.</span></span> <span data-ttu-id="82113-117">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="82113-117">This parameter is optional.</span></span> <span data-ttu-id="82113-118">Ha nincs megadva, a művelet az aktuálisan aktív API-változathoz lesz csatolva.</span><span class="sxs-lookup"><span data-stu-id="82113-118">If not specified, the operation will be attached to the currently active api revision.</span></span>

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

### <span data-ttu-id="82113-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="82113-119">-Context</span></span>
<span data-ttu-id="82113-120">A **PsApiManagementContext** objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="82113-120">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="82113-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82113-121">-DefaultProfile</span></span>
<span data-ttu-id="82113-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82113-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82113-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="82113-123">-Description</span></span>
<span data-ttu-id="82113-124">Az új API-művelet leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="82113-124">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="82113-125">-Method</span><span class="sxs-lookup"><span data-stu-id="82113-125">-Method</span></span>
<span data-ttu-id="82113-126">Az új API-kezelési művelet HTTP-metódusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="82113-126">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="82113-127">-Name</span><span class="sxs-lookup"><span data-stu-id="82113-127">-Name</span></span>
<span data-ttu-id="82113-128">Az új API-kezelési művelet megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="82113-128">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="82113-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="82113-129">-OperationId</span></span>
<span data-ttu-id="82113-130">Az API-kezelési művelet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="82113-130">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="82113-131">-Request</span><span class="sxs-lookup"><span data-stu-id="82113-131">-Request</span></span>
<span data-ttu-id="82113-132">Az API-kezelési művelet részleteit adja meg.</span><span class="sxs-lookup"><span data-stu-id="82113-132">Specifies the details of the API management operation.</span></span>

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

### <span data-ttu-id="82113-133">-Válaszok</span><span class="sxs-lookup"><span data-stu-id="82113-133">-Responses</span></span>
<span data-ttu-id="82113-134">A lehetséges API-kezelési műveletekre adott válaszok tömbje.</span><span class="sxs-lookup"><span data-stu-id="82113-134">Specifies an array of possible API management operation responses.</span></span>

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

### <span data-ttu-id="82113-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="82113-135">-TemplateParameters</span></span>
<span data-ttu-id="82113-136">Az *UrlTemplate* paraméterben definiált paraméterek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="82113-136">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="82113-137">Ha nem adja meg ezt a paramétert, a rendszer létrehoz egy alapértelmezett értéket az *UrlTemplate mező alapján.*</span><span class="sxs-lookup"><span data-stu-id="82113-137">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

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

### <span data-ttu-id="82113-138">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="82113-138">-UrlTemplate</span></span>
<span data-ttu-id="82113-139">Megadja az URL-sablont.</span><span class="sxs-lookup"><span data-stu-id="82113-139">Specifies the URL template.</span></span>

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

### <span data-ttu-id="82113-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82113-140">CommonParameters</span></span>
<span data-ttu-id="82113-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82113-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82113-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82113-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82113-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82113-143">INPUTS</span></span>

### <span data-ttu-id="82113-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="82113-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="82113-145">System.String</span><span class="sxs-lookup"><span data-stu-id="82113-145">System.String</span></span>

### <span data-ttu-id="82113-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span><span class="sxs-lookup"><span data-stu-id="82113-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="82113-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="82113-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="82113-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span><span class="sxs-lookup"><span data-stu-id="82113-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

## <span data-ttu-id="82113-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82113-149">OUTPUTS</span></span>

### <span data-ttu-id="82113-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="82113-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="82113-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="82113-151">NOTES</span></span>

## <span data-ttu-id="82113-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82113-152">RELATED LINKS</span></span>

[<span data-ttu-id="82113-153">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="82113-153">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="82113-154">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="82113-154">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="82113-155">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="82113-155">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


