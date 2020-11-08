---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: e1999387cc2beb5a55fba3aef771a76440804f22
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188152"
---
# <span data-ttu-id="54516-101">Remove-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="54516-101">Remove-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="54516-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54516-102">SYNOPSIS</span></span>
<span data-ttu-id="54516-103">A meglévő Átjáróból eltávolítja a gépnév konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="54516-103">Removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="54516-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54516-104">SYNTAX</span></span>

### <span data-ttu-id="54516-105">ContextParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="54516-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54516-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54516-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -InputObject <PsApiManagementGatewayHostnameConfiguration>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54516-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="54516-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54516-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="54516-108">DESCRIPTION</span></span>
<span data-ttu-id="54516-109">A **Remove-AzApiManagementGatewayHostnameConfiguration** parancsmag eltávolítja a gépnév konfigurációját a meglévő átjáróból.</span><span class="sxs-lookup"><span data-stu-id="54516-109">The **Remove-AzApiManagementGatewayHostnameConfiguration** cmdlet removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="54516-110">Példák</span><span class="sxs-lookup"><span data-stu-id="54516-110">EXAMPLES</span></span>

### <span data-ttu-id="54516-111">1. példa: meglévő átjáró-állomásnév konfigurációjának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="54516-111">Example 1: Remove an existing gateway hostname configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g0001" -GatewayHostnameConfigurationId "h0001" -Force
```

<span data-ttu-id="54516-112">Ez a parancs eltávolítja a meglévő átjáró-állomásnevek konfigurációját, és nem kéri a felhasználótól a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="54516-112">This command removes an existing gateway hostname configuration and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="54516-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54516-113">PARAMETERS</span></span>

### <span data-ttu-id="54516-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="54516-114">-Context</span></span>
<span data-ttu-id="54516-115">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="54516-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="54516-116">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="54516-116">This parameter is required.</span></span>

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

### <span data-ttu-id="54516-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54516-117">-DefaultProfile</span></span>
<span data-ttu-id="54516-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54516-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54516-119">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="54516-119">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="54516-120">A meglévő átjáró gépnév-konfigurációjának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="54516-120">Identifier of existing gateway hostname configuration.</span></span>
<span data-ttu-id="54516-121">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="54516-121">This parameter is required.</span></span>

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

### <span data-ttu-id="54516-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="54516-122">-GatewayId</span></span>
<span data-ttu-id="54516-123">A meglévő átjáró azonosítója</span><span class="sxs-lookup"><span data-stu-id="54516-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="54516-124">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="54516-124">This parameter is required.</span></span>

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

### <span data-ttu-id="54516-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54516-125">-InputObject</span></span>
<span data-ttu-id="54516-126">A PsApiManagementGatewayHostnameConfiguration példánya.</span><span class="sxs-lookup"><span data-stu-id="54516-126">Instance of PsApiManagementGatewayHostnameConfiguration.</span></span> <span data-ttu-id="54516-127">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="54516-127">This parameter is required.</span></span>

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

### <span data-ttu-id="54516-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54516-128">-PassThru</span></span>
<span data-ttu-id="54516-129">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="54516-129">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="54516-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="54516-130">This parameter is optional.</span></span>
<span data-ttu-id="54516-131">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="54516-131">Default value is false.</span></span>

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

### <span data-ttu-id="54516-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54516-132">-ResourceId</span></span>
<span data-ttu-id="54516-133">A GatewayHostnameConfiguration kar ResourceId</span><span class="sxs-lookup"><span data-stu-id="54516-133">Arm ResourceId of the GatewayHostnameConfiguration.</span></span> <span data-ttu-id="54516-134">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="54516-134">This parameter is required.</span></span>

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

### <span data-ttu-id="54516-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="54516-135">-Confirm</span></span>
<span data-ttu-id="54516-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="54516-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54516-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54516-137">-WhatIf</span></span>
<span data-ttu-id="54516-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="54516-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54516-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="54516-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54516-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54516-140">CommonParameters</span></span>
<span data-ttu-id="54516-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54516-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54516-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="54516-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54516-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54516-143">INPUTS</span></span>

### <span data-ttu-id="54516-144">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="54516-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="54516-145">System. String</span><span class="sxs-lookup"><span data-stu-id="54516-145">System.String</span></span>

### <span data-ttu-id="54516-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="54516-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="54516-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54516-147">OUTPUTS</span></span>

### <span data-ttu-id="54516-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="54516-148">System.Boolean</span></span>

## <span data-ttu-id="54516-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54516-149">NOTES</span></span>

## <span data-ttu-id="54516-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54516-150">RELATED LINKS</span></span>