---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: 833351c3abbf95eb898405f23241a20fe9affefa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157627"
---
# <span data-ttu-id="55eeb-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="55eeb-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="55eeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55eeb-102">SYNOPSIS</span></span>
<span data-ttu-id="55eeb-103">Létrehozza egy meglévő API új változatát.</span><span class="sxs-lookup"><span data-stu-id="55eeb-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="55eeb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="55eeb-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ApiRevisionDescription <String>] [-SourceApiRevision <String>] [-ServiceUrl <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55eeb-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="55eeb-105">DESCRIPTION</span></span>

<span data-ttu-id="55eeb-106">A **New-AzApiManagementApiRevision** parancsmag létrehoz egy API-változatot egy meglévő API-hoz az API-kezelés környezetében.</span><span class="sxs-lookup"><span data-stu-id="55eeb-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="55eeb-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="55eeb-107">EXAMPLES</span></span>

### <span data-ttu-id="55eeb-108">1. példa: Üres API-változat létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="55eeb-108">Example 1: Create an empty API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"


New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"
```

<span data-ttu-id="55eeb-109">Ez a parancs létrehozza az `2` API API-változatát. `echo-api`</span><span class="sxs-lookup"><span data-stu-id="55eeb-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

### <span data-ttu-id="55eeb-110">2. példa: API-változat létrehozása egy meglévő API-ból, és az összes művelet, címke és házirend másolása</span><span class="sxs-lookup"><span data-stu-id="55eeb-110">Example 2: Create an API Revision from an Existing Api and copy All operations, tags and Policies</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5" -SourceApiRevision "1" -ServiceUrl "https://echoapi.cloudapp.net/rev4"


ApiId                         : echo-api;rev=5
Name                          : Echo API
Description                   :
ServiceUrl                    : http://echoapi.cloudapp.net/api
Path                          : echo
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 5
ApiVersion                    :
IsCurrent                     : False
IsOnline                      : False
SubscriptionRequired          : True
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               :
Id                            : /subscriptions/subid/resourceGroups/apimService1/providers/Microsoft.ApiManagement/service/sdktestapim4163/apis/echo-api;rev=5
ResourceGroupName             : apimService1
ServiceName                   : sdktestapim4163
```

<span data-ttu-id="55eeb-111">Ez a parancs létrehozza az API `5` `echo-api` API-változatát.</span><span class="sxs-lookup"><span data-stu-id="55eeb-111">This command creates an API Revision `5` of the `echo-api` API.</span></span>

## <span data-ttu-id="55eeb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55eeb-112">PARAMETERS</span></span>

### <span data-ttu-id="55eeb-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="55eeb-113">-ApiId</span></span>
<span data-ttu-id="55eeb-114">Annak az API-nak az azonosítója, amelynek a korrektúraszámát létre kell hozatni.</span><span class="sxs-lookup"><span data-stu-id="55eeb-114">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="55eeb-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="55eeb-115">-ApiRevision</span></span>
<span data-ttu-id="55eeb-116">Az Api korrektúraazonosítója.</span><span class="sxs-lookup"><span data-stu-id="55eeb-116">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="55eeb-117">-ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="55eeb-117">-ApiRevisionDescription</span></span>
<span data-ttu-id="55eeb-118">Az API változatának leírása.</span><span class="sxs-lookup"><span data-stu-id="55eeb-118">Api Revision Description.</span></span> <span data-ttu-id="55eeb-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="55eeb-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="55eeb-120">-Környezet</span><span class="sxs-lookup"><span data-stu-id="55eeb-120">-Context</span></span>
<span data-ttu-id="55eeb-121">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="55eeb-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="55eeb-122">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="55eeb-122">This parameter is required.</span></span>

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

### <span data-ttu-id="55eeb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55eeb-123">-DefaultProfile</span></span>
<span data-ttu-id="55eeb-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="55eeb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55eeb-125">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="55eeb-125">-ServiceUrl</span></span>
<span data-ttu-id="55eeb-126">A webszolgáltatás URL-címe, amely felfedi az API-t a Háttérszolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="55eeb-126">A URL of the web service exposing the API in the Backend service.</span></span> <span data-ttu-id="55eeb-127">Ezt az URL-címet csak az Azure API Management fogja használni, és nem teszi nyilvánosra.</span><span class="sxs-lookup"><span data-stu-id="55eeb-127">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="55eeb-128">1–2000 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="55eeb-128">Must be 1 to 2000 characters long.</span></span> <span data-ttu-id="55eeb-129">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="55eeb-129">This parameter is required.</span></span>

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

### <span data-ttu-id="55eeb-130">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="55eeb-130">-SourceApiRevision</span></span>
<span data-ttu-id="55eeb-131">A forrás API Api-korrektúraazonosítója.</span><span class="sxs-lookup"><span data-stu-id="55eeb-131">Api Revision identifier of the source API.</span></span> <span data-ttu-id="55eeb-132">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="55eeb-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="55eeb-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55eeb-133">-Confirm</span></span>
<span data-ttu-id="55eeb-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="55eeb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55eeb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55eeb-135">-WhatIf</span></span>
<span data-ttu-id="55eeb-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="55eeb-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55eeb-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="55eeb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55eeb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55eeb-138">CommonParameters</span></span>
<span data-ttu-id="55eeb-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55eeb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55eeb-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55eeb-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55eeb-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55eeb-141">INPUTS</span></span>

### <span data-ttu-id="55eeb-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="55eeb-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="55eeb-143">System.String</span><span class="sxs-lookup"><span data-stu-id="55eeb-143">System.String</span></span>

## <span data-ttu-id="55eeb-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55eeb-144">OUTPUTS</span></span>

### <span data-ttu-id="55eeb-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="55eeb-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="55eeb-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="55eeb-146">NOTES</span></span>

## <span data-ttu-id="55eeb-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55eeb-147">RELATED LINKS</span></span>

[<span data-ttu-id="55eeb-148">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="55eeb-148">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="55eeb-149">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="55eeb-149">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="55eeb-150">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="55eeb-150">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
