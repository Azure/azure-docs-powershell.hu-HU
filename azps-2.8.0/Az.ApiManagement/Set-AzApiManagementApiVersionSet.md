---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: a29713e91027ee6ca6e3cbc6390d63829fbb612c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667948"
---
# <span data-ttu-id="1235c-101">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1235c-101">Set-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="1235c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1235c-102">SYNOPSIS</span></span>
<span data-ttu-id="1235c-103">Frissít egy API-verziót az API-kezelés kontextusában.</span><span class="sxs-lookup"><span data-stu-id="1235c-103">Updates an API Version Set in the API Management Context.</span></span>

## <span data-ttu-id="1235c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1235c-104">SYNTAX</span></span>

### <span data-ttu-id="1235c-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1235c-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1235c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1235c-106">ByInputObject</span></span>
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1235c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1235c-107">DESCRIPTION</span></span>

<span data-ttu-id="1235c-108">A **set-AzApiManagementApiVersionSet** parancsmag módosította az Azure API Management API-készletét.</span><span class="sxs-lookup"><span data-stu-id="1235c-108">The **Set-AzApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="1235c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1235c-109">EXAMPLES</span></span>

### <span data-ttu-id="1235c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1235c-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="1235c-111">A parancs frissíti a verziószámozási sémával `Header` és a fejléc paraméterrel beállított API-verziót `api-version` .</span><span class="sxs-lookup"><span data-stu-id="1235c-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="1235c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1235c-112">PARAMETERS</span></span>

### <span data-ttu-id="1235c-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="1235c-113">-ApiVersionSetId</span></span>
<span data-ttu-id="1235c-114">Az új API-verzió azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1235c-114">Identifier for new API Version Set.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1235c-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="1235c-115">-Context</span></span>
<span data-ttu-id="1235c-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="1235c-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1235c-117">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="1235c-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1235c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1235c-118">-DefaultProfile</span></span>
<span data-ttu-id="1235c-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1235c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1235c-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="1235c-120">-Description</span></span>
<span data-ttu-id="1235c-121">Az API-verzió készletének leírása.</span><span class="sxs-lookup"><span data-stu-id="1235c-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="1235c-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="1235c-122">-HeaderName</span></span>
<span data-ttu-id="1235c-123">A verziószámozási információkat tartalmazó fejléc értéke.</span><span class="sxs-lookup"><span data-stu-id="1235c-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="1235c-124">Ha a verziószámozási séma FEJLÉCe van kiválasztva, akkor ezt az értéket kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="1235c-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="1235c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1235c-125">-InputObject</span></span>
<span data-ttu-id="1235c-126">A PsApiManagementApiVersionSet példánya.</span><span class="sxs-lookup"><span data-stu-id="1235c-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="1235c-127">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="1235c-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1235c-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1235c-128">-Name</span></span>
<span data-ttu-id="1235c-129">A ApiVersion neve.</span><span class="sxs-lookup"><span data-stu-id="1235c-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="1235c-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1235c-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="1235c-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1235c-131">-PassThru</span></span>
<span data-ttu-id="1235c-132">Ha meg van adva a Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiVersionSet típusa, amely a módosított apiVersionSet jeleníti meg, a program a kimenetre ír.</span><span class="sxs-lookup"><span data-stu-id="1235c-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

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

### <span data-ttu-id="1235c-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="1235c-133">-QueryName</span></span>
<span data-ttu-id="1235c-134">A lekérdezési érték, amely a verziószámozási információkat fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="1235c-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="1235c-135">Ha a verziószámozási séma lekérdezése van kiválasztva, akkor ezt az értéket kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="1235c-135">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="1235c-136">-Scheme (séma)</span><span class="sxs-lookup"><span data-stu-id="1235c-136">-Scheme</span></span>
<span data-ttu-id="1235c-137">Verziószámozási séma az API verziószámozási készletének kiválasztásához.</span><span class="sxs-lookup"><span data-stu-id="1235c-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="1235c-138">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1235c-138">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1235c-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1235c-139">-Confirm</span></span>
<span data-ttu-id="1235c-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1235c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1235c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1235c-141">-WhatIf</span></span>
<span data-ttu-id="1235c-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1235c-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1235c-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1235c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1235c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1235c-144">CommonParameters</span></span>
<span data-ttu-id="1235c-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1235c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1235c-146">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1235c-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1235c-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1235c-147">INPUTS</span></span>

### <span data-ttu-id="1235c-148">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1235c-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1235c-149">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1235c-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="1235c-150">System. String</span><span class="sxs-lookup"><span data-stu-id="1235c-150">System.String</span></span>

### <span data-ttu-id="1235c-151">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="1235c-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="1235c-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1235c-152">OUTPUTS</span></span>

### <span data-ttu-id="1235c-153">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1235c-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="1235c-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1235c-154">NOTES</span></span>

## <span data-ttu-id="1235c-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1235c-155">RELATED LINKS</span></span>

[<span data-ttu-id="1235c-156">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1235c-156">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="1235c-157">Új – AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1235c-157">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="1235c-158">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1235c-158">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
