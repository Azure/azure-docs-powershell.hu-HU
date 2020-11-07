---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 16fea88f5a5a1ad8a0e39f62b26d918ca7a64dbd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665695"
---
# <span data-ttu-id="66343-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="66343-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="66343-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66343-102">SYNOPSIS</span></span>
<span data-ttu-id="66343-103">Az API-készletek részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="66343-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="66343-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66343-104">SYNTAX</span></span>

```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66343-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="66343-105">DESCRIPTION</span></span>
<span data-ttu-id="66343-106">A **Get-AzApiManagementApiVersionSet** parancsmag az API-kezelés kontextusában konfigurált API-verziók adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="66343-106">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="66343-107">Példák</span><span class="sxs-lookup"><span data-stu-id="66343-107">EXAMPLES</span></span>

### <span data-ttu-id="66343-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="66343-108">Example 1</span></span>

### <span data-ttu-id="66343-109">1. példa: az összes API-verzió beszerzése</span><span class="sxs-lookup"><span data-stu-id="66343-109">Example 1: Get all API Version Sets</span></span>
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

<span data-ttu-id="66343-110">Ez a parancs a megadott környezetben az összes API-verzió halmazát beolvassa.</span><span class="sxs-lookup"><span data-stu-id="66343-110">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="66343-111">2. példa: az API-verzió beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="66343-111">Example 2: Get a API Version Set by ID</span></span>
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

<span data-ttu-id="66343-112">Ez a parancs a megadott AZONOSÍTÓJÚ API-verziót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="66343-112">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="66343-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66343-113">PARAMETERS</span></span>

### <span data-ttu-id="66343-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="66343-114">-ApiVersionSetId</span></span>
<span data-ttu-id="66343-115">A keresni kívánt API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="66343-115">API identifier to look for.</span></span>
<span data-ttu-id="66343-116">Ha meg van adva az API-t, az azonosítóval is próbálkozhat.</span><span class="sxs-lookup"><span data-stu-id="66343-116">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="66343-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="66343-117">-Context</span></span>
<span data-ttu-id="66343-118">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="66343-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="66343-119">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="66343-119">This parameter is required.</span></span>

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

### <span data-ttu-id="66343-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66343-120">-DefaultProfile</span></span>
<span data-ttu-id="66343-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66343-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66343-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66343-122">CommonParameters</span></span>
<span data-ttu-id="66343-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="66343-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66343-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66343-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66343-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66343-125">INPUTS</span></span>

### <span data-ttu-id="66343-126">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="66343-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="66343-127">System. String</span><span class="sxs-lookup"><span data-stu-id="66343-127">System.String</span></span>

## <span data-ttu-id="66343-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66343-128">OUTPUTS</span></span>

### <span data-ttu-id="66343-129">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="66343-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="66343-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66343-130">NOTES</span></span>

## <span data-ttu-id="66343-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66343-131">RELATED LINKS</span></span>

[<span data-ttu-id="66343-132">Új – AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="66343-132">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="66343-133">Remove-AzApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="66343-133">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="66343-134">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="66343-134">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiSet.md)
