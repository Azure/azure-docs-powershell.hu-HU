---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/add-azapimanagementapitogateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
ms.openlocfilehash: 9c6d556845192a4bd6e5d6c856d113be4a4074a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929122"
---
# <span data-ttu-id="8449e-101">Add-AzApiManagementApiToGateway</span><span class="sxs-lookup"><span data-stu-id="8449e-101">Add-AzApiManagementApiToGateway</span></span>

## <span data-ttu-id="8449e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8449e-102">SYNOPSIS</span></span>
<span data-ttu-id="8449e-103">API-t csatol egy átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="8449e-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="8449e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8449e-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-ProvisioningState <PsApiManagementGatewayApiProvisioningState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8449e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8449e-105">DESCRIPTION</span></span>
<span data-ttu-id="8449e-106">Az **Add-AzApiManagementApiToGateway** parancsmag hozzáad egy Azure API Felügyeleti API-t egy átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="8449e-106">The **Add-AzApiManagementApiToGateway** cmdlet adds an Azure API Management API to a Gateway.</span></span>

## <span data-ttu-id="8449e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8449e-107">EXAMPLES</span></span>

### <span data-ttu-id="8449e-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="8449e-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001"
```

<span data-ttu-id="8449e-109">Ez a parancs hozzáadja a megadott API-t a megadott átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="8449e-109">This command adds the specified API to the specified Gateway.</span></span>

## <span data-ttu-id="8449e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8449e-110">PARAMETERS</span></span>

### <span data-ttu-id="8449e-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8449e-111">-ApiId</span></span>
<span data-ttu-id="8449e-112">A meglévő API azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8449e-112">Identifier of existing API.</span></span>
<span data-ttu-id="8449e-113">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8449e-113">This parameter is required.</span></span>

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

### <span data-ttu-id="8449e-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8449e-114">-Context</span></span>
<span data-ttu-id="8449e-115">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="8449e-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8449e-116">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8449e-116">This parameter is required.</span></span>

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

### <span data-ttu-id="8449e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8449e-117">-DefaultProfile</span></span>
<span data-ttu-id="8449e-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8449e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8449e-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="8449e-119">-GatewayId</span></span>
<span data-ttu-id="8449e-120">A meglévő átjáró azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8449e-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="8449e-121">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8449e-121">This parameter is required.</span></span>

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

### <span data-ttu-id="8449e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8449e-122">-PassThru</span></span>
<span data-ttu-id="8449e-123">Ha a megadott érték igaz értéket ad meg, akkor a művelet sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="8449e-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="8449e-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8449e-124">This parameter is optional.</span></span>
<span data-ttu-id="8449e-125">Az alapértelmezett érték hamis.</span><span class="sxs-lookup"><span data-stu-id="8449e-125">Default value is false.</span></span>

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

### <span data-ttu-id="8449e-126">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="8449e-126">-ProvisioningState</span></span>
<span data-ttu-id="8449e-127">Kiépítési állapot (létrehozva).</span><span class="sxs-lookup"><span data-stu-id="8449e-127">Provisioning State (Created).</span></span>
<span data-ttu-id="8449e-128">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8449e-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="8449e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8449e-129">-Confirm</span></span>
<span data-ttu-id="8449e-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8449e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8449e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8449e-131">-WhatIf</span></span>
<span data-ttu-id="8449e-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8449e-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8449e-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8449e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8449e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8449e-134">CommonParameters</span></span>
<span data-ttu-id="8449e-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8449e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8449e-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8449e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8449e-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8449e-137">INPUTS</span></span>

### <span data-ttu-id="8449e-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8449e-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8449e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8449e-139">System.String</span></span>

### <span data-ttu-id="8449e-140">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="8449e-140">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="8449e-141">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8449e-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8449e-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8449e-142">OUTPUTS</span></span>

### <span data-ttu-id="8449e-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8449e-143">System.Boolean</span></span>

## <span data-ttu-id="8449e-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8449e-144">NOTES</span></span>

## <span data-ttu-id="8449e-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8449e-145">RELATED LINKS</span></span>

[<span data-ttu-id="8449e-146">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="8449e-146">Remove-AzApiManagementApiFromGateway</span></span>](./Remove-AzApiManagementApiFromGateway.md)