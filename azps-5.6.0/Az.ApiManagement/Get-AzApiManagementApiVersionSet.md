---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: be18436936a7329de0b43701311a899713311ad9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009446"
---
# <span data-ttu-id="9e468-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9e468-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="9e468-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e468-102">SYNOPSIS</span></span>
<span data-ttu-id="9e468-103">Az API verziókészletek részleteinek lekérte</span><span class="sxs-lookup"><span data-stu-id="9e468-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="9e468-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9e468-104">SYNTAX</span></span>

### <span data-ttu-id="9e468-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9e468-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e468-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e468-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e468-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9e468-107">DESCRIPTION</span></span>
<span data-ttu-id="9e468-108">A **Get-AzApiManagementApiVersionSet** parancsmag api-kezelési környezetben konfigurált API-verziókészletek részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9e468-108">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="9e468-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9e468-109">EXAMPLES</span></span>

### <span data-ttu-id="9e468-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="9e468-110">Example 1</span></span>

### <span data-ttu-id="9e468-111">2. példa: Az összes API-verziókészlet lekérte</span><span class="sxs-lookup"><span data-stu-id="9e468-111">Example 2: Get all API Version Sets</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiVersionSet -Context $ApiMgmtContext

ApiVersionSetId   : a93316c8-8b88-46cc-8260-380789a5d598
Description       :
VersionQueryName  :
VersionHeaderName :
DisplayName       : Echo API
VersioningScheme  : Segment
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/a916c8-8b88-46cc-8260-380789a5d598
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso

ApiVersionSetId   : 4cbdfa34-25f3-4a93-a9b6-76b6eade7562
Description       :
VersionQueryName  : api-version
VersionHeaderName :
DisplayName       : getproduct old
VersioningScheme  : Query
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/4cbdfa34-25f3-4a93-a9b6-76b6eade7562
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso


ApiVersionSetId   : 8c441e0e-a0cd-47d8-8d88-f944a83b41bd
Description       :
VersionQueryName  :
VersionHeaderName : Api-Version
DisplayName       : ordersapi
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/8c441e0e-a0cd-47d8-8d88-f944a83b41bd
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="9e468-112">Ez a parancs a megadott környezethez az összes API-verziókészletet beállítja.</span><span class="sxs-lookup"><span data-stu-id="9e468-112">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="9e468-113">3. példa: API verzióazonosító szerint beállítva</span><span class="sxs-lookup"><span data-stu-id="9e468-113">Example 3: Get a API Version Set by ID</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId $ApiVersionSetId

ApiVersionSetId   : 8c441e0e-a0cd-47d8-8d88-f944a83b41bd
Description       :
VersionQueryName  :
VersionHeaderName : Api-Version
DisplayName       : ordersapi
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/8c441e0e-a0cd-47d8-8d88-f944a83b41bd
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="9e468-114">Ez a parancs a megadott azonosítójú API-verziókészletet kapja.</span><span class="sxs-lookup"><span data-stu-id="9e468-114">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="9e468-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e468-115">PARAMETERS</span></span>

### <span data-ttu-id="9e468-116">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="9e468-116">-ApiVersionSetId</span></span>
<span data-ttu-id="9e468-117">Keresend meg az API-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="9e468-117">API identifier to look for.</span></span>
<span data-ttu-id="9e468-118">Ha meg van adva, az API-t az azonosító próbálja meg lehozni.</span><span class="sxs-lookup"><span data-stu-id="9e468-118">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="9e468-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="9e468-119">-Context</span></span>
<span data-ttu-id="9e468-120">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="9e468-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9e468-121">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="9e468-121">This parameter is required.</span></span>

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

### <span data-ttu-id="9e468-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e468-122">-DefaultProfile</span></span>
<span data-ttu-id="9e468-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e468-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e468-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e468-124">-ResourceId</span></span>
<span data-ttu-id="9e468-125">Arm Resource Identifier of the ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="9e468-125">Arm Resource Identifier of the ApiVersionSet.</span></span> <span data-ttu-id="9e468-126">Ha meg van adva, az apiVersionSet az azonosító alapján próbálja megtalálni.</span><span class="sxs-lookup"><span data-stu-id="9e468-126">If specified will try to find apiVersionSet by the identifier.</span></span> <span data-ttu-id="9e468-127">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="9e468-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e468-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e468-128">CommonParameters</span></span>
<span data-ttu-id="9e468-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e468-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e468-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e468-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e468-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e468-131">INPUTS</span></span>

### <span data-ttu-id="9e468-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9e468-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9e468-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9e468-133">System.String</span></span>

## <span data-ttu-id="9e468-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e468-134">OUTPUTS</span></span>

### <span data-ttu-id="9e468-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9e468-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="9e468-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9e468-136">NOTES</span></span>

## <span data-ttu-id="9e468-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e468-137">RELATED LINKS</span></span>

[<span data-ttu-id="9e468-138">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9e468-138">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="9e468-139">Remove-AzApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="9e468-139">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="9e468-140">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9e468-140">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
