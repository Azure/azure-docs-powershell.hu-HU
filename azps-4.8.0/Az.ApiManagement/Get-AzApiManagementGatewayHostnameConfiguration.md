---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: ecdae500b0c1d81635e23ca6ca4bc4c803665912
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184640"
---
# <span data-ttu-id="32ee3-101">Get-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="32ee3-101">Get-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="32ee3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="32ee3-102">SYNOPSIS</span></span>
<span data-ttu-id="32ee3-103">A meglévő átjáró összes vagy konkrét állomásnév-konfigurációjának beolvasása.</span><span class="sxs-lookup"><span data-stu-id="32ee3-103">Gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="32ee3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="32ee3-104">SYNTAX</span></span>

### <span data-ttu-id="32ee3-105">GetByGatewayId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="32ee3-105">GetByGatewayId (Default)</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32ee3-106">GetByGatewayHostnameId</span><span class="sxs-lookup"><span data-stu-id="32ee3-106">GetByGatewayHostnameId</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32ee3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="32ee3-107">DESCRIPTION</span></span>
<span data-ttu-id="32ee3-108">A **Get-AzApiManagementGatewayHostnameConfiguration** parancsmag a meglévő átjáróhoz tartozó összes vagy konkrét állomásnév-konfigurációt kapja.</span><span class="sxs-lookup"><span data-stu-id="32ee3-108">The **Get-AzApiManagementGatewayHostnameConfiguration** cmdlet gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="32ee3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="32ee3-109">EXAMPLES</span></span>

### <span data-ttu-id="32ee3-110">Példa 1: az átjáró összes gépnév-konfigurációjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="32ee3-110">Example 1: Get all hostname configurations for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext  -GatewayId "0123456789"
```

<span data-ttu-id="32ee3-111">Ez a parancs a "0123456789" átjáró minden gépnév-konfigurációját bekapja.</span><span class="sxs-lookup"><span data-stu-id="32ee3-111">This command gets all hostname configurations for a "0123456789" gateway.</span></span>

### <span data-ttu-id="32ee3-112">2. példa: állomásnév-konfiguráció kérése az átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="32ee3-112">Example 2: Get a hostname configuration for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "0123456789" -GatewayHostnameConfigurationId "123"
```

<span data-ttu-id="32ee3-113">Ez a parancs "123" gépnév-konfigurációt kap egy "0123456789" átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="32ee3-113">This command gets "123" hostname configuration for a "0123456789" gateway.</span></span>

## <span data-ttu-id="32ee3-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="32ee3-114">PARAMETERS</span></span>

### <span data-ttu-id="32ee3-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="32ee3-115">-Context</span></span>
<span data-ttu-id="32ee3-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="32ee3-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="32ee3-117">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="32ee3-117">This parameter is required.</span></span>

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

### <span data-ttu-id="32ee3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32ee3-118">-DefaultProfile</span></span>
<span data-ttu-id="32ee3-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="32ee3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32ee3-120">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="32ee3-120">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="32ee3-121">Állomásnév-konfigurációs azonosító</span><span class="sxs-lookup"><span data-stu-id="32ee3-121">Hostname Configuration identifier.</span></span>
<span data-ttu-id="32ee3-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="32ee3-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="32ee3-123">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="32ee3-123">-GatewayId</span></span>
<span data-ttu-id="32ee3-124">Átjáró-azonosító.</span><span class="sxs-lookup"><span data-stu-id="32ee3-124">Gateway identifier.</span></span>
<span data-ttu-id="32ee3-125">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="32ee3-125">This parameter is required.</span></span>

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

### <span data-ttu-id="32ee3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32ee3-126">CommonParameters</span></span>
<span data-ttu-id="32ee3-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="32ee3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32ee3-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="32ee3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32ee3-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="32ee3-129">INPUTS</span></span>

### <span data-ttu-id="32ee3-130">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="32ee3-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="32ee3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="32ee3-131">System.String</span></span>

## <span data-ttu-id="32ee3-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32ee3-132">OUTPUTS</span></span>

### <span data-ttu-id="32ee3-133">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="32ee3-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="32ee3-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="32ee3-134">NOTES</span></span>

## <span data-ttu-id="32ee3-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32ee3-135">RELATED LINKS</span></span>
