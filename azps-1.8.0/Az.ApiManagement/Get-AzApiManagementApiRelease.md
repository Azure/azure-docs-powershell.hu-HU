---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 4f9e917f17037e5f47b52501007da5556bde1187
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401079"
---
# <span data-ttu-id="87837-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="87837-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="87837-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87837-102">SYNOPSIS</span></span>
<span data-ttu-id="87837-103">Szerezze be az API-kiadást.</span><span class="sxs-lookup"><span data-stu-id="87837-103">Get the API Release.</span></span>

## <span data-ttu-id="87837-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="87837-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87837-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="87837-105">DESCRIPTION</span></span>
<span data-ttu-id="87837-106">A **Get-AzApiManagementApiRelease** parancsmag az Azure API Felügyeleti API egy vagy több kiadását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="87837-106">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="87837-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="87837-107">EXAMPLES</span></span>

### <span data-ttu-id="87837-108">1. példa: Az API összes kiadásának lekérte</span><span class="sxs-lookup"><span data-stu-id="87837-108">Example 1: Get all releases of the API</span></span>
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
ServiceName       : contos
```

<span data-ttu-id="87837-109">Ez a parancs az API összes kiadását beveszi `echo-api` a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="87837-109">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="87837-110">2. példa: Az adott API-kiadás kibocsátási információinak lekérte</span><span class="sxs-lookup"><span data-stu-id="87837-110">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contos/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402
                    e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contos
```

<span data-ttu-id="87837-111">Ez a parancs egy adott API kibocsátási adatait kapja meg a megadott releaseId értékekkel.</span><span class="sxs-lookup"><span data-stu-id="87837-111">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="87837-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87837-112">PARAMETERS</span></span>

### <span data-ttu-id="87837-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="87837-113">-ApiId</span></span>
<span data-ttu-id="87837-114">Keresend meg az API-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="87837-114">API identifier to look for.</span></span>
<span data-ttu-id="87837-115">Ha meg van adva, az API-t az azonosító próbálja meg lehozni.</span><span class="sxs-lookup"><span data-stu-id="87837-115">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="87837-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="87837-116">-Context</span></span>
<span data-ttu-id="87837-117">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="87837-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="87837-118">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="87837-118">This parameter is required.</span></span>

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

### <span data-ttu-id="87837-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87837-119">-DefaultProfile</span></span>
<span data-ttu-id="87837-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87837-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87837-121">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="87837-121">-ReleaseId</span></span>
<span data-ttu-id="87837-122">A Kiadás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="87837-122">The identifier of the Release.</span></span>

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

### <span data-ttu-id="87837-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87837-123">CommonParameters</span></span>
<span data-ttu-id="87837-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87837-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87837-125">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87837-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87837-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87837-126">INPUTS</span></span>

### <span data-ttu-id="87837-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="87837-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="87837-128">System.String</span><span class="sxs-lookup"><span data-stu-id="87837-128">System.String</span></span>

## <span data-ttu-id="87837-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87837-129">OUTPUTS</span></span>

### <span data-ttu-id="87837-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="87837-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="87837-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="87837-131">NOTES</span></span>

## <span data-ttu-id="87837-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87837-132">RELATED LINKS</span></span>

[<span data-ttu-id="87837-133">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="87837-133">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="87837-134">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="87837-134">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="87837-135">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="87837-135">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)