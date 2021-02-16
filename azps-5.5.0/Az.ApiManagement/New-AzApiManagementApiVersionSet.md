---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 0e007634659d842b0c59712a2ee191a79e1aeb58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157618"
---
# <span data-ttu-id="f3990-101">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f3990-101">New-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="f3990-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3990-102">SYNOPSIS</span></span>
<span data-ttu-id="f3990-103">Létrehoz egy API-verziókészletet.</span><span class="sxs-lookup"><span data-stu-id="f3990-103">Creates an API Version Set.</span></span>

## <span data-ttu-id="f3990-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f3990-104">SYNTAX</span></span>

```
New-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>] -Name <String>
 -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3990-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f3990-105">DESCRIPTION</span></span>
<span data-ttu-id="f3990-106">A **New-AzApiManagementApiVersionSet** parancsmag létrehoz egy API-verziókészlet-entitást az Azure API Management környezetben.</span><span class="sxs-lookup"><span data-stu-id="f3990-106">The **New-AzApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="f3990-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f3990-107">EXAMPLES</span></span>

### <span data-ttu-id="f3990-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f3990-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> New-AzApiManagementApiVersionSet -Context $ApiMgmtContext  -Name "newversion" -Scheme Header -HeaderName "x-ms-version" -Description "version by xmsversion"

ApiVersionSetId   : ea9a87cd-a699-4a75-bf7d-909846b91268
Description       : version by xmsversion
VersionQueryName  :
VersionHeaderName : x-ms-version
DisplayName       : newversion
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/ea9a87cd-a699-4a75-bf7d-909846b91268
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="f3990-109">Ez a parancs létrehoz egy API-verziókészletet, amely verziószámozási sémát és `Query` Lekérdezés paramétert hoz `api-version` létre.</span><span class="sxs-lookup"><span data-stu-id="f3990-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="f3990-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3990-110">PARAMETERS</span></span>

### <span data-ttu-id="f3990-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="f3990-111">-ApiVersionSetId</span></span>
<span data-ttu-id="f3990-112">Az új API-verziókészlet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f3990-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="f3990-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="f3990-113">This parameter is optional.</span></span>
<span data-ttu-id="f3990-114">Ha nincs megadva, a rendszer létrehoz egy azonosítót.</span><span class="sxs-lookup"><span data-stu-id="f3990-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="f3990-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f3990-115">-Context</span></span>
<span data-ttu-id="f3990-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="f3990-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f3990-117">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="f3990-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3990-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3990-118">-DefaultProfile</span></span>
<span data-ttu-id="f3990-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3990-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3990-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f3990-120">-Description</span></span>
<span data-ttu-id="f3990-121">Az Api-verziókészlet leírása.</span><span class="sxs-lookup"><span data-stu-id="f3990-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="f3990-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="f3990-122">-HeaderName</span></span>
<span data-ttu-id="f3990-123">A verziószámozási adatokat tartalmazó fejlécérték.</span><span class="sxs-lookup"><span data-stu-id="f3990-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="f3990-124">Ha a verziószámozási séma FEJLÉCe van kiválasztva, akkor ezt az értéket kell megadni.</span><span class="sxs-lookup"><span data-stu-id="f3990-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="f3990-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f3990-125">-Name</span></span>
<span data-ttu-id="f3990-126">Az ApiVersion-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="f3990-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="f3990-127">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="f3990-127">This parameter is required.</span></span>

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

### <span data-ttu-id="f3990-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="f3990-128">-QueryName</span></span>
<span data-ttu-id="f3990-129">A verziószámozási adatokat tartalmazó Lekérdezés érték.</span><span class="sxs-lookup"><span data-stu-id="f3990-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="f3990-130">Ha a verziószámozási séma lekérdezése van kiválasztva, akkor ezt az értéket kell megadni.</span><span class="sxs-lookup"><span data-stu-id="f3990-130">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="f3990-131">-Scheme</span><span class="sxs-lookup"><span data-stu-id="f3990-131">-Scheme</span></span>
<span data-ttu-id="f3990-132">Verziószámozási séma, amely kiválasztja az Api verziószámozási készletét.</span><span class="sxs-lookup"><span data-stu-id="f3990-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="f3990-133">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="f3990-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3990-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3990-134">-Confirm</span></span>
<span data-ttu-id="f3990-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f3990-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3990-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3990-136">-WhatIf</span></span>
<span data-ttu-id="f3990-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f3990-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3990-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3990-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3990-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3990-139">CommonParameters</span></span>
<span data-ttu-id="f3990-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3990-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3990-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3990-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3990-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3990-142">INPUTS</span></span>

### <span data-ttu-id="f3990-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f3990-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f3990-144">System.String</span><span class="sxs-lookup"><span data-stu-id="f3990-144">System.String</span></span>

### <span data-ttu-id="f3990-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="f3990-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="f3990-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3990-146">OUTPUTS</span></span>

### <span data-ttu-id="f3990-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f3990-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="f3990-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f3990-148">NOTES</span></span>

## <span data-ttu-id="f3990-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3990-149">RELATED LINKS</span></span>

[<span data-ttu-id="f3990-150">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f3990-150">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="f3990-151">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f3990-151">Remove-AzApiManagementApiVersionSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="f3990-152">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f3990-152">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)