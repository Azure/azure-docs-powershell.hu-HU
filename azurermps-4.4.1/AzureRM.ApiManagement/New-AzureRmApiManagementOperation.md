---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
ms.openlocfilehash: 545c1f57d269b8cdb36e006a07c754811e0f2b04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498039"
---
# <span data-ttu-id="fb227-101">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="fb227-101">New-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="fb227-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb227-102">SYNOPSIS</span></span>
<span data-ttu-id="fb227-103">API-kezelési műveletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fb227-103">Creates an API management operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb227-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb227-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-OperationId <String>]
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb227-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb227-105">DESCRIPTION</span></span>
<span data-ttu-id="fb227-106">A **New-AzureRmApiManagementOperation** parancsmag API-műveletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fb227-106">The **New-AzureRmApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="fb227-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fb227-107">EXAMPLES</span></span>

### <span data-ttu-id="fb227-108">Példa 1: API-kezelési művelet létrehozása</span><span class="sxs-lookup"><span data-stu-id="fb227-108">Example 1: Create an API management operation</span></span>
```
PS C:\>New-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="fb227-109">Ez a parancs API-kezelési műveletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fb227-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="fb227-110">2. példa: API-kezelési művelet létrehozása a kérés és válasz részleteivel</span><span class="sxs-lookup"><span data-stu-id="fb227-110">Example 2: Create an API management operation with request and response details</span></span>
```
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
New-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "01234567890" -Name 'Create/update resource' -Method 'PUT' -UrlTemplate '/resource/{rid}?q={query}' -Description "Use this operation to create new or update existing resource" -TemplateParameters @($rid, $query) -Request $Request -Responses @($response)
```

<span data-ttu-id="fb227-111">Ez a példa API-kezelési műveletet hoz létre a kérés és válasz részleteivel.</span><span class="sxs-lookup"><span data-stu-id="fb227-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="fb227-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb227-112">PARAMETERS</span></span>

### <span data-ttu-id="fb227-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fb227-113">-ApiId</span></span>
<span data-ttu-id="fb227-114">Az API-kezelési művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb227-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="fb227-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="fb227-115">-Context</span></span>
<span data-ttu-id="fb227-116">A **PsApiManagementContext** objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb227-116">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fb227-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="fb227-117">-Description</span></span>
<span data-ttu-id="fb227-118">Az új API-művelet leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb227-118">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="fb227-119">-Módszer</span><span class="sxs-lookup"><span data-stu-id="fb227-119">-Method</span></span>
<span data-ttu-id="fb227-120">Az új API-kezelési művelet HTTP-metódusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb227-120">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="fb227-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fb227-121">-Name</span></span>
<span data-ttu-id="fb227-122">Az új API-kezelési művelet megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb227-122">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="fb227-123">-OperationId</span><span class="sxs-lookup"><span data-stu-id="fb227-123">-OperationId</span></span>
<span data-ttu-id="fb227-124">Az API-kezelési művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb227-124">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="fb227-125">-Request (kérés)</span><span class="sxs-lookup"><span data-stu-id="fb227-125">-Request</span></span>
<span data-ttu-id="fb227-126">Az API-kezelési művelet részleteit adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb227-126">Specifies the details of the API management operation.</span></span>

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

### <span data-ttu-id="fb227-127">– Válaszok</span><span class="sxs-lookup"><span data-stu-id="fb227-127">-Responses</span></span>
<span data-ttu-id="fb227-128">A lehetséges API-kezelési műveletek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb227-128">Specifies an array of possible API management operation responses.</span></span>

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

### <span data-ttu-id="fb227-129">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="fb227-129">-TemplateParameters</span></span>
<span data-ttu-id="fb227-130">Az *UrlTemplate* paraméterben megadott paraméterek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb227-130">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="fb227-131">Ha nem adja meg ezt a paramétert, akkor a *UrlTemplate* alapuló alapértelmezett érték jön létre.</span><span class="sxs-lookup"><span data-stu-id="fb227-131">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

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

### <span data-ttu-id="fb227-132">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="fb227-132">-UrlTemplate</span></span>
<span data-ttu-id="fb227-133">Az URL-sablon megadása</span><span class="sxs-lookup"><span data-stu-id="fb227-133">Specifies the URL template.</span></span>

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

### <span data-ttu-id="fb227-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb227-134">-DefaultProfile</span></span>
<span data-ttu-id="fb227-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb227-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb227-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb227-136">CommonParameters</span></span>
<span data-ttu-id="fb227-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb227-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb227-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb227-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb227-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb227-139">INPUTS</span></span>

## <span data-ttu-id="fb227-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb227-140">OUTPUTS</span></span>

### <span data-ttu-id="fb227-141">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="fb227-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="fb227-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb227-142">NOTES</span></span>

## <span data-ttu-id="fb227-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb227-143">RELATED LINKS</span></span>

[<span data-ttu-id="fb227-144">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="fb227-144">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="fb227-145">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="fb227-145">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="fb227-146">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="fb227-146">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


