---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitogateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
ms.openlocfilehash: 6bb40d46c80e609824b1c56d05091ade5716f7f8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025838"
---
# <span data-ttu-id="ffd61-101">Add-AzApiManagementApiToGateway</span><span class="sxs-lookup"><span data-stu-id="ffd61-101">Add-AzApiManagementApiToGateway</span></span>

## <span data-ttu-id="ffd61-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ffd61-102">SYNOPSIS</span></span>
<span data-ttu-id="ffd61-103">API-t csatol az átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="ffd61-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="ffd61-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ffd61-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-ProvisioningState <PsApiManagementGatewayApiProvisioningState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffd61-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ffd61-105">DESCRIPTION</span></span>
<span data-ttu-id="ffd61-106">Az **Add-AzApiManagementApiToGateway** parancsmag egy Azure API-kezelési API-t ad az átjárónak.</span><span class="sxs-lookup"><span data-stu-id="ffd61-106">The **Add-AzApiManagementApiToGateway** cmdlet adds an Azure API Management API to a Gateway.</span></span>

## <span data-ttu-id="ffd61-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ffd61-107">EXAMPLES</span></span>

### <span data-ttu-id="ffd61-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ffd61-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001"
```

<span data-ttu-id="ffd61-109">Ez a parancs hozzáadja a megadott API-t a megadott átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="ffd61-109">This command adds the specified API to the specified Gateway.</span></span>

## <span data-ttu-id="ffd61-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ffd61-110">PARAMETERS</span></span>

### <span data-ttu-id="ffd61-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ffd61-111">-ApiId</span></span>
<span data-ttu-id="ffd61-112">A meglévő API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ffd61-112">Identifier of existing API.</span></span>
<span data-ttu-id="ffd61-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="ffd61-113">This parameter is required.</span></span>

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

### <span data-ttu-id="ffd61-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ffd61-114">-Context</span></span>
<span data-ttu-id="ffd61-115">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="ffd61-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ffd61-116">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="ffd61-116">This parameter is required.</span></span>

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

### <span data-ttu-id="ffd61-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffd61-117">-DefaultProfile</span></span>
<span data-ttu-id="ffd61-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ffd61-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffd61-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="ffd61-119">-GatewayId</span></span>
<span data-ttu-id="ffd61-120">A meglévő átjáró azonosítója</span><span class="sxs-lookup"><span data-stu-id="ffd61-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="ffd61-121">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="ffd61-121">This parameter is required.</span></span>

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

### <span data-ttu-id="ffd61-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ffd61-122">-PassThru</span></span>
<span data-ttu-id="ffd61-123">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="ffd61-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="ffd61-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ffd61-124">This parameter is optional.</span></span>
<span data-ttu-id="ffd61-125">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="ffd61-125">Default value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd61-126">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="ffd61-126">-ProvisioningState</span></span>
<span data-ttu-id="ffd61-127">Kiépítési állapot (létrehozva)</span><span class="sxs-lookup"><span data-stu-id="ffd61-127">Provisioning State (Created).</span></span>
<span data-ttu-id="ffd61-128">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ffd61-128">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState]
Parameter Sets: (All)
Aliases:
Accepted values: Created

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd61-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ffd61-129">-Confirm</span></span>
<span data-ttu-id="ffd61-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ffd61-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffd61-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffd61-131">-WhatIf</span></span>
<span data-ttu-id="ffd61-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ffd61-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ffd61-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ffd61-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffd61-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffd61-134">CommonParameters</span></span>
<span data-ttu-id="ffd61-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ffd61-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffd61-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ffd61-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffd61-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffd61-137">INPUTS</span></span>

### <span data-ttu-id="ffd61-138">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ffd61-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ffd61-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ffd61-139">System.String</span></span>

### <span data-ttu-id="ffd61-140">System. nulla ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementGatewayApiProvisioningState, Microsoft. Azure. PowerShell. parancsmagok. ApiManagement. ServiceManagement, Version = 2.0.1.0, = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ffd61-140">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="ffd61-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ffd61-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ffd61-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffd61-142">OUTPUTS</span></span>

### <span data-ttu-id="ffd61-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ffd61-143">System.Boolean</span></span>

## <span data-ttu-id="ffd61-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ffd61-144">NOTES</span></span>

## <span data-ttu-id="ffd61-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ffd61-145">RELATED LINKS</span></span>

[<span data-ttu-id="ffd61-146">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="ffd61-146">Remove-AzApiManagementApiFromGateway</span></span>](./Remove-AzApiManagementApiFromGateway.md)