---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 7a3c418c5f55aa70b23972e5cd51065557335866
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302264"
---
# <span data-ttu-id="3e1a0-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3e1a0-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="3e1a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3e1a0-102">SYNOPSIS</span></span>
<span data-ttu-id="3e1a0-103">Az API-kiadás beszerzése.</span><span class="sxs-lookup"><span data-stu-id="3e1a0-103">Get the API Release.</span></span>

## <span data-ttu-id="3e1a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3e1a0-104">SYNTAX</span></span>

### <span data-ttu-id="3e1a0-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3e1a0-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e1a0-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e1a0-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiRelease -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e1a0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3e1a0-107">DESCRIPTION</span></span>
<span data-ttu-id="3e1a0-108">A **Get-AzApiManagementApiRelease** parancsmag egy vagy több kiadást kap az Azure API Management API-hoz.</span><span class="sxs-lookup"><span data-stu-id="3e1a0-108">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="3e1a0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3e1a0-109">EXAMPLES</span></span>

### <span data-ttu-id="3e1a0-110">1. példa: az API minden kiadásának lekérése</span><span class="sxs-lookup"><span data-stu-id="3e1a0-110">Example 1: Get all releases of the API</span></span>
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

<span data-ttu-id="3e1a0-111">Ez a parancs az API összes kiadását megkapja `echo-api` a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="3e1a0-111">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="3e1a0-112">2. példa: az adott API-kiadás kiadási adatainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="3e1a0-112">Example 2: Get the release information of the particular API release</span></span>
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

<span data-ttu-id="3e1a0-113">A parancs Kinyeri a megadott releaseId adott API-val kapcsolatos információkat.</span><span class="sxs-lookup"><span data-stu-id="3e1a0-113">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="3e1a0-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3e1a0-114">PARAMETERS</span></span>

### <span data-ttu-id="3e1a0-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3e1a0-115">-ApiId</span></span>
<span data-ttu-id="3e1a0-116">A keresni kívánt API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="3e1a0-116">API identifier to look for.</span></span>
<span data-ttu-id="3e1a0-117">Ha meg van adva az API-t, az azonosítóval is próbálkozhat.</span><span class="sxs-lookup"><span data-stu-id="3e1a0-117">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="3e1a0-118">-Környezet</span><span class="sxs-lookup"><span data-stu-id="3e1a0-118">-Context</span></span>
<span data-ttu-id="3e1a0-119">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="3e1a0-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3e1a0-120">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="3e1a0-120">This parameter is required.</span></span>

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

### <span data-ttu-id="3e1a0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e1a0-121">-DefaultProfile</span></span>
<span data-ttu-id="3e1a0-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e1a0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e1a0-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="3e1a0-123">-ReleaseId</span></span>
<span data-ttu-id="3e1a0-124">A kiadás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3e1a0-124">The identifier of the Release.</span></span>

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

### <span data-ttu-id="3e1a0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e1a0-125">-ResourceId</span></span>
<span data-ttu-id="3e1a0-126">Az API-kiadás kar erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3e1a0-126">Arm Resource Identifier of a Api Release.</span></span> <span data-ttu-id="3e1a0-127">Ha meg van adva az API-kiadás keresése az azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="3e1a0-127">If specified will try to find api release by the identifier.</span></span> <span data-ttu-id="3e1a0-128">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="3e1a0-128">This parameter is required.</span></span>

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

### <span data-ttu-id="3e1a0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e1a0-129">CommonParameters</span></span>
<span data-ttu-id="3e1a0-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3e1a0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e1a0-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3e1a0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e1a0-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e1a0-132">INPUTS</span></span>

### <span data-ttu-id="3e1a0-133">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3e1a0-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3e1a0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3e1a0-134">System.String</span></span>

## <span data-ttu-id="3e1a0-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e1a0-135">OUTPUTS</span></span>

### <span data-ttu-id="3e1a0-136">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3e1a0-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="3e1a0-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3e1a0-137">NOTES</span></span>

## <span data-ttu-id="3e1a0-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e1a0-138">RELATED LINKS</span></span>

[<span data-ttu-id="3e1a0-139">Új – AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3e1a0-139">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="3e1a0-140">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3e1a0-140">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="3e1a0-141">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3e1a0-141">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)