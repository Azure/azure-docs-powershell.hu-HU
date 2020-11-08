---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
ms.openlocfilehash: 80b059a82264cf7d0adedbfca477616abcaa232d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184643"
---
# <span data-ttu-id="e8523-101">Get-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="e8523-101">Get-AzApiManagementGateway</span></span>

## <span data-ttu-id="e8523-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8523-102">SYNOPSIS</span></span>
<span data-ttu-id="e8523-103">Beolvassa az API-kezelési átjárót.</span><span class="sxs-lookup"><span data-stu-id="e8523-103">Gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="e8523-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8523-104">SYNTAX</span></span>

### <span data-ttu-id="e8523-105">GetAllGateways (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e8523-105">GetAllGateways (Default)</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8523-106">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="e8523-106">GetByGatewayId</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8523-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8523-107">DESCRIPTION</span></span>
<span data-ttu-id="e8523-108">A **Get-AzApiManagementGateway** PARANCSMAG az API-kezelési átjárókat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e8523-108">The **Get-AzApiManagementGateway** cmdlet gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="e8523-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e8523-109">EXAMPLES</span></span>

### <span data-ttu-id="e8523-110">Példa 1: az összes átjáró beolvasása</span><span class="sxs-lookup"><span data-stu-id="e8523-110">Example 1: Get all gateways</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext
```

<span data-ttu-id="e8523-111">Ez a parancs beilleszti az összes átjárót.</span><span class="sxs-lookup"><span data-stu-id="e8523-111">This command gets all gateways.</span></span>

### <span data-ttu-id="e8523-112">2. példa: átjáró beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="e8523-112">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="e8523-113">Ez a parancs a 0123456789 átjárót kapja.</span><span class="sxs-lookup"><span data-stu-id="e8523-113">This command gets the gateway 0123456789.</span></span>

## <span data-ttu-id="e8523-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8523-114">PARAMETERS</span></span>

### <span data-ttu-id="e8523-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e8523-115">-Context</span></span>
<span data-ttu-id="e8523-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="e8523-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e8523-117">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="e8523-117">This parameter is required.</span></span>

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

### <span data-ttu-id="e8523-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8523-118">-DefaultProfile</span></span>
<span data-ttu-id="e8523-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8523-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8523-120">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="e8523-120">-GatewayId</span></span>
<span data-ttu-id="e8523-121">Átjáró azonosítója</span><span class="sxs-lookup"><span data-stu-id="e8523-121">Identifier of a gateway.</span></span>
<span data-ttu-id="e8523-122">Ha meg van adva, az azonosító megkeresésével megpróbálja megtalálni az átjárót.</span><span class="sxs-lookup"><span data-stu-id="e8523-122">If specified will try to find gateway by the identifier.</span></span>

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

### <span data-ttu-id="e8523-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8523-123">CommonParameters</span></span>
<span data-ttu-id="e8523-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8523-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8523-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e8523-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8523-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8523-126">INPUTS</span></span>

### <span data-ttu-id="e8523-127">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e8523-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e8523-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e8523-128">System.String</span></span>

## <span data-ttu-id="e8523-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8523-129">OUTPUTS</span></span>

### <span data-ttu-id="e8523-130">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="e8523-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="e8523-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8523-131">NOTES</span></span>

## <span data-ttu-id="e8523-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8523-132">RELATED LINKS</span></span>
