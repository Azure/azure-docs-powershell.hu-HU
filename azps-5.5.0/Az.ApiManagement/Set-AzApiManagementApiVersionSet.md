---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: d85d480adc5d6c588c7da2f03c514258dc96a9e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205614"
---
# <span data-ttu-id="b99f8-101">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b99f8-101">Set-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="b99f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b99f8-102">SYNOPSIS</span></span>
<span data-ttu-id="b99f8-103">Frissíti az API-verziókészletet az API-kezelési környezetben.</span><span class="sxs-lookup"><span data-stu-id="b99f8-103">Updates an API Version Set in the API Management Context.</span></span>

## <span data-ttu-id="b99f8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b99f8-104">SYNTAX</span></span>

### <span data-ttu-id="b99f8-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b99f8-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b99f8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b99f8-106">ByInputObject</span></span>
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b99f8-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b99f8-107">DESCRIPTION</span></span>

<span data-ttu-id="b99f8-108">A **Set-AzApiManagementApiVersionSet** parancsmag módosítja az Azure API Management API verziókészletét.</span><span class="sxs-lookup"><span data-stu-id="b99f8-108">The **Set-AzApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="b99f8-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b99f8-109">EXAMPLES</span></span>

### <span data-ttu-id="b99f8-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="b99f8-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="b99f8-111">Ez a parancs frissíti a meglévő, verziószámozási sémát és fejléc paramétert használó `Header` API-verziókészletet. `api-version`</span><span class="sxs-lookup"><span data-stu-id="b99f8-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="b99f8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b99f8-112">PARAMETERS</span></span>

### <span data-ttu-id="b99f8-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="b99f8-113">-ApiVersionSetId</span></span>
<span data-ttu-id="b99f8-114">Az új API-verziókészlet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b99f8-114">Identifier for new API Version Set.</span></span>

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

### <span data-ttu-id="b99f8-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b99f8-115">-Context</span></span>
<span data-ttu-id="b99f8-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="b99f8-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b99f8-117">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="b99f8-117">This parameter is required.</span></span>

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

### <span data-ttu-id="b99f8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b99f8-118">-DefaultProfile</span></span>
<span data-ttu-id="b99f8-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b99f8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b99f8-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="b99f8-120">-Description</span></span>
<span data-ttu-id="b99f8-121">Az Api-verziókészlet leírása.</span><span class="sxs-lookup"><span data-stu-id="b99f8-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="b99f8-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="b99f8-122">-HeaderName</span></span>
<span data-ttu-id="b99f8-123">A verziószámozási adatokat tartalmazó fejlécérték.</span><span class="sxs-lookup"><span data-stu-id="b99f8-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="b99f8-124">Ha a verziószámozási séma FEJLÉCe van kiválasztva, ezt az értéket kell megadni.</span><span class="sxs-lookup"><span data-stu-id="b99f8-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="b99f8-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b99f8-125">-InputObject</span></span>
<span data-ttu-id="b99f8-126">A PsApiManagementApiVersionSet példánya.</span><span class="sxs-lookup"><span data-stu-id="b99f8-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="b99f8-127">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="b99f8-127">This parameter is required.</span></span>

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

### <span data-ttu-id="b99f8-128">-Name</span><span class="sxs-lookup"><span data-stu-id="b99f8-128">-Name</span></span>
<span data-ttu-id="b99f8-129">Az ApiVersion-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="b99f8-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="b99f8-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b99f8-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="b99f8-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b99f8-131">-PassThru</span></span>
<span data-ttu-id="b99f8-132">Ha ez meg van adva, akkor a módosított apiVersionSet-et képviselő Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet típust a program kimenetre írja.</span><span class="sxs-lookup"><span data-stu-id="b99f8-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

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

### <span data-ttu-id="b99f8-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="b99f8-133">-QueryName</span></span>
<span data-ttu-id="b99f8-134">A verziószámozási adatokat tartalmazó Lekérdezés érték.</span><span class="sxs-lookup"><span data-stu-id="b99f8-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="b99f8-135">Ha a verziószámozási sémalekérdezés van kiválasztva, akkor ezt az értéket kell megadni.</span><span class="sxs-lookup"><span data-stu-id="b99f8-135">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="b99f8-136">-Scheme</span><span class="sxs-lookup"><span data-stu-id="b99f8-136">-Scheme</span></span>
<span data-ttu-id="b99f8-137">Verziószámozási séma az Api verziókészlethez való kiválasztásához.</span><span class="sxs-lookup"><span data-stu-id="b99f8-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="b99f8-138">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b99f8-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="b99f8-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b99f8-139">-Confirm</span></span>
<span data-ttu-id="b99f8-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b99f8-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b99f8-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b99f8-141">-WhatIf</span></span>
<span data-ttu-id="b99f8-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b99f8-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b99f8-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b99f8-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b99f8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b99f8-144">CommonParameters</span></span>
<span data-ttu-id="b99f8-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b99f8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b99f8-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b99f8-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b99f8-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b99f8-147">INPUTS</span></span>

### <span data-ttu-id="b99f8-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b99f8-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b99f8-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b99f8-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="b99f8-150">System.String</span><span class="sxs-lookup"><span data-stu-id="b99f8-150">System.String</span></span>

### <span data-ttu-id="b99f8-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="b99f8-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="b99f8-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b99f8-152">OUTPUTS</span></span>

### <span data-ttu-id="b99f8-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b99f8-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="b99f8-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b99f8-154">NOTES</span></span>

## <span data-ttu-id="b99f8-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b99f8-155">RELATED LINKS</span></span>

[<span data-ttu-id="b99f8-156">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b99f8-156">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="b99f8-157">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b99f8-157">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="b99f8-158">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b99f8-158">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
