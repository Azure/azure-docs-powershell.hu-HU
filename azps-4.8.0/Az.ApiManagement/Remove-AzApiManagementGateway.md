---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
ms.openlocfilehash: 9b6eac7a0c0c994797de51c936840da515ef3f4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024260"
---
# <span data-ttu-id="0852a-101">Remove-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="0852a-101">Remove-AzApiManagementGateway</span></span>

## <span data-ttu-id="0852a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0852a-102">SYNOPSIS</span></span>
<span data-ttu-id="0852a-103">Az API-t leválasztja egy átjáróról.</span><span class="sxs-lookup"><span data-stu-id="0852a-103">Detaches an API from a Gateway.</span></span>

## <span data-ttu-id="0852a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0852a-104">SYNTAX</span></span>

### <span data-ttu-id="0852a-105">ContextParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0852a-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0852a-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0852a-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0852a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0852a-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGateway -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0852a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0852a-108">DESCRIPTION</span></span>
<span data-ttu-id="0852a-109">A **Remove-AzApiManagementGateway** parancsmag leválasztja az API-t egy átjáróról.</span><span class="sxs-lookup"><span data-stu-id="0852a-109">The **Remove-AzApiManagementGateway** cmdlet detaches an API from a Gateway.</span></span>

## <span data-ttu-id="0852a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0852a-110">EXAMPLES</span></span>

### <span data-ttu-id="0852a-111">1. példa: meglévő átjáró eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0852a-111">Example 1: Remove an existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGateway -Context $apimContext -GatewayId "g0001" -Force
```

<span data-ttu-id="0852a-112">Ez a parancs eltávolítja a meglévő átjárót, és nem kéri a felhasználótól a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0852a-112">This command removes an existing gateway and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="0852a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0852a-113">PARAMETERS</span></span>

### <span data-ttu-id="0852a-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0852a-114">-Context</span></span>
<span data-ttu-id="0852a-115">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="0852a-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0852a-116">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="0852a-116">This parameter is required.</span></span>

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

### <span data-ttu-id="0852a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0852a-117">-DefaultProfile</span></span>
<span data-ttu-id="0852a-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0852a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0852a-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="0852a-119">-GatewayId</span></span>
<span data-ttu-id="0852a-120">A meglévő átjáró azonosítója</span><span class="sxs-lookup"><span data-stu-id="0852a-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="0852a-121">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="0852a-121">This parameter is required.</span></span>

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

### <span data-ttu-id="0852a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0852a-122">-InputObject</span></span>
<span data-ttu-id="0852a-123">A PsApiManagementGateway példánya.</span><span class="sxs-lookup"><span data-stu-id="0852a-123">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="0852a-124">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="0852a-124">This parameter is required.</span></span>

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

### <span data-ttu-id="0852a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0852a-125">-PassThru</span></span>
<span data-ttu-id="0852a-126">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="0852a-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="0852a-127">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="0852a-127">This parameter is optional.</span></span>
<span data-ttu-id="0852a-128">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="0852a-128">Default value is false.</span></span>

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

### <span data-ttu-id="0852a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0852a-129">-ResourceId</span></span>
<span data-ttu-id="0852a-130">A kar ResourceId az átjáróról.</span><span class="sxs-lookup"><span data-stu-id="0852a-130">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="0852a-131">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="0852a-131">This parameter is required.</span></span>

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

### <span data-ttu-id="0852a-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0852a-132">-Confirm</span></span>
<span data-ttu-id="0852a-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0852a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0852a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0852a-134">-WhatIf</span></span>
<span data-ttu-id="0852a-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0852a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0852a-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0852a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0852a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0852a-137">CommonParameters</span></span>
<span data-ttu-id="0852a-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0852a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0852a-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0852a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0852a-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0852a-140">INPUTS</span></span>

### <span data-ttu-id="0852a-141">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0852a-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0852a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="0852a-142">System.String</span></span>

### <span data-ttu-id="0852a-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0852a-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0852a-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0852a-144">OUTPUTS</span></span>

### <span data-ttu-id="0852a-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0852a-145">System.Boolean</span></span>

## <span data-ttu-id="0852a-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0852a-146">NOTES</span></span>

## <span data-ttu-id="0852a-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0852a-147">RELATED LINKS</span></span>
