---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: 8b6f27191ee92240a8dc9e5e8289fda72db856ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299921"
---
# <span data-ttu-id="33f6f-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="33f6f-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="33f6f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="33f6f-102">SYNOPSIS</span></span>
<span data-ttu-id="33f6f-103">Megkapja az API-t.</span><span class="sxs-lookup"><span data-stu-id="33f6f-103">Gets an API.</span></span>

## <span data-ttu-id="33f6f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="33f6f-104">SYNTAX</span></span>

### <span data-ttu-id="33f6f-105">GetAllApis (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="33f6f-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="33f6f-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="33f6f-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33f6f-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="33f6f-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33f6f-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="33f6f-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33f6f-109">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="33f6f-109">GetByGatewayId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33f6f-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="33f6f-110">DESCRIPTION</span></span>
<span data-ttu-id="33f6f-111">A **Get-AzApiManagementApi** parancsmag egy vagy több Azure API-kezelési API-t kap.</span><span class="sxs-lookup"><span data-stu-id="33f6f-111">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="33f6f-112">Példák</span><span class="sxs-lookup"><span data-stu-id="33f6f-112">EXAMPLES</span></span>

### <span data-ttu-id="33f6f-113">Példa 1: az összes felügyeleti API beszerzése</span><span class="sxs-lookup"><span data-stu-id="33f6f-113">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="33f6f-114">Ez a parancs a megadott környezet összes API-t megkapja.</span><span class="sxs-lookup"><span data-stu-id="33f6f-114">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="33f6f-115">2. példa: felügyeleti API beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="33f6f-115">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="33f6f-116">Ez a parancs a megadott AZONOSÍTÓJÚ API-t kapja.</span><span class="sxs-lookup"><span data-stu-id="33f6f-116">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="33f6f-117">3. példa: felügyeleti API beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="33f6f-117">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="33f6f-118">Ez a parancs a megadott nevű API-t kapja.</span><span class="sxs-lookup"><span data-stu-id="33f6f-118">This command gets the API with the specified name.</span></span>

### <span data-ttu-id="33f6f-119">Példa 4: felügyeleti API beszerzése GatewayId</span><span class="sxs-lookup"><span data-stu-id="33f6f-119">Example 4: Get a management API by GatewayId</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -GatewayId "g01"
```

<span data-ttu-id="33f6f-120">Ez a parancs a megadott GatewayId API-t kapja.</span><span class="sxs-lookup"><span data-stu-id="33f6f-120">This command gets the API for the specified GatewayId.</span></span>

## <span data-ttu-id="33f6f-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="33f6f-121">PARAMETERS</span></span>

### <span data-ttu-id="33f6f-122">-ApiId</span><span class="sxs-lookup"><span data-stu-id="33f6f-122">-ApiId</span></span>
<span data-ttu-id="33f6f-123">A beolvasott API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="33f6f-123">Specifies the ID of the API to get.</span></span>

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

### <span data-ttu-id="33f6f-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="33f6f-124">-ApiRevision</span></span>
<span data-ttu-id="33f6f-125">Az adott API-verzió verziószámának verziószáma.</span><span class="sxs-lookup"><span data-stu-id="33f6f-125">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="33f6f-126">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="33f6f-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="33f6f-127">-Környezet</span><span class="sxs-lookup"><span data-stu-id="33f6f-127">-Context</span></span>
<span data-ttu-id="33f6f-128">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="33f6f-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="33f6f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33f6f-129">-DefaultProfile</span></span>
<span data-ttu-id="33f6f-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="33f6f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33f6f-131">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="33f6f-131">-GatewayId</span></span>
<span data-ttu-id="33f6f-132">Ha meg van adva, a program megkísérli az összes átjáró API-t beszerezni.</span><span class="sxs-lookup"><span data-stu-id="33f6f-132">If specified will try to get all Gateway APIs.</span></span>

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

### <span data-ttu-id="33f6f-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="33f6f-133">-Name</span></span>
<span data-ttu-id="33f6f-134">A beolvasott API nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="33f6f-134">Specifies the name of the API to get.</span></span>

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

### <span data-ttu-id="33f6f-135">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="33f6f-135">-ProductId</span></span>
<span data-ttu-id="33f6f-136">Annak a termékeknek az AZONOSÍTÓját adja meg, amelynek az API-t be kell szereznie.</span><span class="sxs-lookup"><span data-stu-id="33f6f-136">Specifies the ID of the product for which to get the API.</span></span>

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

### <span data-ttu-id="33f6f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33f6f-137">CommonParameters</span></span>
<span data-ttu-id="33f6f-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="33f6f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33f6f-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="33f6f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33f6f-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="33f6f-140">INPUTS</span></span>

### <span data-ttu-id="33f6f-141">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="33f6f-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="33f6f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="33f6f-142">System.String</span></span>

## <span data-ttu-id="33f6f-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33f6f-143">OUTPUTS</span></span>

### <span data-ttu-id="33f6f-144">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="33f6f-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="33f6f-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="33f6f-145">NOTES</span></span>

## <span data-ttu-id="33f6f-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33f6f-146">RELATED LINKS</span></span>

[<span data-ttu-id="33f6f-147">Exportálás – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="33f6f-147">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="33f6f-148">Importálás – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="33f6f-148">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="33f6f-149">Új – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="33f6f-149">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="33f6f-150">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="33f6f-150">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="33f6f-151">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="33f6f-151">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


