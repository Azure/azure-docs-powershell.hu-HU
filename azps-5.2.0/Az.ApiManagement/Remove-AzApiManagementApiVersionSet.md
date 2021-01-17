---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 58a082288a121e5e6b04353bad862edaea4c20fc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342954"
---
# <span data-ttu-id="372ba-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="372ba-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="372ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="372ba-102">SYNOPSIS</span></span>
<span data-ttu-id="372ba-103">Egy adott Api-verziókészlet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="372ba-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="372ba-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="372ba-104">SYNTAX</span></span>

### <span data-ttu-id="372ba-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="372ba-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="372ba-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="372ba-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="372ba-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="372ba-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="372ba-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="372ba-108">DESCRIPTION</span></span>

<span data-ttu-id="372ba-109">A **Remove-AzAzureRmApiManagementApiVersionSet** parancsmag eltávolít egy meglévő API-verziókészletet.</span><span class="sxs-lookup"><span data-stu-id="372ba-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="372ba-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="372ba-110">EXAMPLES</span></span>

### <span data-ttu-id="372ba-111">1. példa: API-verziókészlet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="372ba-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="372ba-112">Ez a parancs eltávolítja az API-verziókészletet a megadott ApiVersionSetId értékekkel.</span><span class="sxs-lookup"><span data-stu-id="372ba-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="372ba-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="372ba-113">PARAMETERS</span></span>

### <span data-ttu-id="372ba-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="372ba-114">-ApiVersionSetId</span></span>
<span data-ttu-id="372ba-115">Az API-verziókészlet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="372ba-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="372ba-116">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="372ba-116">This parameter is required.</span></span>

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

### <span data-ttu-id="372ba-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="372ba-117">-Context</span></span>
<span data-ttu-id="372ba-118">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="372ba-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="372ba-119">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="372ba-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="372ba-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="372ba-120">-DefaultProfile</span></span>
<span data-ttu-id="372ba-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="372ba-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="372ba-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="372ba-122">-InputObject</span></span>
<span data-ttu-id="372ba-123">A PsApiManagementApiVersionSet példánya.</span><span class="sxs-lookup"><span data-stu-id="372ba-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="372ba-124">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="372ba-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="372ba-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="372ba-125">-PassThru</span></span>
<span data-ttu-id="372ba-126">Ha a megadott érték igaz értéket ad meg, akkor a művelet sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="372ba-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="372ba-127">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="372ba-127">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="372ba-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="372ba-128">-ResourceId</span></span>
<span data-ttu-id="372ba-129">Arm ResourceId of ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="372ba-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="372ba-130">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="372ba-130">This parameter is required.</span></span>

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

### <span data-ttu-id="372ba-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="372ba-131">-Confirm</span></span>
<span data-ttu-id="372ba-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="372ba-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="372ba-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="372ba-133">-WhatIf</span></span>
<span data-ttu-id="372ba-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="372ba-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="372ba-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="372ba-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="372ba-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="372ba-136">CommonParameters</span></span>
<span data-ttu-id="372ba-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="372ba-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="372ba-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="372ba-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="372ba-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="372ba-139">INPUTS</span></span>

### <span data-ttu-id="372ba-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="372ba-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="372ba-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="372ba-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="372ba-142">System.String</span><span class="sxs-lookup"><span data-stu-id="372ba-142">System.String</span></span>

## <span data-ttu-id="372ba-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="372ba-143">OUTPUTS</span></span>

### <span data-ttu-id="372ba-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="372ba-144">System.Boolean</span></span>

## <span data-ttu-id="372ba-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="372ba-145">NOTES</span></span>

## <span data-ttu-id="372ba-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="372ba-146">RELATED LINKS</span></span>

[<span data-ttu-id="372ba-147">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="372ba-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="372ba-148">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="372ba-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="372ba-149">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="372ba-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)