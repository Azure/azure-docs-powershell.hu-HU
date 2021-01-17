---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
ms.openlocfilehash: 80b059a82264cf7d0adedbfca477616abcaa232d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478970"
---
# <span data-ttu-id="a146b-101">Get-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="a146b-101">Get-AzApiManagementGateway</span></span>

## <span data-ttu-id="a146b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a146b-102">SYNOPSIS</span></span>
<span data-ttu-id="a146b-103">Az összes vagy adott API-kezelési átjárót beveszi.</span><span class="sxs-lookup"><span data-stu-id="a146b-103">Gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="a146b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a146b-104">SYNTAX</span></span>

### <span data-ttu-id="a146b-105">GetAllGateways (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a146b-105">GetAllGateways (Default)</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a146b-106">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="a146b-106">GetByGatewayId</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a146b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a146b-107">DESCRIPTION</span></span>
<span data-ttu-id="a146b-108">A **Get-AzApiManagementGateway** parancsmag az összes vagy adott API-kezelési átjárót megkapja.</span><span class="sxs-lookup"><span data-stu-id="a146b-108">The **Get-AzApiManagementGateway** cmdlet gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="a146b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a146b-109">EXAMPLES</span></span>

### <span data-ttu-id="a146b-110">1. példa: Az összes átjáró lekérte</span><span class="sxs-lookup"><span data-stu-id="a146b-110">Example 1: Get all gateways</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext
```

<span data-ttu-id="a146b-111">Ez a parancs az összes átjárót megkapja.</span><span class="sxs-lookup"><span data-stu-id="a146b-111">This command gets all gateways.</span></span>

### <span data-ttu-id="a146b-112">2. példa: Átjáró létrehozása azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="a146b-112">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="a146b-113">Ez a parancs a 0123456789-es átjárót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a146b-113">This command gets the gateway 0123456789.</span></span>

## <span data-ttu-id="a146b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a146b-114">PARAMETERS</span></span>

### <span data-ttu-id="a146b-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a146b-115">-Context</span></span>
<span data-ttu-id="a146b-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="a146b-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a146b-117">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="a146b-117">This parameter is required.</span></span>

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

### <span data-ttu-id="a146b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a146b-118">-DefaultProfile</span></span>
<span data-ttu-id="a146b-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a146b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a146b-120">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="a146b-120">-GatewayId</span></span>
<span data-ttu-id="a146b-121">Egy átjáró azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a146b-121">Identifier of a gateway.</span></span>
<span data-ttu-id="a146b-122">Ha meg van adva, az átjárót az azonosító alapján próbálja megtalálni.</span><span class="sxs-lookup"><span data-stu-id="a146b-122">If specified will try to find gateway by the identifier.</span></span>

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

### <span data-ttu-id="a146b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a146b-123">CommonParameters</span></span>
<span data-ttu-id="a146b-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a146b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a146b-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a146b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a146b-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a146b-126">INPUTS</span></span>

### <span data-ttu-id="a146b-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a146b-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a146b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a146b-128">System.String</span></span>

## <span data-ttu-id="a146b-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a146b-129">OUTPUTS</span></span>

### <span data-ttu-id="a146b-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="a146b-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="a146b-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a146b-131">NOTES</span></span>

## <span data-ttu-id="a146b-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a146b-132">RELATED LINKS</span></span>
