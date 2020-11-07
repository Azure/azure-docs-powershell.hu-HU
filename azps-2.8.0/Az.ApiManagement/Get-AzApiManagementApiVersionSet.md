---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 4fefe6e7a763cdce60483342e8e8db880405e060
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668124"
---
# <span data-ttu-id="9cc6e-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9cc6e-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="9cc6e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9cc6e-102">SYNOPSIS</span></span>
<span data-ttu-id="9cc6e-103">Az API-készletek részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="9cc6e-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="9cc6e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9cc6e-104">SYNTAX</span></span>

### <span data-ttu-id="9cc6e-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9cc6e-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cc6e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cc6e-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cc6e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9cc6e-107">DESCRIPTION</span></span>
<span data-ttu-id="9cc6e-108">A **Get-AzApiManagementApiVersionSet** parancsmag az API-kezelés kontextusában konfigurált API-verziók adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9cc6e-108">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="9cc6e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9cc6e-109">EXAMPLES</span></span>

### <span data-ttu-id="9cc6e-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9cc6e-110">Example 1</span></span>

### <span data-ttu-id="9cc6e-111">1. példa: az összes API-verzió beszerzése</span><span class="sxs-lookup"><span data-stu-id="9cc6e-111">Example 1: Get all API Version Sets</span></span>
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

<span data-ttu-id="9cc6e-112">Ez a parancs a megadott környezetben az összes API-verzió halmazát beolvassa.</span><span class="sxs-lookup"><span data-stu-id="9cc6e-112">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="9cc6e-113">2. példa: az API-verzió beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="9cc6e-113">Example 2: Get a API Version Set by ID</span></span>
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

<span data-ttu-id="9cc6e-114">Ez a parancs a megadott AZONOSÍTÓJÚ API-verziót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9cc6e-114">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="9cc6e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9cc6e-115">PARAMETERS</span></span>

### <span data-ttu-id="9cc6e-116">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="9cc6e-116">-ApiVersionSetId</span></span>
<span data-ttu-id="9cc6e-117">A keresni kívánt API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="9cc6e-117">API identifier to look for.</span></span>
<span data-ttu-id="9cc6e-118">Ha meg van adva az API-t, az azonosítóval is próbálkozhat.</span><span class="sxs-lookup"><span data-stu-id="9cc6e-118">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="9cc6e-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="9cc6e-119">-Context</span></span>
<span data-ttu-id="9cc6e-120">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="9cc6e-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9cc6e-121">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="9cc6e-121">This parameter is required.</span></span>

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

### <span data-ttu-id="9cc6e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cc6e-122">-DefaultProfile</span></span>
<span data-ttu-id="9cc6e-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9cc6e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cc6e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cc6e-124">-ResourceId</span></span>
<span data-ttu-id="9cc6e-125">A ApiVersionSet kar erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9cc6e-125">Arm Resource Identifier of the ApiVersionSet.</span></span> <span data-ttu-id="9cc6e-126">Ha meg van adva, a apiVersionSet megkeresi az azonosítót.</span><span class="sxs-lookup"><span data-stu-id="9cc6e-126">If specified will try to find apiVersionSet by the identifier.</span></span> <span data-ttu-id="9cc6e-127">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="9cc6e-127">This parameter is required.</span></span>

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

### <span data-ttu-id="9cc6e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cc6e-128">CommonParameters</span></span>
<span data-ttu-id="9cc6e-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9cc6e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cc6e-130">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9cc6e-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cc6e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cc6e-131">INPUTS</span></span>

### <span data-ttu-id="9cc6e-132">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9cc6e-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9cc6e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9cc6e-133">System.String</span></span>

## <span data-ttu-id="9cc6e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cc6e-134">OUTPUTS</span></span>

### <span data-ttu-id="9cc6e-135">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9cc6e-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="9cc6e-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9cc6e-136">NOTES</span></span>

## <span data-ttu-id="9cc6e-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9cc6e-137">RELATED LINKS</span></span>

[<span data-ttu-id="9cc6e-138">Új – AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9cc6e-138">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="9cc6e-139">Remove-AzApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="9cc6e-139">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="9cc6e-140">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9cc6e-140">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiSet.md)
