---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/Update-AzApiManagementGateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
ms.openlocfilehash: d053bc60390c43c3409bb7adfad5a3ff3720f5b7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381553"
---
# <span data-ttu-id="225eb-101">Update-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="225eb-101">Update-AzApiManagementGateway</span></span>

## <span data-ttu-id="225eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="225eb-102">SYNOPSIS</span></span>
<span data-ttu-id="225eb-103">Konfigurál egy API-kezelési átjárót.</span><span class="sxs-lookup"><span data-stu-id="225eb-103">Configures an API management Gateway.</span></span>

## <span data-ttu-id="225eb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="225eb-104">SYNTAX</span></span>

### <span data-ttu-id="225eb-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="225eb-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="225eb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="225eb-106">ByInputObject</span></span>
```
Update-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="225eb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="225eb-107">ByResourceId</span></span>
```
Update-AzApiManagementGateway -ResourceId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="225eb-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="225eb-108">DESCRIPTION</span></span>
<span data-ttu-id="225eb-109">Az **Update-AzApiManagementGateway** parancsmag konfigurálja az API-kezelési átjárót.</span><span class="sxs-lookup"><span data-stu-id="225eb-109">The **Update-AzApiManagementGateway** cmdlet configures an API management Gateway.</span></span>

## <span data-ttu-id="225eb-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="225eb-110">EXAMPLES</span></span>

### <span data-ttu-id="225eb-111">1. példa: Felügyeleti csoport konfigurálása</span><span class="sxs-lookup"><span data-stu-id="225eb-111">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementGateway -Context $apimContext -GatewayId "0001" -Description "Updated Gateway"
```

<span data-ttu-id="225eb-112">Ez a parancs konfigurál egy átjárót.</span><span class="sxs-lookup"><span data-stu-id="225eb-112">This command configures a gateway.</span></span>

## <span data-ttu-id="225eb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="225eb-113">PARAMETERS</span></span>

### <span data-ttu-id="225eb-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="225eb-114">-Context</span></span>
<span data-ttu-id="225eb-115">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="225eb-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="225eb-116">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="225eb-116">This parameter is required.</span></span>

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

### <span data-ttu-id="225eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="225eb-117">-DefaultProfile</span></span>
<span data-ttu-id="225eb-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="225eb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="225eb-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="225eb-119">-Description</span></span>
<span data-ttu-id="225eb-120">Az átjáró leírása.</span><span class="sxs-lookup"><span data-stu-id="225eb-120">Gateway description.</span></span>
<span data-ttu-id="225eb-121">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="225eb-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="225eb-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="225eb-122">-GatewayId</span></span>
<span data-ttu-id="225eb-123">A meglévő átjáró azonosítója.</span><span class="sxs-lookup"><span data-stu-id="225eb-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="225eb-124">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="225eb-124">This parameter is required.</span></span>

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

### <span data-ttu-id="225eb-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="225eb-125">-InputObject</span></span>
<span data-ttu-id="225eb-126">A PsApiManagementGateway példánya.</span><span class="sxs-lookup"><span data-stu-id="225eb-126">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="225eb-127">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="225eb-127">This parameter is required.</span></span>

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

### <span data-ttu-id="225eb-128">-LocationData</span><span class="sxs-lookup"><span data-stu-id="225eb-128">-LocationData</span></span>
<span data-ttu-id="225eb-129">Átjáró helye.</span><span class="sxs-lookup"><span data-stu-id="225eb-129">Gateway location.</span></span>
<span data-ttu-id="225eb-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="225eb-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="225eb-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="225eb-131">-PassThru</span></span>
<span data-ttu-id="225eb-132">Ha ez meg van adva, akkor a Módosított átjárót képviselő Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway típusú példány.</span><span class="sxs-lookup"><span data-stu-id="225eb-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway type representing the modified gateway.</span></span>

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

### <span data-ttu-id="225eb-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="225eb-133">-ResourceId</span></span>
<span data-ttu-id="225eb-134">Arm ResourceId of the Gateway.</span><span class="sxs-lookup"><span data-stu-id="225eb-134">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="225eb-135">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="225eb-135">This parameter is required.</span></span>

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

### <span data-ttu-id="225eb-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="225eb-136">-Confirm</span></span>
<span data-ttu-id="225eb-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="225eb-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="225eb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="225eb-138">-WhatIf</span></span>
<span data-ttu-id="225eb-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="225eb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="225eb-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="225eb-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="225eb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="225eb-141">CommonParameters</span></span>
<span data-ttu-id="225eb-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="225eb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="225eb-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="225eb-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="225eb-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="225eb-144">INPUTS</span></span>

### <span data-ttu-id="225eb-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="225eb-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="225eb-146">System.String</span><span class="sxs-lookup"><span data-stu-id="225eb-146">System.String</span></span>

### <span data-ttu-id="225eb-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="225eb-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

### <span data-ttu-id="225eb-148">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="225eb-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="225eb-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="225eb-149">OUTPUTS</span></span>

### <span data-ttu-id="225eb-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="225eb-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="225eb-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="225eb-151">NOTES</span></span>

## <span data-ttu-id="225eb-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="225eb-152">RELATED LINKS</span></span>
