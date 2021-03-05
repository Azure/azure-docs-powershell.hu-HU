---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/Update-AzApiManagementGateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
ms.openlocfilehash: 62131f634d049afe137b635d6a970d37e2173b8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001926"
---
# <span data-ttu-id="5f6f5-101">Update-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="5f6f5-101">Update-AzApiManagementGateway</span></span>

## <span data-ttu-id="5f6f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f6f5-102">SYNOPSIS</span></span>
<span data-ttu-id="5f6f5-103">Konfigurál egy API-kezelési átjárót.</span><span class="sxs-lookup"><span data-stu-id="5f6f5-103">Configures an API management Gateway.</span></span>

## <span data-ttu-id="5f6f5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5f6f5-104">SYNTAX</span></span>

### <span data-ttu-id="5f6f5-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5f6f5-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f6f5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5f6f5-106">ByInputObject</span></span>
```
Update-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f6f5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5f6f5-107">ByResourceId</span></span>
```
Update-AzApiManagementGateway -ResourceId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f6f5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5f6f5-108">DESCRIPTION</span></span>
<span data-ttu-id="5f6f5-109">Az **Update-AzApiManagementGateway** parancsmag konfigurálja az API-kezelési átjárót.</span><span class="sxs-lookup"><span data-stu-id="5f6f5-109">The **Update-AzApiManagementGateway** cmdlet configures an API management Gateway.</span></span>

## <span data-ttu-id="5f6f5-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5f6f5-110">EXAMPLES</span></span>

### <span data-ttu-id="5f6f5-111">1. példa: Felügyeleti csoport konfigurálása</span><span class="sxs-lookup"><span data-stu-id="5f6f5-111">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementGateway -Context $apimContext -GatewayId "0001" -Description "Updated Gateway"
```

<span data-ttu-id="5f6f5-112">Ez a parancs konfigurál egy átjárót.</span><span class="sxs-lookup"><span data-stu-id="5f6f5-112">This command configures a gateway.</span></span>

## <span data-ttu-id="5f6f5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f6f5-113">PARAMETERS</span></span>

### <span data-ttu-id="5f6f5-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5f6f5-114">-Context</span></span>
<span data-ttu-id="5f6f5-115">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="5f6f5-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5f6f5-116">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="5f6f5-116">This parameter is required.</span></span>

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

### <span data-ttu-id="5f6f5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f6f5-117">-DefaultProfile</span></span>
<span data-ttu-id="5f6f5-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5f6f5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f6f5-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="5f6f5-119">-Description</span></span>
<span data-ttu-id="5f6f5-120">Az átjáró leírása.</span><span class="sxs-lookup"><span data-stu-id="5f6f5-120">Gateway description.</span></span>
<span data-ttu-id="5f6f5-121">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5f6f5-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="5f6f5-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="5f6f5-122">-GatewayId</span></span>
<span data-ttu-id="5f6f5-123">A meglévő átjáró azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5f6f5-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="5f6f5-124">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="5f6f5-124">This parameter is required.</span></span>

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

### <span data-ttu-id="5f6f5-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f6f5-125">-InputObject</span></span>
<span data-ttu-id="5f6f5-126">A PsApiManagementGateway példánya.</span><span class="sxs-lookup"><span data-stu-id="5f6f5-126">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="5f6f5-127">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="5f6f5-127">This parameter is required.</span></span>

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

### <span data-ttu-id="5f6f5-128">-LocationData</span><span class="sxs-lookup"><span data-stu-id="5f6f5-128">-LocationData</span></span>
<span data-ttu-id="5f6f5-129">Átjáró helye.</span><span class="sxs-lookup"><span data-stu-id="5f6f5-129">Gateway location.</span></span>
<span data-ttu-id="5f6f5-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5f6f5-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="5f6f5-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5f6f5-131">-PassThru</span></span>
<span data-ttu-id="5f6f5-132">Ha a megadott példány a Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway típus, amely a módosított átjárót képviseli.</span><span class="sxs-lookup"><span data-stu-id="5f6f5-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway type representing the modified gateway.</span></span>

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

### <span data-ttu-id="5f6f5-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f6f5-133">-ResourceId</span></span>
<span data-ttu-id="5f6f5-134">Arm ResourceId of the Gateway.</span><span class="sxs-lookup"><span data-stu-id="5f6f5-134">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="5f6f5-135">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="5f6f5-135">This parameter is required.</span></span>

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

### <span data-ttu-id="5f6f5-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f6f5-136">-Confirm</span></span>
<span data-ttu-id="5f6f5-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5f6f5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f6f5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f6f5-138">-WhatIf</span></span>
<span data-ttu-id="5f6f5-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5f6f5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f6f5-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5f6f5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f6f5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f6f5-141">CommonParameters</span></span>
<span data-ttu-id="5f6f5-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f6f5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f6f5-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f6f5-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f6f5-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5f6f5-144">INPUTS</span></span>

### <span data-ttu-id="5f6f5-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5f6f5-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5f6f5-146">System.String</span><span class="sxs-lookup"><span data-stu-id="5f6f5-146">System.String</span></span>

### <span data-ttu-id="5f6f5-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="5f6f5-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

### <span data-ttu-id="5f6f5-148">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5f6f5-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5f6f5-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f6f5-149">OUTPUTS</span></span>

### <span data-ttu-id="5f6f5-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="5f6f5-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="5f6f5-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5f6f5-151">NOTES</span></span>

## <span data-ttu-id="5f6f5-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f6f5-152">RELATED LINKS</span></span>
