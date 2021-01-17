---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: ecdae500b0c1d81635e23ca6ca4bc4c803665912
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478973"
---
# <span data-ttu-id="116c9-101">Get-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="116c9-101">Get-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="116c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="116c9-102">SYNOPSIS</span></span>
<span data-ttu-id="116c9-103">Az összes vagy adott állomásnév-konfigurációt beveszi a meglévő átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="116c9-103">Gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="116c9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="116c9-104">SYNTAX</span></span>

### <span data-ttu-id="116c9-105">GetByGatewayId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="116c9-105">GetByGatewayId (Default)</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="116c9-106">GetByGatewayHostnameId</span><span class="sxs-lookup"><span data-stu-id="116c9-106">GetByGatewayHostnameId</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="116c9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="116c9-107">DESCRIPTION</span></span>
<span data-ttu-id="116c9-108">A **Get-AzApiManagementGatewayHostnameConfiguration** parancsmag az összes vagy adott állomásnév-konfigurációt megkapja a meglévő átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="116c9-108">The **Get-AzApiManagementGatewayHostnameConfiguration** cmdlet gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="116c9-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="116c9-109">EXAMPLES</span></span>

### <span data-ttu-id="116c9-110">1. példa: Az átjáró összes állomásnevének beállítása</span><span class="sxs-lookup"><span data-stu-id="116c9-110">Example 1: Get all hostname configurations for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext  -GatewayId "0123456789"
```

<span data-ttu-id="116c9-111">Ez a parancs egy "0123456789" átjáró összes állomásnevét beveszi.</span><span class="sxs-lookup"><span data-stu-id="116c9-111">This command gets all hostname configurations for a "0123456789" gateway.</span></span>

### <span data-ttu-id="116c9-112">2. példa: Állomásnév beállítása az átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="116c9-112">Example 2: Get a hostname configuration for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "0123456789" -GatewayHostnameConfigurationId "123"
```

<span data-ttu-id="116c9-113">Ez a parancs "123" állomásnév-konfigurációt kap egy "0123456789" átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="116c9-113">This command gets "123" hostname configuration for a "0123456789" gateway.</span></span>

## <span data-ttu-id="116c9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="116c9-114">PARAMETERS</span></span>

### <span data-ttu-id="116c9-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="116c9-115">-Context</span></span>
<span data-ttu-id="116c9-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="116c9-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="116c9-117">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="116c9-117">This parameter is required.</span></span>

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

### <span data-ttu-id="116c9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="116c9-118">-DefaultProfile</span></span>
<span data-ttu-id="116c9-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="116c9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="116c9-120">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="116c9-120">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="116c9-121">Hostname Configuration identifier.</span><span class="sxs-lookup"><span data-stu-id="116c9-121">Hostname Configuration identifier.</span></span>
<span data-ttu-id="116c9-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="116c9-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayHostnameId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="116c9-123">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="116c9-123">-GatewayId</span></span>
<span data-ttu-id="116c9-124">Átjáró azonosítója.</span><span class="sxs-lookup"><span data-stu-id="116c9-124">Gateway identifier.</span></span>
<span data-ttu-id="116c9-125">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="116c9-125">This parameter is required.</span></span>

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

### <span data-ttu-id="116c9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="116c9-126">CommonParameters</span></span>
<span data-ttu-id="116c9-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="116c9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="116c9-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="116c9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="116c9-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="116c9-129">INPUTS</span></span>

### <span data-ttu-id="116c9-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="116c9-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="116c9-131">System.String</span><span class="sxs-lookup"><span data-stu-id="116c9-131">System.String</span></span>

## <span data-ttu-id="116c9-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="116c9-132">OUTPUTS</span></span>

### <span data-ttu-id="116c9-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="116c9-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="116c9-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="116c9-134">NOTES</span></span>

## <span data-ttu-id="116c9-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="116c9-135">RELATED LINKS</span></span>
