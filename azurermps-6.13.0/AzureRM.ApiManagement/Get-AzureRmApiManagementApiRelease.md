---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 880d96ba0e9eff053084517452c03ffb018b72a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672128"
---
# <span data-ttu-id="c86c9-101">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c86c9-101">Get-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="c86c9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c86c9-102">SYNOPSIS</span></span>
<span data-ttu-id="c86c9-103">Az API-kiadás beszerzése.</span><span class="sxs-lookup"><span data-stu-id="c86c9-103">Get the API Release.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c86c9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c86c9-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c86c9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c86c9-105">DESCRIPTION</span></span>
<span data-ttu-id="c86c9-106">A **Get-AzureRmApiManagementApiRelease** parancsmag egy vagy több kiadást kap az Azure API Management API-hoz.</span><span class="sxs-lookup"><span data-stu-id="c86c9-106">The **Get-AzureRmApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="c86c9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c86c9-107">EXAMPLES</span></span>

### <span data-ttu-id="c86c9-108">1. példa: az API minden kiadásának lekérése</span><span class="sxs-lookup"><span data-stu-id="c86c9-108">Example 1: Get all releases of the API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contos
```

<span data-ttu-id="c86c9-109">Ez a parancs az API összes kiadását megkapja `echo-api` a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="c86c9-109">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="c86c9-110">2. példa: az adott API-kiadás kiadási adatainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="c86c9-110">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
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

<span data-ttu-id="c86c9-111">A parancs Kinyeri a megadott releaseId adott API-val kapcsolatos információkat.</span><span class="sxs-lookup"><span data-stu-id="c86c9-111">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="c86c9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c86c9-112">PARAMETERS</span></span>

### <span data-ttu-id="c86c9-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c86c9-113">-ApiId</span></span>
<span data-ttu-id="c86c9-114">A keresni kívánt API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c86c9-114">API identifier to look for.</span></span>
<span data-ttu-id="c86c9-115">Ha meg van adva az API-t, az azonosítóval is próbálkozhat.</span><span class="sxs-lookup"><span data-stu-id="c86c9-115">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="c86c9-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c86c9-116">-Context</span></span>
<span data-ttu-id="c86c9-117">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="c86c9-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c86c9-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="c86c9-118">This parameter is required.</span></span>

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

### <span data-ttu-id="c86c9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c86c9-119">-DefaultProfile</span></span>
<span data-ttu-id="c86c9-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c86c9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c86c9-121">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="c86c9-121">-ReleaseId</span></span>
<span data-ttu-id="c86c9-122">A kiadás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c86c9-122">The identifier of the Release.</span></span>

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

### <span data-ttu-id="c86c9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c86c9-123">CommonParameters</span></span>
<span data-ttu-id="c86c9-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c86c9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c86c9-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c86c9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c86c9-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c86c9-126">INPUTS</span></span>

### <span data-ttu-id="c86c9-127">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c86c9-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c86c9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c86c9-128">System.String</span></span>

## <span data-ttu-id="c86c9-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c86c9-129">OUTPUTS</span></span>

### <span data-ttu-id="c86c9-130">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c86c9-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="c86c9-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c86c9-131">NOTES</span></span>

## <span data-ttu-id="c86c9-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c86c9-132">RELATED LINKS</span></span>

[<span data-ttu-id="c86c9-133">Új – AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c86c9-133">New-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="c86c9-134">Remove-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c86c9-134">Remove-AzureRmApiManagementApiRelease</span></span>](./Remove-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="c86c9-135">Set-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c86c9-135">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
