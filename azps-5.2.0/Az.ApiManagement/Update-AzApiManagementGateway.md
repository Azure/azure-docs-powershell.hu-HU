---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/Update-AzApiManagementGateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
ms.openlocfilehash: d053bc60390c43c3409bb7adfad5a3ff3720f5b7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355457"
---
# <span data-ttu-id="043c6-101">Update-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="043c6-101">Update-AzApiManagementGateway</span></span>

## <span data-ttu-id="043c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="043c6-102">SYNOPSIS</span></span>
<span data-ttu-id="043c6-103">Konfigurál egy API-kezelési átjárót.</span><span class="sxs-lookup"><span data-stu-id="043c6-103">Configures an API management Gateway.</span></span>

## <span data-ttu-id="043c6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="043c6-104">SYNTAX</span></span>

### <span data-ttu-id="043c6-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="043c6-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="043c6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="043c6-106">ByInputObject</span></span>
```
Update-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="043c6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="043c6-107">ByResourceId</span></span>
```
Update-AzApiManagementGateway -ResourceId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="043c6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="043c6-108">DESCRIPTION</span></span>
<span data-ttu-id="043c6-109">Az **Update-AzApiManagementGateway** parancsmag konfigurálja az API-kezelési átjárót.</span><span class="sxs-lookup"><span data-stu-id="043c6-109">The **Update-AzApiManagementGateway** cmdlet configures an API management Gateway.</span></span>

## <span data-ttu-id="043c6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="043c6-110">EXAMPLES</span></span>

### <span data-ttu-id="043c6-111">1. példa: Felügyeleti csoport konfigurálása</span><span class="sxs-lookup"><span data-stu-id="043c6-111">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementGateway -Context $apimContext -GatewayId "0001" -Description "Updated Gateway"
```

<span data-ttu-id="043c6-112">Ez a parancs konfigurál egy átjárót.</span><span class="sxs-lookup"><span data-stu-id="043c6-112">This command configures a gateway.</span></span>

## <span data-ttu-id="043c6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="043c6-113">PARAMETERS</span></span>

### <span data-ttu-id="043c6-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="043c6-114">-Context</span></span>
<span data-ttu-id="043c6-115">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="043c6-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="043c6-116">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="043c6-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="043c6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="043c6-117">-DefaultProfile</span></span>
<span data-ttu-id="043c6-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="043c6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="043c6-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="043c6-119">-Description</span></span>
<span data-ttu-id="043c6-120">Az átjáró leírása.</span><span class="sxs-lookup"><span data-stu-id="043c6-120">Gateway description.</span></span>
<span data-ttu-id="043c6-121">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="043c6-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="043c6-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="043c6-122">-GatewayId</span></span>
<span data-ttu-id="043c6-123">A meglévő átjáró azonosítója.</span><span class="sxs-lookup"><span data-stu-id="043c6-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="043c6-124">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="043c6-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="043c6-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="043c6-125">-InputObject</span></span>
<span data-ttu-id="043c6-126">A PsApiManagementGateway példánya.</span><span class="sxs-lookup"><span data-stu-id="043c6-126">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="043c6-127">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="043c6-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="043c6-128">-LocationData</span><span class="sxs-lookup"><span data-stu-id="043c6-128">-LocationData</span></span>
<span data-ttu-id="043c6-129">Átjáró helye.</span><span class="sxs-lookup"><span data-stu-id="043c6-129">Gateway location.</span></span>
<span data-ttu-id="043c6-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="043c6-130">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="043c6-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="043c6-131">-PassThru</span></span>
<span data-ttu-id="043c6-132">Ha a megadott példány a Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway típus, amely a módosított átjárót képviseli.</span><span class="sxs-lookup"><span data-stu-id="043c6-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway type representing the modified gateway.</span></span>

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

### <span data-ttu-id="043c6-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="043c6-133">-ResourceId</span></span>
<span data-ttu-id="043c6-134">Arm ResourceId of the Gateway.</span><span class="sxs-lookup"><span data-stu-id="043c6-134">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="043c6-135">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="043c6-135">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="043c6-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="043c6-136">-Confirm</span></span>
<span data-ttu-id="043c6-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="043c6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="043c6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="043c6-138">-WhatIf</span></span>
<span data-ttu-id="043c6-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="043c6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="043c6-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="043c6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="043c6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="043c6-141">CommonParameters</span></span>
<span data-ttu-id="043c6-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="043c6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="043c6-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="043c6-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="043c6-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="043c6-144">INPUTS</span></span>

### <span data-ttu-id="043c6-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="043c6-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="043c6-146">System.String</span><span class="sxs-lookup"><span data-stu-id="043c6-146">System.String</span></span>

### <span data-ttu-id="043c6-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="043c6-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

### <span data-ttu-id="043c6-148">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="043c6-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="043c6-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="043c6-149">OUTPUTS</span></span>

### <span data-ttu-id="043c6-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="043c6-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="043c6-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="043c6-151">NOTES</span></span>

## <span data-ttu-id="043c6-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="043c6-152">RELATED LINKS</span></span>
