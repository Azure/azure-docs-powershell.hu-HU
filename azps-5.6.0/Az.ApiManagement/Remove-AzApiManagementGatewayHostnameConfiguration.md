---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: ad0c40e649384d4fb2bef9220f6ab8a994dea96c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012838"
---
# <span data-ttu-id="5f58a-101">Remove-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f58a-101">Remove-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="5f58a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f58a-102">SYNOPSIS</span></span>
<span data-ttu-id="5f58a-103">Eltávolít egy állomásnév-konfigurációt a meglévő átjáróból.</span><span class="sxs-lookup"><span data-stu-id="5f58a-103">Removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="5f58a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5f58a-104">SYNTAX</span></span>

### <span data-ttu-id="5f58a-105">ContextParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5f58a-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f58a-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f58a-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -InputObject <PsApiManagementGatewayHostnameConfiguration>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f58a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f58a-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f58a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5f58a-108">DESCRIPTION</span></span>
<span data-ttu-id="5f58a-109">A **Remove-AzApiManagementGatewayHostnameConfiguration** parancsmag eltávolít egy állomásnevet a meglévő átjáróból.</span><span class="sxs-lookup"><span data-stu-id="5f58a-109">The **Remove-AzApiManagementGatewayHostnameConfiguration** cmdlet removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="5f58a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5f58a-110">EXAMPLES</span></span>

### <span data-ttu-id="5f58a-111">1. példa: Meglévő átjáró gazdakiszolgáló-konfigurációjának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5f58a-111">Example 1: Remove an existing gateway hostname configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g0001" -GatewayHostnameConfigurationId "h0001" -Force
```

<span data-ttu-id="5f58a-112">Ez a parancs eltávolít egy meglévő átjáró-állomásnevet, és nem kér megerősítést a felhasználótól.</span><span class="sxs-lookup"><span data-stu-id="5f58a-112">This command removes an existing gateway hostname configuration and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="5f58a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f58a-113">PARAMETERS</span></span>

### <span data-ttu-id="5f58a-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5f58a-114">-Context</span></span>
<span data-ttu-id="5f58a-115">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="5f58a-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5f58a-116">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="5f58a-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f58a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f58a-117">-DefaultProfile</span></span>
<span data-ttu-id="5f58a-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5f58a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f58a-119">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5f58a-119">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="5f58a-120">A meglévő átjáró gazdakiszolgáló-konfigurációjának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5f58a-120">Identifier of existing gateway hostname configuration.</span></span>
<span data-ttu-id="5f58a-121">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="5f58a-121">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f58a-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="5f58a-122">-GatewayId</span></span>
<span data-ttu-id="5f58a-123">A meglévő átjáró azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5f58a-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="5f58a-124">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="5f58a-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f58a-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f58a-125">-InputObject</span></span>
<span data-ttu-id="5f58a-126">A PsApiManagementGatewayHostnameConfiguration példánya.</span><span class="sxs-lookup"><span data-stu-id="5f58a-126">Instance of PsApiManagementGatewayHostnameConfiguration.</span></span> <span data-ttu-id="5f58a-127">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="5f58a-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f58a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5f58a-128">-PassThru</span></span>
<span data-ttu-id="5f58a-129">Ha a megadott érték igaz értéket ad meg, akkor a művelet sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="5f58a-129">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="5f58a-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5f58a-130">This parameter is optional.</span></span>
<span data-ttu-id="5f58a-131">Az alapértelmezett érték hamis.</span><span class="sxs-lookup"><span data-stu-id="5f58a-131">Default value is false.</span></span>

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

### <span data-ttu-id="5f58a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f58a-132">-ResourceId</span></span>
<span data-ttu-id="5f58a-133">Arm ResourceId of the GatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5f58a-133">Arm ResourceId of the GatewayHostnameConfiguration.</span></span> <span data-ttu-id="5f58a-134">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="5f58a-134">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f58a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f58a-135">-Confirm</span></span>
<span data-ttu-id="5f58a-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5f58a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f58a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f58a-137">-WhatIf</span></span>
<span data-ttu-id="5f58a-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5f58a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f58a-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5f58a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f58a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f58a-140">CommonParameters</span></span>
<span data-ttu-id="5f58a-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f58a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f58a-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f58a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f58a-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5f58a-143">INPUTS</span></span>

### <span data-ttu-id="5f58a-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5f58a-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5f58a-145">System.String</span><span class="sxs-lookup"><span data-stu-id="5f58a-145">System.String</span></span>

### <span data-ttu-id="5f58a-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5f58a-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5f58a-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f58a-147">OUTPUTS</span></span>

### <span data-ttu-id="5f58a-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5f58a-148">System.Boolean</span></span>

## <span data-ttu-id="5f58a-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5f58a-149">NOTES</span></span>

## <span data-ttu-id="5f58a-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f58a-150">RELATED LINKS</span></span>
