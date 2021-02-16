---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: 8b6f27191ee92240a8dc9e5e8289fda72db856ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143747"
---
# <span data-ttu-id="ef812-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ef812-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="ef812-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef812-102">SYNOPSIS</span></span>
<span data-ttu-id="ef812-103">Api-t kap.</span><span class="sxs-lookup"><span data-stu-id="ef812-103">Gets an API.</span></span>

## <span data-ttu-id="ef812-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ef812-104">SYNTAX</span></span>

### <span data-ttu-id="ef812-105">GetAllApis (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef812-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef812-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="ef812-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef812-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="ef812-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef812-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="ef812-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef812-109">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="ef812-109">GetByGatewayId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef812-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ef812-110">DESCRIPTION</span></span>
<span data-ttu-id="ef812-111">A **Get-AzApiManagementApi** parancsmag egy vagy több Azure API Management API-t kap.</span><span class="sxs-lookup"><span data-stu-id="ef812-111">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="ef812-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ef812-112">EXAMPLES</span></span>

### <span data-ttu-id="ef812-113">1. példa: Az összes felügyeleti API lekérte</span><span class="sxs-lookup"><span data-stu-id="ef812-113">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="ef812-114">Ez a parancs a megadott környezet összes API-ját beveszi.</span><span class="sxs-lookup"><span data-stu-id="ef812-114">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="ef812-115">2. példa: Felügyeleti API lekért azonosítója</span><span class="sxs-lookup"><span data-stu-id="ef812-115">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="ef812-116">Ez a parancs a megadott azonosítóval kapja meg az API-t.</span><span class="sxs-lookup"><span data-stu-id="ef812-116">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="ef812-117">3. példa: Felügyeleti API lekért név szerint</span><span class="sxs-lookup"><span data-stu-id="ef812-117">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="ef812-118">Ez a parancs a megadott nevű API-t kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ef812-118">This command gets the API with the specified name.</span></span>

### <span data-ttu-id="ef812-119">4. példa: Felügyeleti API lekérte a GatewayId-et</span><span class="sxs-lookup"><span data-stu-id="ef812-119">Example 4: Get a management API by GatewayId</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -GatewayId "g01"
```

<span data-ttu-id="ef812-120">Ez a parancs a megadott GatewayId API-t kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ef812-120">This command gets the API for the specified GatewayId.</span></span>

## <span data-ttu-id="ef812-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef812-121">PARAMETERS</span></span>

### <span data-ttu-id="ef812-122">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ef812-122">-ApiId</span></span>
<span data-ttu-id="ef812-123">A lekért API azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ef812-123">Specifies the ID of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef812-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="ef812-124">-ApiRevision</span></span>
<span data-ttu-id="ef812-125">Az adott Api-változat korrektúraazonosítója.</span><span class="sxs-lookup"><span data-stu-id="ef812-125">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="ef812-126">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ef812-126">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef812-127">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ef812-127">-Context</span></span>
<span data-ttu-id="ef812-128">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="ef812-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ef812-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef812-129">-DefaultProfile</span></span>
<span data-ttu-id="ef812-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef812-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef812-131">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="ef812-131">-GatewayId</span></span>
<span data-ttu-id="ef812-132">Ha meg van adva, az összes átjáró api-ját megpróbálja lekésni.</span><span class="sxs-lookup"><span data-stu-id="ef812-132">If specified will try to get all Gateway APIs.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef812-133">-Name</span><span class="sxs-lookup"><span data-stu-id="ef812-133">-Name</span></span>
<span data-ttu-id="ef812-134">A lekért API neve.</span><span class="sxs-lookup"><span data-stu-id="ef812-134">Specifies the name of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef812-135">-ProductId</span><span class="sxs-lookup"><span data-stu-id="ef812-135">-ProductId</span></span>
<span data-ttu-id="ef812-136">Annak a terméknek az azonosítója, amelyhez az API-t le kell szerezni.</span><span class="sxs-lookup"><span data-stu-id="ef812-136">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef812-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef812-137">CommonParameters</span></span>
<span data-ttu-id="ef812-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef812-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef812-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef812-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef812-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef812-140">INPUTS</span></span>

### <span data-ttu-id="ef812-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ef812-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ef812-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ef812-142">System.String</span></span>

## <span data-ttu-id="ef812-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef812-143">OUTPUTS</span></span>

### <span data-ttu-id="ef812-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ef812-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="ef812-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ef812-145">NOTES</span></span>

## <span data-ttu-id="ef812-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef812-146">RELATED LINKS</span></span>

[<span data-ttu-id="ef812-147">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ef812-147">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="ef812-148">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ef812-148">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="ef812-149">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ef812-149">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="ef812-150">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ef812-150">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="ef812-151">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ef812-151">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


