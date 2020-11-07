---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 95444b74b3d62dd187a701e2305df2e241ff236f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668067"
---
# <span data-ttu-id="bf028-101">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="bf028-101">New-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="bf028-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf028-102">SYNOPSIS</span></span>
<span data-ttu-id="bf028-103">API-készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bf028-103">Creates an API Version Set.</span></span>

## <span data-ttu-id="bf028-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf028-104">SYNTAX</span></span>

```
New-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>] -Name <String>
 -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf028-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf028-105">DESCRIPTION</span></span>
<span data-ttu-id="bf028-106">A **New-AzApiManagementApiVersionSet** parancsmag létrehoz egy API-készletet az Azure API felügyeleti környezetében.</span><span class="sxs-lookup"><span data-stu-id="bf028-106">The **New-AzApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="bf028-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bf028-107">EXAMPLES</span></span>

### <span data-ttu-id="bf028-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bf028-108">Example 1</span></span>
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

<span data-ttu-id="bf028-109">A parancs létrehoz egy API-verziót, amely a verziószámozási sémát `Query` és a lekérdezési paramétert adja meg `api-version` .</span><span class="sxs-lookup"><span data-stu-id="bf028-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="bf028-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf028-110">PARAMETERS</span></span>

### <span data-ttu-id="bf028-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="bf028-111">-ApiVersionSetId</span></span>
<span data-ttu-id="bf028-112">Az új API-verzió azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf028-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="bf028-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="bf028-113">This parameter is optional.</span></span>
<span data-ttu-id="bf028-114">Ha nem ad meg azonosítót, a program létrehozza az azonosítót.</span><span class="sxs-lookup"><span data-stu-id="bf028-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="bf028-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="bf028-115">-Context</span></span>
<span data-ttu-id="bf028-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="bf028-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="bf028-117">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="bf028-117">This parameter is required.</span></span>

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

### <span data-ttu-id="bf028-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf028-118">-DefaultProfile</span></span>
<span data-ttu-id="bf028-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf028-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf028-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="bf028-120">-Description</span></span>
<span data-ttu-id="bf028-121">Az API-verzió készletének leírása.</span><span class="sxs-lookup"><span data-stu-id="bf028-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="bf028-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="bf028-122">-HeaderName</span></span>
<span data-ttu-id="bf028-123">A verziószámozási információkat tartalmazó fejléc értéke.</span><span class="sxs-lookup"><span data-stu-id="bf028-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="bf028-124">Ha a verziószámozási séma FEJLÉCe van kiválasztva, akkor ezt az értéket kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="bf028-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="bf028-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bf028-125">-Name</span></span>
<span data-ttu-id="bf028-126">A ApiVersion neve.</span><span class="sxs-lookup"><span data-stu-id="bf028-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="bf028-127">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="bf028-127">This parameter is required.</span></span>

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

### <span data-ttu-id="bf028-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="bf028-128">-QueryName</span></span>
<span data-ttu-id="bf028-129">A lekérdezési érték, amely a verziószámozási információkat fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="bf028-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="bf028-130">Ha a verziószámozási séma lekérdezése van kiválasztva, akkor ezt az értéket kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="bf028-130">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="bf028-131">-Scheme (séma)</span><span class="sxs-lookup"><span data-stu-id="bf028-131">-Scheme</span></span>
<span data-ttu-id="bf028-132">Verziószámozási séma az API verziószámozási készletének kiválasztásához.</span><span class="sxs-lookup"><span data-stu-id="bf028-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="bf028-133">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="bf028-133">This parameter is required.</span></span>

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

### <span data-ttu-id="bf028-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bf028-134">-Confirm</span></span>
<span data-ttu-id="bf028-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bf028-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf028-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf028-136">-WhatIf</span></span>
<span data-ttu-id="bf028-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bf028-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf028-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bf028-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf028-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf028-139">CommonParameters</span></span>
<span data-ttu-id="bf028-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf028-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf028-141">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bf028-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf028-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf028-142">INPUTS</span></span>

### <span data-ttu-id="bf028-143">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bf028-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bf028-144">System. String</span><span class="sxs-lookup"><span data-stu-id="bf028-144">System.String</span></span>

### <span data-ttu-id="bf028-145">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="bf028-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="bf028-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf028-146">OUTPUTS</span></span>

### <span data-ttu-id="bf028-147">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="bf028-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="bf028-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf028-148">NOTES</span></span>

## <span data-ttu-id="bf028-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf028-149">RELATED LINKS</span></span>

[<span data-ttu-id="bf028-150">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="bf028-150">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="bf028-151">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="bf028-151">Remove-AzApiManagementApiVersionSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="bf028-152">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="bf028-152">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)