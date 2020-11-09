---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/Update-AzApiManagementGateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
ms.openlocfilehash: d053bc60390c43c3409bb7adfad5a3ff3720f5b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303857"
---
# <span data-ttu-id="ec0b5-101">Update-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="ec0b5-101">Update-AzApiManagementGateway</span></span>

## <span data-ttu-id="ec0b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec0b5-102">SYNOPSIS</span></span>
<span data-ttu-id="ec0b5-103">API-kezelési átjáró beállítása.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-103">Configures an API management Gateway.</span></span>

## <span data-ttu-id="ec0b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec0b5-104">SYNTAX</span></span>

### <span data-ttu-id="ec0b5-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ec0b5-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec0b5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ec0b5-106">ByInputObject</span></span>
```
Update-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec0b5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ec0b5-107">ByResourceId</span></span>
```
Update-AzApiManagementGateway -ResourceId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec0b5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec0b5-108">DESCRIPTION</span></span>
<span data-ttu-id="ec0b5-109">Az **Update-AzApiManagementGateway** parancsmag API-kezelési átjárót állít be.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-109">The **Update-AzApiManagementGateway** cmdlet configures an API management Gateway.</span></span>

## <span data-ttu-id="ec0b5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ec0b5-110">EXAMPLES</span></span>

### <span data-ttu-id="ec0b5-111">Példa 1: felügyeleti csoport beállítása</span><span class="sxs-lookup"><span data-stu-id="ec0b5-111">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementGateway -Context $apimContext -GatewayId "0001" -Description "Updated Gateway"
```

<span data-ttu-id="ec0b5-112">Ez a parancs átjárót konfigurál.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-112">This command configures a gateway.</span></span>

## <span data-ttu-id="ec0b5-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec0b5-113">PARAMETERS</span></span>

### <span data-ttu-id="ec0b5-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ec0b5-114">-Context</span></span>
<span data-ttu-id="ec0b5-115">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ec0b5-116">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-116">This parameter is required.</span></span>

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

### <span data-ttu-id="ec0b5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec0b5-117">-DefaultProfile</span></span>
<span data-ttu-id="ec0b5-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec0b5-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="ec0b5-119">-Description</span></span>
<span data-ttu-id="ec0b5-120">Átjáró leírása.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-120">Gateway description.</span></span>
<span data-ttu-id="ec0b5-121">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="ec0b5-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="ec0b5-122">-GatewayId</span></span>
<span data-ttu-id="ec0b5-123">A meglévő átjáró azonosítója</span><span class="sxs-lookup"><span data-stu-id="ec0b5-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="ec0b5-124">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-124">This parameter is required.</span></span>

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

### <span data-ttu-id="ec0b5-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec0b5-125">-InputObject</span></span>
<span data-ttu-id="ec0b5-126">A PsApiManagementGateway példánya.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-126">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="ec0b5-127">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-127">This parameter is required.</span></span>

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

### <span data-ttu-id="ec0b5-128">-LocationData</span><span class="sxs-lookup"><span data-stu-id="ec0b5-128">-LocationData</span></span>
<span data-ttu-id="ec0b5-129">Átjáró helye.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-129">Gateway location.</span></span>
<span data-ttu-id="ec0b5-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="ec0b5-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec0b5-131">-PassThru</span></span>
<span data-ttu-id="ec0b5-132">Ha az adott esetben a Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementGateway típusa a módosított átjárót jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway type representing the modified gateway.</span></span>

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

### <span data-ttu-id="ec0b5-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec0b5-133">-ResourceId</span></span>
<span data-ttu-id="ec0b5-134">A kar ResourceId az átjáróról.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-134">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="ec0b5-135">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-135">This parameter is required.</span></span>

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

### <span data-ttu-id="ec0b5-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ec0b5-136">-Confirm</span></span>
<span data-ttu-id="ec0b5-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec0b5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec0b5-138">-WhatIf</span></span>
<span data-ttu-id="ec0b5-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec0b5-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec0b5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec0b5-141">CommonParameters</span></span>
<span data-ttu-id="ec0b5-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec0b5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec0b5-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec0b5-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec0b5-144">INPUTS</span></span>

### <span data-ttu-id="ec0b5-145">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ec0b5-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ec0b5-146">System. String</span><span class="sxs-lookup"><span data-stu-id="ec0b5-146">System.String</span></span>

### <span data-ttu-id="ec0b5-147">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="ec0b5-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

### <span data-ttu-id="ec0b5-148">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ec0b5-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ec0b5-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec0b5-149">OUTPUTS</span></span>

### <span data-ttu-id="ec0b5-150">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="ec0b5-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="ec0b5-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec0b5-151">NOTES</span></span>

## <span data-ttu-id="ec0b5-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec0b5-152">RELATED LINKS</span></span>
