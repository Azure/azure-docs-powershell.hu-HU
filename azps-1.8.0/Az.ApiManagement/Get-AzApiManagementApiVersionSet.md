---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 5b7c06e9ed75cf973a3b9e375ff888477b9a96d7
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400977"
---
# <span data-ttu-id="913d5-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="913d5-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="913d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="913d5-102">SYNOPSIS</span></span>
<span data-ttu-id="913d5-103">Az API verziókészletek részleteinek lekérte</span><span class="sxs-lookup"><span data-stu-id="913d5-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="913d5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="913d5-104">SYNTAX</span></span>

```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="913d5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="913d5-105">DESCRIPTION</span></span>
<span data-ttu-id="913d5-106">A **Get-AzApiManagementApiVersionSet** parancsmag api-kezelési környezetben konfigurált API-verziókészletek részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="913d5-106">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="913d5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="913d5-107">EXAMPLES</span></span>

### <span data-ttu-id="913d5-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="913d5-108">Example 1</span></span>

### <span data-ttu-id="913d5-109">1. példa: Az összes API-verziókészlet lekérte</span><span class="sxs-lookup"><span data-stu-id="913d5-109">Example 1: Get all API Version Sets</span></span>
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

<span data-ttu-id="913d5-110">Ez a parancs a megadott környezethez az összes API-verziókészletet beállítja.</span><span class="sxs-lookup"><span data-stu-id="913d5-110">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="913d5-111">2. példa: API verzióazonosító szerint beállítva</span><span class="sxs-lookup"><span data-stu-id="913d5-111">Example 2: Get a API Version Set by ID</span></span>
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

<span data-ttu-id="913d5-112">Ez a parancs a megadott azonosítójú API-verziókészletet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="913d5-112">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="913d5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="913d5-113">PARAMETERS</span></span>

### <span data-ttu-id="913d5-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="913d5-114">-ApiVersionSetId</span></span>
<span data-ttu-id="913d5-115">Keresend meg az API-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="913d5-115">API identifier to look for.</span></span>
<span data-ttu-id="913d5-116">Ha meg van adva, az API-t az azonosító próbálja meg lehozni.</span><span class="sxs-lookup"><span data-stu-id="913d5-116">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="913d5-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="913d5-117">-Context</span></span>
<span data-ttu-id="913d5-118">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="913d5-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="913d5-119">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="913d5-119">This parameter is required.</span></span>

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

### <span data-ttu-id="913d5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="913d5-120">-DefaultProfile</span></span>
<span data-ttu-id="913d5-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="913d5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="913d5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="913d5-122">CommonParameters</span></span>
<span data-ttu-id="913d5-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="913d5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="913d5-124">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="913d5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="913d5-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="913d5-125">INPUTS</span></span>

### <span data-ttu-id="913d5-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="913d5-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="913d5-127">System.String</span><span class="sxs-lookup"><span data-stu-id="913d5-127">System.String</span></span>

## <span data-ttu-id="913d5-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="913d5-128">OUTPUTS</span></span>

### <span data-ttu-id="913d5-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="913d5-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="913d5-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="913d5-130">NOTES</span></span>

## <span data-ttu-id="913d5-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="913d5-131">RELATED LINKS</span></span>

[<span data-ttu-id="913d5-132">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="913d5-132">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="913d5-133">Remove-AzApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="913d5-133">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="913d5-134">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="913d5-134">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
