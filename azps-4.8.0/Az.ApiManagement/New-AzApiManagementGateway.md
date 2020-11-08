---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
ms.openlocfilehash: c06442ef9ab4b5f80943da33ed87fc24c276107d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180676"
---
# <span data-ttu-id="f0ef1-101">New-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="f0ef1-101">New-AzApiManagementGateway</span></span>

## <span data-ttu-id="f0ef1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f0ef1-102">SYNOPSIS</span></span>
<span data-ttu-id="f0ef1-103">Új átjáró entitás létrehozása</span><span class="sxs-lookup"><span data-stu-id="f0ef1-103">Creates new Gateway entity.</span></span>

## <span data-ttu-id="f0ef1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f0ef1-104">SYNTAX</span></span>

```
New-AzApiManagementGateway -Context <PsApiManagementContext> [-GatewayId <String>] [-Description <String>]
 -LocationData <PsApiManagementResourceLocation> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0ef1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f0ef1-105">DESCRIPTION</span></span>
<span data-ttu-id="f0ef1-106">A **New-AzApiManagementGateway** parancsmag új átjáró entitást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f0ef1-106">The **New-AzApiManagementGateway** cmdlet creates new Gateway entity.</span></span>

## <span data-ttu-id="f0ef1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f0ef1-107">EXAMPLES</span></span>

### <span data-ttu-id="f0ef1-108">Példa 1: átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="f0ef1-108">Example 1: Create a gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
PS C:\>New-AzApiManagementGateway -Context $apimContext -GatewayId "123" -Description "desc" -LocationData $location
```

<span data-ttu-id="f0ef1-109">Ez a parancs átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f0ef1-109">This command creates a gateway.</span></span>

## <span data-ttu-id="f0ef1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f0ef1-110">PARAMETERS</span></span>

### <span data-ttu-id="f0ef1-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f0ef1-111">-Context</span></span>
<span data-ttu-id="f0ef1-112">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="f0ef1-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f0ef1-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="f0ef1-113">This parameter is required.</span></span>

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

### <span data-ttu-id="f0ef1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0ef1-114">-DefaultProfile</span></span>
<span data-ttu-id="f0ef1-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f0ef1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0ef1-116">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f0ef1-116">-Description</span></span>
<span data-ttu-id="f0ef1-117">Átjáró leírása.</span><span class="sxs-lookup"><span data-stu-id="f0ef1-117">Gateway description.</span></span>
<span data-ttu-id="f0ef1-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="f0ef1-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="f0ef1-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="f0ef1-119">-GatewayId</span></span>
<span data-ttu-id="f0ef1-120">Az új átjáró azonosítója</span><span class="sxs-lookup"><span data-stu-id="f0ef1-120">Identifier of new gateway.</span></span>
<span data-ttu-id="f0ef1-121">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="f0ef1-121">This parameter is optional.</span></span>
<span data-ttu-id="f0ef1-122">Ha a program nem adja meg a megadott értéket.</span><span class="sxs-lookup"><span data-stu-id="f0ef1-122">If not specified will be generated.</span></span>

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

### <span data-ttu-id="f0ef1-123">-LocationData</span><span class="sxs-lookup"><span data-stu-id="f0ef1-123">-LocationData</span></span>
<span data-ttu-id="f0ef1-124">Átjáró helye.</span><span class="sxs-lookup"><span data-stu-id="f0ef1-124">Gateway location.</span></span>
<span data-ttu-id="f0ef1-125">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="f0ef1-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ef1-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f0ef1-126">-Confirm</span></span>
<span data-ttu-id="f0ef1-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f0ef1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0ef1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0ef1-128">-WhatIf</span></span>
<span data-ttu-id="f0ef1-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f0ef1-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0ef1-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f0ef1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0ef1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0ef1-131">CommonParameters</span></span>
<span data-ttu-id="f0ef1-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f0ef1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0ef1-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f0ef1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0ef1-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0ef1-134">INPUTS</span></span>

### <span data-ttu-id="f0ef1-135">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f0ef1-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f0ef1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f0ef1-136">System.String</span></span>

### <span data-ttu-id="f0ef1-137">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="f0ef1-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="f0ef1-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0ef1-138">OUTPUTS</span></span>

### <span data-ttu-id="f0ef1-139">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="f0ef1-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="f0ef1-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f0ef1-140">NOTES</span></span>

## <span data-ttu-id="f0ef1-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f0ef1-141">RELATED LINKS</span></span>
