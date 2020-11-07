---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 353fd6365f85ba71105f80324ba740b4d829a85a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665699"
---
# <span data-ttu-id="fd0c5-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="fd0c5-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="fd0c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd0c5-102">SYNOPSIS</span></span>
<span data-ttu-id="fd0c5-103">Az API-kiadás beszerzése.</span><span class="sxs-lookup"><span data-stu-id="fd0c5-103">Get the API Release.</span></span>

## <span data-ttu-id="fd0c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd0c5-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd0c5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd0c5-105">DESCRIPTION</span></span>
<span data-ttu-id="fd0c5-106">A **Get-AzApiManagementApiRelease** parancsmag egy vagy több kiadást kap az Azure API Management API-hoz.</span><span class="sxs-lookup"><span data-stu-id="fd0c5-106">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="fd0c5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fd0c5-107">EXAMPLES</span></span>

### <span data-ttu-id="fd0c5-108">1. példa: az API minden kiadásának lekérése</span><span class="sxs-lookup"><span data-stu-id="fd0c5-108">Example 1: Get all releases of the API</span></span>
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

<span data-ttu-id="fd0c5-109">Ez a parancs az API összes kiadását megkapja `echo-api` a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="fd0c5-109">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="fd0c5-110">2. példa: az adott API-kiadás kiadási adatainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="fd0c5-110">Example 2: Get the release information of the particular API release</span></span>
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

<span data-ttu-id="fd0c5-111">A parancs Kinyeri a megadott releaseId adott API-val kapcsolatos információkat.</span><span class="sxs-lookup"><span data-stu-id="fd0c5-111">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="fd0c5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd0c5-112">PARAMETERS</span></span>

### <span data-ttu-id="fd0c5-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fd0c5-113">-ApiId</span></span>
<span data-ttu-id="fd0c5-114">A keresni kívánt API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="fd0c5-114">API identifier to look for.</span></span>
<span data-ttu-id="fd0c5-115">Ha meg van adva az API-t, az azonosítóval is próbálkozhat.</span><span class="sxs-lookup"><span data-stu-id="fd0c5-115">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="fd0c5-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="fd0c5-116">-Context</span></span>
<span data-ttu-id="fd0c5-117">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="fd0c5-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fd0c5-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="fd0c5-118">This parameter is required.</span></span>

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

### <span data-ttu-id="fd0c5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd0c5-119">-DefaultProfile</span></span>
<span data-ttu-id="fd0c5-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd0c5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd0c5-121">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="fd0c5-121">-ReleaseId</span></span>
<span data-ttu-id="fd0c5-122">A kiadás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fd0c5-122">The identifier of the Release.</span></span>

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

### <span data-ttu-id="fd0c5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd0c5-123">CommonParameters</span></span>
<span data-ttu-id="fd0c5-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd0c5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd0c5-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd0c5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd0c5-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd0c5-126">INPUTS</span></span>

### <span data-ttu-id="fd0c5-127">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fd0c5-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fd0c5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fd0c5-128">System.String</span></span>

## <span data-ttu-id="fd0c5-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd0c5-129">OUTPUTS</span></span>

### <span data-ttu-id="fd0c5-130">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="fd0c5-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="fd0c5-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd0c5-131">NOTES</span></span>

## <span data-ttu-id="fd0c5-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd0c5-132">RELATED LINKS</span></span>

[<span data-ttu-id="fd0c5-133">Új – AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="fd0c5-133">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="fd0c5-134">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="fd0c5-134">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="fd0c5-135">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="fd0c5-135">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)