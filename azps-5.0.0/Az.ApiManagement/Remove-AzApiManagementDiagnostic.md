---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
ms.openlocfilehash: 488f4082007c96a111483d7efac6a8b9a74dba8f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188156"
---
# <span data-ttu-id="776d2-101">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="776d2-101">Remove-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="776d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="776d2-102">SYNOPSIS</span></span>
<span data-ttu-id="776d2-103">A diagnosztikai entitás eltávolítása globális vagy API-szintű hatókörből</span><span class="sxs-lookup"><span data-stu-id="776d2-103">Remove the Diagnostic entity from Global or API level scope.</span></span>

## <span data-ttu-id="776d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="776d2-104">SYNTAX</span></span>

### <span data-ttu-id="776d2-105">ByResourceIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="776d2-105">ByResourceIdParameterSet (Default)</span></span>
```
Remove-AzApiManagementDiagnostic -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="776d2-106">ExpandParameterSetName</span><span class="sxs-lookup"><span data-stu-id="776d2-106">ExpandParameterSetName</span></span>
```
Remove-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-ApiId <String>] -DiagnosticId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="776d2-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="776d2-107">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="776d2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="776d2-108">DESCRIPTION</span></span>
<span data-ttu-id="776d2-109">A parancsmag **eltávolítása – AzApiManagementDiagnostic** eltávolítja a `DiagnosticId` globális hatókörből vagy hatókörből megadott diagnosztikai entitást. `ApiId`</span><span class="sxs-lookup"><span data-stu-id="776d2-109">The cmdlet **Remove-AzApiManagementDiagnostic** removes the diagnostic entity specified by `DiagnosticId` from global scope or an `ApiId` scope</span></span>

## <span data-ttu-id="776d2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="776d2-110">EXAMPLES</span></span>

### <span data-ttu-id="776d2-111">1. példa: a diagnosztikai entitás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="776d2-111">Example 1: Remove the Diagnostic entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementDiagnostic -Context $apimContext -DiagnosticId "applicationinsights"
```

<span data-ttu-id="776d2-112">Ez a példa eltávolítja az `applicationinsights` API-menedzsment szolgáltatás diagnosztikai szolgáltatását.</span><span class="sxs-lookup"><span data-stu-id="776d2-112">This example remove the diagnostic `applicationinsights` from the Api Management service.</span></span>

## <span data-ttu-id="776d2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="776d2-113">PARAMETERS</span></span>

### <span data-ttu-id="776d2-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="776d2-114">-ApiId</span></span>
<span data-ttu-id="776d2-115">Az API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="776d2-115">Identifier of the API.</span></span>
<span data-ttu-id="776d2-116">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="776d2-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="776d2-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="776d2-117">-Context</span></span>
<span data-ttu-id="776d2-118">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="776d2-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="776d2-119">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="776d2-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="776d2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="776d2-120">-DefaultProfile</span></span>
<span data-ttu-id="776d2-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="776d2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="776d2-122">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="776d2-122">-DiagnosticId</span></span>
<span data-ttu-id="776d2-123">A meglévő szorzat azonosítója</span><span class="sxs-lookup"><span data-stu-id="776d2-123">Identifier of existing product.</span></span>
<span data-ttu-id="776d2-124">Ha meg van adva a termékek hatókörét visszaadó házirend.</span><span class="sxs-lookup"><span data-stu-id="776d2-124">If specified will return product-scope policy.</span></span>
<span data-ttu-id="776d2-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="776d2-125">This parameters is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="776d2-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="776d2-126">-InputObject</span></span>
<span data-ttu-id="776d2-127">A PsApiManagementDiagnostic példánya.</span><span class="sxs-lookup"><span data-stu-id="776d2-127">Instance of PsApiManagementDiagnostic.</span></span> <span data-ttu-id="776d2-128">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="776d2-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="776d2-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="776d2-129">-PassThru</span></span>
<span data-ttu-id="776d2-130">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="776d2-130">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="776d2-131">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="776d2-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="776d2-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="776d2-132">-ResourceId</span></span>
<span data-ttu-id="776d2-133">A kar ResourceId diagnosztikai nézete.</span><span class="sxs-lookup"><span data-stu-id="776d2-133">Arm ResourceId of Diagnostic.</span></span> <span data-ttu-id="776d2-134">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="776d2-134">This parameter is required.</span></span>

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

### <span data-ttu-id="776d2-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="776d2-135">-Confirm</span></span>
<span data-ttu-id="776d2-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="776d2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="776d2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="776d2-137">-WhatIf</span></span>
<span data-ttu-id="776d2-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="776d2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="776d2-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="776d2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="776d2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="776d2-140">CommonParameters</span></span>
<span data-ttu-id="776d2-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="776d2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="776d2-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="776d2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="776d2-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="776d2-143">INPUTS</span></span>

### <span data-ttu-id="776d2-144">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="776d2-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="776d2-145">System. String</span><span class="sxs-lookup"><span data-stu-id="776d2-145">System.String</span></span>

### <span data-ttu-id="776d2-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="776d2-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="776d2-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="776d2-147">OUTPUTS</span></span>

### <span data-ttu-id="776d2-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="776d2-148">System.Boolean</span></span>

## <span data-ttu-id="776d2-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="776d2-149">NOTES</span></span>

## <span data-ttu-id="776d2-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="776d2-150">RELATED LINKS</span></span>

[<span data-ttu-id="776d2-151">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="776d2-151">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="776d2-152">Új – AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="776d2-152">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="776d2-153">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="776d2-153">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)