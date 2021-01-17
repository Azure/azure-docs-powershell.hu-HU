---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
ms.openlocfilehash: 9b6eac7a0c0c994797de51c936840da515ef3f4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361379"
---
# <span data-ttu-id="0f358-101">Remove-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="0f358-101">Remove-AzApiManagementGateway</span></span>

## <span data-ttu-id="0f358-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f358-102">SYNOPSIS</span></span>
<span data-ttu-id="0f358-103">Leválasztja az API-t az átjáróról.</span><span class="sxs-lookup"><span data-stu-id="0f358-103">Detaches an API from a Gateway.</span></span>

## <span data-ttu-id="0f358-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0f358-104">SYNTAX</span></span>

### <span data-ttu-id="0f358-105">ContextParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0f358-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f358-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f358-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f358-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f358-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGateway -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f358-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0f358-108">DESCRIPTION</span></span>
<span data-ttu-id="0f358-109">A **Remove-AzApiManagementGateway** parancsmag leválasztja az API-t az átjáróról.</span><span class="sxs-lookup"><span data-stu-id="0f358-109">The **Remove-AzApiManagementGateway** cmdlet detaches an API from a Gateway.</span></span>

## <span data-ttu-id="0f358-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0f358-110">EXAMPLES</span></span>

### <span data-ttu-id="0f358-111">1. példa: Meglévő átjáró eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0f358-111">Example 1: Remove an existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGateway -Context $apimContext -GatewayId "g0001" -Force
```

<span data-ttu-id="0f358-112">Ez a parancs eltávolít egy meglévő átjárót, és nem kér megerősítést a felhasználótól.</span><span class="sxs-lookup"><span data-stu-id="0f358-112">This command removes an existing gateway and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="0f358-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f358-113">PARAMETERS</span></span>

### <span data-ttu-id="0f358-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0f358-114">-Context</span></span>
<span data-ttu-id="0f358-115">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="0f358-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0f358-116">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="0f358-116">This parameter is required.</span></span>

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

### <span data-ttu-id="0f358-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f358-117">-DefaultProfile</span></span>
<span data-ttu-id="0f358-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f358-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f358-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="0f358-119">-GatewayId</span></span>
<span data-ttu-id="0f358-120">A meglévő átjáró azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0f358-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="0f358-121">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="0f358-121">This parameter is required.</span></span>

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

### <span data-ttu-id="0f358-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f358-122">-InputObject</span></span>
<span data-ttu-id="0f358-123">A PsApiManagementGateway példánya.</span><span class="sxs-lookup"><span data-stu-id="0f358-123">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="0f358-124">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="0f358-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f358-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f358-125">-PassThru</span></span>
<span data-ttu-id="0f358-126">Ha a megadott érték igaz értéket ad meg, akkor a művelet sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="0f358-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="0f358-127">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="0f358-127">This parameter is optional.</span></span>
<span data-ttu-id="0f358-128">Az alapértelmezett érték hamis.</span><span class="sxs-lookup"><span data-stu-id="0f358-128">Default value is false.</span></span>

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

### <span data-ttu-id="0f358-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f358-129">-ResourceId</span></span>
<span data-ttu-id="0f358-130">Arm ResourceId of the Gateway.</span><span class="sxs-lookup"><span data-stu-id="0f358-130">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="0f358-131">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="0f358-131">This parameter is required.</span></span>

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

### <span data-ttu-id="0f358-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f358-132">-Confirm</span></span>
<span data-ttu-id="0f358-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0f358-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f358-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f358-134">-WhatIf</span></span>
<span data-ttu-id="0f358-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0f358-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f358-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0f358-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f358-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f358-137">CommonParameters</span></span>
<span data-ttu-id="0f358-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f358-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f358-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f358-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f358-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f358-140">INPUTS</span></span>

### <span data-ttu-id="0f358-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0f358-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0f358-142">System.String</span><span class="sxs-lookup"><span data-stu-id="0f358-142">System.String</span></span>

### <span data-ttu-id="0f358-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0f358-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0f358-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f358-144">OUTPUTS</span></span>

### <span data-ttu-id="0f358-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0f358-145">System.Boolean</span></span>

## <span data-ttu-id="0f358-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0f358-146">NOTES</span></span>

## <span data-ttu-id="0f358-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f358-147">RELATED LINKS</span></span>
