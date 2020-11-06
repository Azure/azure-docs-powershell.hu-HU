---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: e50e912c55a09ef5d036bee668bc45f58fc42c19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492915"
---
# <span data-ttu-id="e501b-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e501b-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="e501b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e501b-102">SYNOPSIS</span></span>
<span data-ttu-id="e501b-103">Az API-műveletek részleteit határozza meg.</span><span class="sxs-lookup"><span data-stu-id="e501b-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e501b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e501b-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e501b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e501b-105">DESCRIPTION</span></span>
<span data-ttu-id="e501b-106">A **set-AzureRmApiManagementOperation** PARANCSMAG az API-műveletek részleteit állítja be.</span><span class="sxs-lookup"><span data-stu-id="e501b-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="e501b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e501b-107">EXAMPLES</span></span>

### <span data-ttu-id="e501b-108">Példa 1: a művelet részleteinek beállítása</span><span class="sxs-lookup"><span data-stu-id="e501b-108">Example 1: Set the operation details</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="e501b-109">Ez a parancs beállítja az API-kezelés működésének részleteit.</span><span class="sxs-lookup"><span data-stu-id="e501b-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="e501b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e501b-110">PARAMETERS</span></span>

### <span data-ttu-id="e501b-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e501b-111">-ApiId</span></span>
<span data-ttu-id="e501b-112">Az API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e501b-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="e501b-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="e501b-113">-ApiRevision</span></span>
<span data-ttu-id="e501b-114">Az API-módosítás azonosítója</span><span class="sxs-lookup"><span data-stu-id="e501b-114">Identifier of API Revision.</span></span> <span data-ttu-id="e501b-115">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="e501b-115">This parameter is optional.</span></span> <span data-ttu-id="e501b-116">Ha nem adja meg, akkor a művelet a jelenleg aktív API-verzióban lesz frissítve.</span><span class="sxs-lookup"><span data-stu-id="e501b-116">If not specified, the operation will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="e501b-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e501b-117">-Context</span></span>
<span data-ttu-id="e501b-118">A **PsApiManagementContext** példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e501b-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="e501b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e501b-119">-DefaultProfile</span></span>
<span data-ttu-id="e501b-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e501b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e501b-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="e501b-121">-Description</span></span>
<span data-ttu-id="e501b-122">Az új művelet leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="e501b-122">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="e501b-123">-Módszer</span><span class="sxs-lookup"><span data-stu-id="e501b-123">-Method</span></span>
<span data-ttu-id="e501b-124">Az új művelet HTTP-metódusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e501b-124">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="e501b-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e501b-125">-Name</span></span>
<span data-ttu-id="e501b-126">Az új művelet megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e501b-126">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="e501b-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="e501b-127">-OperationId</span></span>
<span data-ttu-id="e501b-128">A meglévő művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e501b-128">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="e501b-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e501b-129">-PassThru</span></span>
<span data-ttu-id="e501b-130">passthru</span><span class="sxs-lookup"><span data-stu-id="e501b-130">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e501b-131">-Request (kérés)</span><span class="sxs-lookup"><span data-stu-id="e501b-131">-Request</span></span>
<span data-ttu-id="e501b-132">A műveleti kérés részleteit adja meg.</span><span class="sxs-lookup"><span data-stu-id="e501b-132">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="e501b-133">– Válaszok</span><span class="sxs-lookup"><span data-stu-id="e501b-133">-Responses</span></span>
<span data-ttu-id="e501b-134">A lehetséges műveletekre adott válaszok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e501b-134">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="e501b-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="e501b-135">-TemplateParameters</span></span>
<span data-ttu-id="e501b-136">Az *UrlTemplate* paraméterben megadott tömböt vagy paramétereket adja meg.</span><span class="sxs-lookup"><span data-stu-id="e501b-136">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="e501b-137">Ha nem ad meg egy értéket, az alapértelmezett érték a UrlTemplate alapján jön létre.</span><span class="sxs-lookup"><span data-stu-id="e501b-137">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="e501b-138">A paraméter segítségével további részleteket adhat a paraméterekről, például a leírásról, a típusról és más lehetséges értékekről.</span><span class="sxs-lookup"><span data-stu-id="e501b-138">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="e501b-139">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="e501b-139">-UrlTemplate</span></span>
<span data-ttu-id="e501b-140">Az URL-sablon megadása</span><span class="sxs-lookup"><span data-stu-id="e501b-140">Specifies the URL template.</span></span>
<span data-ttu-id="e501b-141">Például: vevők/{CID}/rendelések/{OID}/? Date = {Date}.</span><span class="sxs-lookup"><span data-stu-id="e501b-141">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="e501b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e501b-142">CommonParameters</span></span>
<span data-ttu-id="e501b-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e501b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e501b-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e501b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e501b-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e501b-145">INPUTS</span></span>

### <span data-ttu-id="e501b-146">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e501b-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e501b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e501b-147">System.String</span></span>

### <span data-ttu-id="e501b-148">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementParameter []</span><span class="sxs-lookup"><span data-stu-id="e501b-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="e501b-149">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="e501b-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="e501b-150">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementResponse []</span><span class="sxs-lookup"><span data-stu-id="e501b-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

### <span data-ttu-id="e501b-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e501b-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e501b-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e501b-152">OUTPUTS</span></span>

### <span data-ttu-id="e501b-153">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e501b-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="e501b-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e501b-154">NOTES</span></span>

## <span data-ttu-id="e501b-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e501b-155">RELATED LINKS</span></span>

[<span data-ttu-id="e501b-156">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e501b-156">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="e501b-157">Új – AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e501b-157">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="e501b-158">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e501b-158">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)


