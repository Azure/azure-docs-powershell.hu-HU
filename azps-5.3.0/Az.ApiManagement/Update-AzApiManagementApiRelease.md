---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
ms.openlocfilehash: 99ec1234eea582fb91f2722032cb23c27e86b878
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381582"
---
# <span data-ttu-id="0158a-101">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="0158a-101">Update-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="0158a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0158a-102">SYNOPSIS</span></span>
<span data-ttu-id="0158a-103">Frissíti az adott Api-kiadást.</span><span class="sxs-lookup"><span data-stu-id="0158a-103">Updates a particular Api Release.</span></span>

## <span data-ttu-id="0158a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0158a-104">SYNTAX</span></span>

### <span data-ttu-id="0158a-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0158a-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0158a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0158a-106">ByInputObject</span></span>
```
Update-AzApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0158a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0158a-107">DESCRIPTION</span></span>
<span data-ttu-id="0158a-108">Az **Update-AzApiManagementApiRelease** parancsmag módosítja az Azure API Management API-kiadást.</span><span class="sxs-lookup"><span data-stu-id="0158a-108">The **Update-AzApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="0158a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0158a-109">EXAMPLES</span></span>

### <span data-ttu-id="0158a-110">1. példa: Api-kiadás frissítése API-változathoz</span><span class="sxs-lookup"><span data-stu-id="0158a-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="0158a-111">Ez a parancs egy új megjegyzéssel frissíti `echo-api-release` az API API-kiadását. `echo-api`</span><span class="sxs-lookup"><span data-stu-id="0158a-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="0158a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0158a-112">PARAMETERS</span></span>

### <span data-ttu-id="0158a-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0158a-113">-ApiId</span></span>
<span data-ttu-id="0158a-114">A meglévő API azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0158a-114">Identifier of existing API.</span></span>
<span data-ttu-id="0158a-115">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="0158a-115">This parameter is required.</span></span>

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

### <span data-ttu-id="0158a-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0158a-116">-Context</span></span>
<span data-ttu-id="0158a-117">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="0158a-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0158a-118">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="0158a-118">This parameter is required.</span></span>

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

### <span data-ttu-id="0158a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0158a-119">-DefaultProfile</span></span>
<span data-ttu-id="0158a-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0158a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0158a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0158a-121">-InputObject</span></span>
<span data-ttu-id="0158a-122">A Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease típus példánya.</span><span class="sxs-lookup"><span data-stu-id="0158a-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0158a-123">-Note</span><span class="sxs-lookup"><span data-stu-id="0158a-123">-Note</span></span>
<span data-ttu-id="0158a-124">Api kibocsátási megjegyzései.</span><span class="sxs-lookup"><span data-stu-id="0158a-124">Api Release Notes.</span></span>
<span data-ttu-id="0158a-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="0158a-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="0158a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0158a-126">-PassThru</span></span>
<span data-ttu-id="0158a-127">Ha ez a beállítás meg van adva, akkor a Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease típus, amely a beállított API Release típust képviseli.</span><span class="sxs-lookup"><span data-stu-id="0158a-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="0158a-128">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="0158a-128">-ReleaseId</span></span>
<span data-ttu-id="0158a-129">Az Api Revision ReleaseId azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0158a-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="0158a-130">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="0158a-130">This parameter is required.</span></span>

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

### <span data-ttu-id="0158a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0158a-131">-Confirm</span></span>
<span data-ttu-id="0158a-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0158a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0158a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0158a-133">-WhatIf</span></span>
<span data-ttu-id="0158a-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0158a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0158a-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0158a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0158a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0158a-136">CommonParameters</span></span>
<span data-ttu-id="0158a-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0158a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0158a-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0158a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0158a-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0158a-139">INPUTS</span></span>

### <span data-ttu-id="0158a-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0158a-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0158a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0158a-141">System.String</span></span>

### <span data-ttu-id="0158a-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="0158a-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="0158a-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0158a-143">OUTPUTS</span></span>

### <span data-ttu-id="0158a-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="0158a-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="0158a-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0158a-145">NOTES</span></span>

## <span data-ttu-id="0158a-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0158a-146">RELATED LINKS</span></span>

[<span data-ttu-id="0158a-147">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="0158a-147">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="0158a-148">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="0158a-148">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)
