---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
ms.openlocfilehash: 488f4082007c96a111483d7efac6a8b9a74dba8f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341465"
---
# <span data-ttu-id="8c721-101">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8c721-101">Remove-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="8c721-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c721-102">SYNOPSIS</span></span>
<span data-ttu-id="8c721-103">Távolítsa el a diagnosztikai entitást a globális vagy API-szintű hatókörből.</span><span class="sxs-lookup"><span data-stu-id="8c721-103">Remove the Diagnostic entity from Global or API level scope.</span></span>

## <span data-ttu-id="8c721-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8c721-104">SYNTAX</span></span>

### <span data-ttu-id="8c721-105">ByResourceIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c721-105">ByResourceIdParameterSet (Default)</span></span>
```
Remove-AzApiManagementDiagnostic -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c721-106">ExpandParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8c721-106">ExpandParameterSetName</span></span>
```
Remove-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-ApiId <String>] -DiagnosticId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c721-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c721-107">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c721-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8c721-108">DESCRIPTION</span></span>
<span data-ttu-id="8c721-109">A **Remove-AzApiManagementDiagnostic** parancsmag eltávolítja a globális hatókörből vagy hatókörből a megadott diagnosztikai `DiagnosticId` `ApiId` entitást.</span><span class="sxs-lookup"><span data-stu-id="8c721-109">The cmdlet **Remove-AzApiManagementDiagnostic** removes the diagnostic entity specified by `DiagnosticId` from global scope or an `ApiId` scope</span></span>

## <span data-ttu-id="8c721-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8c721-110">EXAMPLES</span></span>

### <span data-ttu-id="8c721-111">1. példa: A diagnosztikai entitás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8c721-111">Example 1: Remove the Diagnostic entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementDiagnostic -Context $apimContext -DiagnosticId "applicationinsights"
```

<span data-ttu-id="8c721-112">Ez a példa eltávolítja a diagnosztikai `applicationinsights` adatokat az Api Management szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="8c721-112">This example remove the diagnostic `applicationinsights` from the Api Management service.</span></span>

## <span data-ttu-id="8c721-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c721-113">PARAMETERS</span></span>

### <span data-ttu-id="8c721-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8c721-114">-ApiId</span></span>
<span data-ttu-id="8c721-115">Az API azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8c721-115">Identifier of the API.</span></span>
<span data-ttu-id="8c721-116">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8c721-116">This parameter is required.</span></span>

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

### <span data-ttu-id="8c721-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8c721-117">-Context</span></span>
<span data-ttu-id="8c721-118">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="8c721-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8c721-119">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8c721-119">This parameter is required.</span></span>

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

### <span data-ttu-id="8c721-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c721-120">-DefaultProfile</span></span>
<span data-ttu-id="8c721-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c721-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c721-122">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="8c721-122">-DiagnosticId</span></span>
<span data-ttu-id="8c721-123">A meglévő termék azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8c721-123">Identifier of existing product.</span></span>
<span data-ttu-id="8c721-124">Ha meg van adva, akkor a termék hatókörére vonatkozó házirendet ad vissza.</span><span class="sxs-lookup"><span data-stu-id="8c721-124">If specified will return product-scope policy.</span></span>
<span data-ttu-id="8c721-125">A paraméterek megadása nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8c721-125">This parameters is optional.</span></span>

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

### <span data-ttu-id="8c721-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c721-126">-InputObject</span></span>
<span data-ttu-id="8c721-127">A PsApiManagementDiagnostic példánya.</span><span class="sxs-lookup"><span data-stu-id="8c721-127">Instance of PsApiManagementDiagnostic.</span></span> <span data-ttu-id="8c721-128">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8c721-128">This parameter is required.</span></span>

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

### <span data-ttu-id="8c721-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c721-129">-PassThru</span></span>
<span data-ttu-id="8c721-130">Ha a megadott érték igaz értéket ad meg, akkor a művelet sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="8c721-130">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="8c721-131">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8c721-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="8c721-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c721-132">-ResourceId</span></span>
<span data-ttu-id="8c721-133">Diagnosztikai erőforrásazonosító arm.</span><span class="sxs-lookup"><span data-stu-id="8c721-133">Arm ResourceId of Diagnostic.</span></span> <span data-ttu-id="8c721-134">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8c721-134">This parameter is required.</span></span>

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

### <span data-ttu-id="8c721-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c721-135">-Confirm</span></span>
<span data-ttu-id="8c721-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8c721-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c721-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c721-137">-WhatIf</span></span>
<span data-ttu-id="8c721-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8c721-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c721-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c721-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c721-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c721-140">CommonParameters</span></span>
<span data-ttu-id="8c721-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c721-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c721-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c721-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c721-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c721-143">INPUTS</span></span>

### <span data-ttu-id="8c721-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8c721-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8c721-145">System.String</span><span class="sxs-lookup"><span data-stu-id="8c721-145">System.String</span></span>

### <span data-ttu-id="8c721-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8c721-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8c721-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c721-147">OUTPUTS</span></span>

### <span data-ttu-id="8c721-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8c721-148">System.Boolean</span></span>

## <span data-ttu-id="8c721-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8c721-149">NOTES</span></span>

## <span data-ttu-id="8c721-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c721-150">RELATED LINKS</span></span>

[<span data-ttu-id="8c721-151">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8c721-151">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="8c721-152">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8c721-152">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="8c721-153">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8c721-153">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)