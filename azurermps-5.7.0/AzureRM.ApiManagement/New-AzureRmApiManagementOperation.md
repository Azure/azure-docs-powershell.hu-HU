---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
ms.openlocfilehash: 36560b23d9108ff1f8cd981abdb44a3c24f25402
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492421"
---
# <span data-ttu-id="26320-101">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="26320-101">New-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="26320-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="26320-102">SYNOPSIS</span></span>
<span data-ttu-id="26320-103">API-kezelési műveletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="26320-103">Creates an API management operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26320-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="26320-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-OperationId <String>]
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26320-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="26320-105">DESCRIPTION</span></span>
<span data-ttu-id="26320-106">A **New-AzureRmApiManagementOperation** parancsmag API-műveletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="26320-106">The **New-AzureRmApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="26320-107">Példák</span><span class="sxs-lookup"><span data-stu-id="26320-107">EXAMPLES</span></span>

### <span data-ttu-id="26320-108">Példa 1: API-kezelési művelet létrehozása</span><span class="sxs-lookup"><span data-stu-id="26320-108">Example 1: Create an API management operation</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="26320-109">Ez a parancs API-kezelési műveletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="26320-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="26320-110">2. példa: API-kezelési művelet létrehozása a kérés és válasz részleteivel</span><span class="sxs-lookup"><span data-stu-id="26320-110">Example 2: Create an API management operation with request and response details</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
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
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "01234567890" -Name 'Create/update resource' -Method 'PUT' -UrlTemplate '/resource/{rid}?q={query}' -Description "Use this operation to create new or update existing resource" -TemplateParameters @($rid, $query) -Request $Request -Responses @($response)
```

<span data-ttu-id="26320-111">Ez a példa API-kezelési műveletet hoz létre a kérés és válasz részleteivel.</span><span class="sxs-lookup"><span data-stu-id="26320-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="26320-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="26320-112">PARAMETERS</span></span>

### <span data-ttu-id="26320-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="26320-113">-ApiId</span></span>
<span data-ttu-id="26320-114">Az API-kezelési művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="26320-114">Specifies the identifier of the API management operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26320-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="26320-115">-Context</span></span>
<span data-ttu-id="26320-116">A **PsApiManagementContext** objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="26320-116">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="26320-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26320-117">-DefaultProfile</span></span>
<span data-ttu-id="26320-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26320-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="26320-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="26320-119">-Description</span></span>
<span data-ttu-id="26320-120">Az új API-művelet leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="26320-120">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="26320-121">-Módszer</span><span class="sxs-lookup"><span data-stu-id="26320-121">-Method</span></span>
<span data-ttu-id="26320-122">Az új API-kezelési művelet HTTP-metódusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="26320-122">Specifies the HTTP method of the new API management operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26320-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="26320-123">-Name</span></span>
<span data-ttu-id="26320-124">Az új API-kezelési művelet megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26320-124">Specifies the display name of new API management operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26320-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="26320-125">-OperationId</span></span>
<span data-ttu-id="26320-126">Az API-kezelési művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="26320-126">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="26320-127">-Request (kérés)</span><span class="sxs-lookup"><span data-stu-id="26320-127">-Request</span></span>
<span data-ttu-id="26320-128">Az API-kezelési művelet részleteit adja meg.</span><span class="sxs-lookup"><span data-stu-id="26320-128">Specifies the details of the API management operation.</span></span>

```yaml
Type: PsApiManagementRequest
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26320-129">– Válaszok</span><span class="sxs-lookup"><span data-stu-id="26320-129">-Responses</span></span>
<span data-ttu-id="26320-130">A lehetséges API-kezelési műveletek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26320-130">Specifies an array of possible API management operation responses.</span></span>

```yaml
Type: PsApiManagementResponse[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26320-131">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="26320-131">-TemplateParameters</span></span>
<span data-ttu-id="26320-132">Az *UrlTemplate* paraméterben megadott paraméterek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26320-132">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="26320-133">Ha nem adja meg ezt a paramétert, akkor a *UrlTemplate* alapuló alapértelmezett érték jön létre.</span><span class="sxs-lookup"><span data-stu-id="26320-133">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

```yaml
Type: PsApiManagementParameter[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26320-134">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="26320-134">-UrlTemplate</span></span>
<span data-ttu-id="26320-135">Az URL-sablon megadása</span><span class="sxs-lookup"><span data-stu-id="26320-135">Specifies the URL template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26320-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26320-136">CommonParameters</span></span>
<span data-ttu-id="26320-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="26320-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26320-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26320-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26320-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="26320-139">INPUTS</span></span>

### <span data-ttu-id="26320-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="26320-140">None</span></span>
<span data-ttu-id="26320-141">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="26320-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="26320-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26320-142">OUTPUTS</span></span>

### <span data-ttu-id="26320-143">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="26320-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="26320-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="26320-144">NOTES</span></span>

## <span data-ttu-id="26320-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26320-145">RELATED LINKS</span></span>

[<span data-ttu-id="26320-146">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="26320-146">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="26320-147">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="26320-147">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="26320-148">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="26320-148">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


