---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 9673df14bdd0f5b7d0e946170a155231e8c4e751
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342965"
---
# <span data-ttu-id="da439-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="da439-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="da439-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da439-102">SYNOPSIS</span></span>
<span data-ttu-id="da439-103">Egy adott API-kiadás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="da439-103">Removes a particular API Release</span></span>

## <span data-ttu-id="da439-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="da439-104">SYNTAX</span></span>

### <span data-ttu-id="da439-105">ByApiReleaseId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="da439-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da439-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="da439-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da439-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="da439-107">DESCRIPTION</span></span>

<span data-ttu-id="da439-108">A **Remove-AzAzureRmApiManagementApiRelease** parancsmag eltávolít egy meglévő API-kiadást.</span><span class="sxs-lookup"><span data-stu-id="da439-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="da439-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="da439-109">EXAMPLES</span></span>

### <span data-ttu-id="da439-110">1. példa: API-kiadás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="da439-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="da439-111">Ez a parancs eltávolítja az API Release-t a megadott ApiId és ReleaseId értékekkel.</span><span class="sxs-lookup"><span data-stu-id="da439-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="da439-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da439-112">PARAMETERS</span></span>

### <span data-ttu-id="da439-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="da439-113">-ApiId</span></span>
<span data-ttu-id="da439-114">Az API azonosítója.</span><span class="sxs-lookup"><span data-stu-id="da439-114">Identifier of the API.</span></span>
<span data-ttu-id="da439-115">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="da439-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da439-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="da439-116">-Context</span></span>
<span data-ttu-id="da439-117">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="da439-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="da439-118">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="da439-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da439-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da439-119">-DefaultProfile</span></span>
<span data-ttu-id="da439-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da439-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da439-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da439-121">-InputObject</span></span>
<span data-ttu-id="da439-122">A PsApiManagementApiRelease példánya.</span><span class="sxs-lookup"><span data-stu-id="da439-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="da439-123">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="da439-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da439-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da439-124">-PassThru</span></span>
<span data-ttu-id="da439-125">Ha a megadott érték igaz értéket ad meg, akkor a művelet sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="da439-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="da439-126">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="da439-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="da439-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="da439-127">-ReleaseId</span></span>
<span data-ttu-id="da439-128">Az API-kiadás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="da439-128">Identifier of the API Release.</span></span>
<span data-ttu-id="da439-129">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="da439-129">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da439-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da439-130">-Confirm</span></span>
<span data-ttu-id="da439-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="da439-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da439-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da439-132">-WhatIf</span></span>
<span data-ttu-id="da439-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="da439-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da439-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da439-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da439-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da439-135">CommonParameters</span></span>
<span data-ttu-id="da439-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da439-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da439-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da439-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da439-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da439-138">INPUTS</span></span>

### <span data-ttu-id="da439-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="da439-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="da439-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="da439-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="da439-141">System.String</span><span class="sxs-lookup"><span data-stu-id="da439-141">System.String</span></span>

## <span data-ttu-id="da439-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da439-142">OUTPUTS</span></span>

### <span data-ttu-id="da439-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="da439-143">System.Boolean</span></span>

## <span data-ttu-id="da439-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="da439-144">NOTES</span></span>

## <span data-ttu-id="da439-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da439-145">RELATED LINKS</span></span>

[<span data-ttu-id="da439-146">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="da439-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="da439-147">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="da439-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="da439-148">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="da439-148">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)