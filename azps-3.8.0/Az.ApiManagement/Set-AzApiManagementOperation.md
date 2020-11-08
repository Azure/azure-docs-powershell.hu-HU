---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
ms.openlocfilehash: 92848cb2daa0976d8206549fc16d1a6f039199a6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014178"
---
# <span data-ttu-id="dca5a-101">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="dca5a-101">Set-AzApiManagementOperation</span></span>

## <span data-ttu-id="dca5a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dca5a-102">SYNOPSIS</span></span>
<span data-ttu-id="dca5a-103">Az API-műveletek részleteit határozza meg.</span><span class="sxs-lookup"><span data-stu-id="dca5a-103">Sets API operation details.</span></span>

## <span data-ttu-id="dca5a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dca5a-104">SYNTAX</span></span>

```
Set-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dca5a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dca5a-105">DESCRIPTION</span></span>
<span data-ttu-id="dca5a-106">A **set-AzApiManagementOperation** PARANCSMAG az API-műveletek részleteit állítja be.</span><span class="sxs-lookup"><span data-stu-id="dca5a-106">The **Set-AzApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="dca5a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dca5a-107">EXAMPLES</span></span>

### <span data-ttu-id="dca5a-108">Példa 1: a művelet részleteinek beállítása</span><span class="sxs-lookup"><span data-stu-id="dca5a-108">Example 1: Set the operation details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="dca5a-109">Ez a parancs beállítja az API-kezelés működésének részleteit.</span><span class="sxs-lookup"><span data-stu-id="dca5a-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="dca5a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dca5a-110">PARAMETERS</span></span>

### <span data-ttu-id="dca5a-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="dca5a-111">-ApiId</span></span>
<span data-ttu-id="dca5a-112">Az API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dca5a-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="dca5a-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="dca5a-113">-ApiRevision</span></span>
<span data-ttu-id="dca5a-114">Az API-módosítás azonosítója</span><span class="sxs-lookup"><span data-stu-id="dca5a-114">Identifier of API Revision.</span></span> <span data-ttu-id="dca5a-115">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="dca5a-115">This parameter is optional.</span></span> <span data-ttu-id="dca5a-116">Ha nem adja meg, akkor a művelet a jelenleg aktív API-verzióban lesz frissítve.</span><span class="sxs-lookup"><span data-stu-id="dca5a-116">If not specified, the operation will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="dca5a-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="dca5a-117">-Context</span></span>
<span data-ttu-id="dca5a-118">A **PsApiManagementContext** példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dca5a-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="dca5a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dca5a-119">-DefaultProfile</span></span>
<span data-ttu-id="dca5a-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dca5a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dca5a-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="dca5a-121">-Description</span></span>
<span data-ttu-id="dca5a-122">Az új művelet leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="dca5a-122">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="dca5a-123">-Módszer</span><span class="sxs-lookup"><span data-stu-id="dca5a-123">-Method</span></span>
<span data-ttu-id="dca5a-124">Az új művelet HTTP-metódusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dca5a-124">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="dca5a-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dca5a-125">-Name</span></span>
<span data-ttu-id="dca5a-126">Az új művelet megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dca5a-126">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="dca5a-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="dca5a-127">-OperationId</span></span>
<span data-ttu-id="dca5a-128">A meglévő művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dca5a-128">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="dca5a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dca5a-129">-PassThru</span></span>
<span data-ttu-id="dca5a-130">passthru</span><span class="sxs-lookup"><span data-stu-id="dca5a-130">passthru</span></span>

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

### <span data-ttu-id="dca5a-131">-Request (kérés)</span><span class="sxs-lookup"><span data-stu-id="dca5a-131">-Request</span></span>
<span data-ttu-id="dca5a-132">A műveleti kérés részleteit adja meg.</span><span class="sxs-lookup"><span data-stu-id="dca5a-132">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="dca5a-133">– Válaszok</span><span class="sxs-lookup"><span data-stu-id="dca5a-133">-Responses</span></span>
<span data-ttu-id="dca5a-134">A lehetséges műveletekre adott válaszok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dca5a-134">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="dca5a-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="dca5a-135">-TemplateParameters</span></span>
<span data-ttu-id="dca5a-136">Az *UrlTemplate* paraméterben megadott tömböt vagy paramétereket adja meg.</span><span class="sxs-lookup"><span data-stu-id="dca5a-136">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="dca5a-137">Ha nem ad meg egy értéket, az alapértelmezett érték a UrlTemplate alapján jön létre.</span><span class="sxs-lookup"><span data-stu-id="dca5a-137">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="dca5a-138">A paraméter segítségével további részleteket adhat a paraméterekről, például a leírásról, a típusról és más lehetséges értékekről.</span><span class="sxs-lookup"><span data-stu-id="dca5a-138">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="dca5a-139">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="dca5a-139">-UrlTemplate</span></span>
<span data-ttu-id="dca5a-140">Az URL-sablon megadása</span><span class="sxs-lookup"><span data-stu-id="dca5a-140">Specifies the URL template.</span></span>
<span data-ttu-id="dca5a-141">Például: vevők/{CID}/rendelések/{OID}/? Date = {Date}.</span><span class="sxs-lookup"><span data-stu-id="dca5a-141">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="dca5a-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dca5a-142">-Confirm</span></span>
<span data-ttu-id="dca5a-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dca5a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dca5a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dca5a-144">-WhatIf</span></span>
<span data-ttu-id="dca5a-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dca5a-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dca5a-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dca5a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dca5a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dca5a-147">CommonParameters</span></span>
<span data-ttu-id="dca5a-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dca5a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dca5a-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dca5a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dca5a-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dca5a-150">INPUTS</span></span>

### <span data-ttu-id="dca5a-151">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dca5a-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dca5a-152">System. String</span><span class="sxs-lookup"><span data-stu-id="dca5a-152">System.String</span></span>

### <span data-ttu-id="dca5a-153">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementParameter []</span><span class="sxs-lookup"><span data-stu-id="dca5a-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="dca5a-154">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="dca5a-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="dca5a-155">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementResponse []</span><span class="sxs-lookup"><span data-stu-id="dca5a-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

### <span data-ttu-id="dca5a-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dca5a-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dca5a-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dca5a-157">OUTPUTS</span></span>

### <span data-ttu-id="dca5a-158">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="dca5a-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="dca5a-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dca5a-159">NOTES</span></span>

## <span data-ttu-id="dca5a-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dca5a-160">RELATED LINKS</span></span>

[<span data-ttu-id="dca5a-161">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="dca5a-161">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="dca5a-162">Új – AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="dca5a-162">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="dca5a-163">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="dca5a-163">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)


