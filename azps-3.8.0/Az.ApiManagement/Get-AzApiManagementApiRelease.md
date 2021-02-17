---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 7a3c418c5f55aa70b23972e5cd51065557335866
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404785"
---
# <span data-ttu-id="047eb-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="047eb-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="047eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="047eb-102">SYNOPSIS</span></span>
<span data-ttu-id="047eb-103">Szerezze be az API-kiadást.</span><span class="sxs-lookup"><span data-stu-id="047eb-103">Get the API Release.</span></span>

## <span data-ttu-id="047eb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="047eb-104">SYNTAX</span></span>

### <span data-ttu-id="047eb-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="047eb-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="047eb-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="047eb-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiRelease -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="047eb-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="047eb-107">DESCRIPTION</span></span>
<span data-ttu-id="047eb-108">A **Get-AzApiManagementApiRelease** parancsmag az Azure API Felügyeleti API egy vagy több kiadását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="047eb-108">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="047eb-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="047eb-109">EXAMPLES</span></span>

### <span data-ttu-id="047eb-110">1. példa: Az API összes kiadásának lekérte</span><span class="sxs-lookup"><span data-stu-id="047eb-110">Example 1: Get all releases of the API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="047eb-111">Ez a parancs az API összes kiadását beveszi `echo-api` a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="047eb-111">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="047eb-112">2. példa: Az adott API-kiadás kibocsátási információinak lekérte</span><span class="sxs-lookup"><span data-stu-id="047eb-112">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402
                    e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="047eb-113">Ez a parancs egy adott API kibocsátási adatait kapja meg a megadott releaseId értékekkel.</span><span class="sxs-lookup"><span data-stu-id="047eb-113">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="047eb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="047eb-114">PARAMETERS</span></span>

### <span data-ttu-id="047eb-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="047eb-115">-ApiId</span></span>
<span data-ttu-id="047eb-116">Keresend meg az API-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="047eb-116">API identifier to look for.</span></span>
<span data-ttu-id="047eb-117">Ha meg van adva, az API-t az azonosító próbálja meg lehozni.</span><span class="sxs-lookup"><span data-stu-id="047eb-117">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="047eb-118">-Környezet</span><span class="sxs-lookup"><span data-stu-id="047eb-118">-Context</span></span>
<span data-ttu-id="047eb-119">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="047eb-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="047eb-120">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="047eb-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="047eb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="047eb-121">-DefaultProfile</span></span>
<span data-ttu-id="047eb-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="047eb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="047eb-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="047eb-123">-ReleaseId</span></span>
<span data-ttu-id="047eb-124">A Kiadás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="047eb-124">The identifier of the Release.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="047eb-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="047eb-125">-ResourceId</span></span>
<span data-ttu-id="047eb-126">Api-kiadás Arm Resource Identifier azonosítója.</span><span class="sxs-lookup"><span data-stu-id="047eb-126">Arm Resource Identifier of a Api Release.</span></span> <span data-ttu-id="047eb-127">Ha meg van adva, az api-kiadást az azonosító alapján próbálja megtalálni.</span><span class="sxs-lookup"><span data-stu-id="047eb-127">If specified will try to find api release by the identifier.</span></span> <span data-ttu-id="047eb-128">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="047eb-128">This parameter is required.</span></span>

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

### <span data-ttu-id="047eb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="047eb-129">CommonParameters</span></span>
<span data-ttu-id="047eb-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="047eb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="047eb-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="047eb-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="047eb-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="047eb-132">INPUTS</span></span>

### <span data-ttu-id="047eb-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="047eb-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="047eb-134">System.String</span><span class="sxs-lookup"><span data-stu-id="047eb-134">System.String</span></span>

## <span data-ttu-id="047eb-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="047eb-135">OUTPUTS</span></span>

### <span data-ttu-id="047eb-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="047eb-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="047eb-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="047eb-137">NOTES</span></span>

## <span data-ttu-id="047eb-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="047eb-138">RELATED LINKS</span></span>

[<span data-ttu-id="047eb-139">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="047eb-139">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="047eb-140">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="047eb-140">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="047eb-141">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="047eb-141">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)