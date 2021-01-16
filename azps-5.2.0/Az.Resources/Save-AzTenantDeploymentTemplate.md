---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-aztenantdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
ms.openlocfilehash: dcee9317e6aad113088dc3498a337e16e61b6320
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351762"
---
# <span data-ttu-id="8c0b0-101">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="8c0b0-101">Save-AzTenantDeploymentTemplate</span></span>

## <span data-ttu-id="8c0b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c0b0-102">SYNOPSIS</span></span>
<span data-ttu-id="8c0b0-103">Egy telepítősablont fájlba ment.</span><span class="sxs-lookup"><span data-stu-id="8c0b0-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="8c0b0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8c0b0-104">SYNTAX</span></span>

### <span data-ttu-id="8c0b0-105">SaveByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c0b0-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0b0-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="8c0b0-106">SaveByDeploymentObject</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c0b0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8c0b0-107">DESCRIPTION</span></span>
<span data-ttu-id="8c0b0-108">A **Save-AzTenantDeploymentTemplate**  parancsmag JSON-fájlba menti a telepítősablont a bérlői webhely hatókörén üzemelő telepítéshez.</span><span class="sxs-lookup"><span data-stu-id="8c0b0-108">The **Save-AzTenantDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at tenant scope.</span></span>

## <span data-ttu-id="8c0b0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8c0b0-109">EXAMPLES</span></span>

### <span data-ttu-id="8c0b0-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="8c0b0-110">Example 1</span></span>
```powershell
PS C:\> Save-AzTenantDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="8c0b0-111">Ez a parancs lekérte a telepítési sablont a TestDeploymentből, és JSON-fájlként menti azt az aktuális címtárba.</span><span class="sxs-lookup"><span data-stu-id="8c0b0-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="8c0b0-112">2. példa: Üzembe helyezés és sablon mentése</span><span class="sxs-lookup"><span data-stu-id="8c0b0-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzTenantDeploymentTemplate -Name "RolesDeployment" | Save-AzTenantDeploymentTemplate
```

<span data-ttu-id="8c0b0-113">Ez a parancs a központi telepítés "RolesDeployment" parancsát a bérlő aktuális hatókörében kapja meg, és menti a sablonját.</span><span class="sxs-lookup"><span data-stu-id="8c0b0-113">This command gets the deployment "RolesDeployment" at the current tenant scope and saves its template.</span></span>

## <span data-ttu-id="8c0b0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c0b0-114">PARAMETERS</span></span>

### <span data-ttu-id="8c0b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c0b0-115">-DefaultProfile</span></span>
<span data-ttu-id="8c0b0-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c0b0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c0b0-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="8c0b0-117">-DeploymentName</span></span>
<span data-ttu-id="8c0b0-118">A telepítés neve.</span><span class="sxs-lookup"><span data-stu-id="8c0b0-118">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0b0-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="8c0b0-119">-DeploymentObject</span></span>
<span data-ttu-id="8c0b0-120">A telepítőobjektum.</span><span class="sxs-lookup"><span data-stu-id="8c0b0-120">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: SaveByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c0b0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8c0b0-121">-Force</span></span>
<span data-ttu-id="8c0b0-122">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8c0b0-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8c0b0-123">-Path</span><span class="sxs-lookup"><span data-stu-id="8c0b0-123">-Path</span></span>
<span data-ttu-id="8c0b0-124">A sablonfájl kimeneti útvonala.</span><span class="sxs-lookup"><span data-stu-id="8c0b0-124">The output path of the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0b0-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="8c0b0-125">-Pre</span></span>
<span data-ttu-id="8c0b0-126">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="8c0b0-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8c0b0-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c0b0-127">-Confirm</span></span>
<span data-ttu-id="8c0b0-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8c0b0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c0b0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c0b0-129">-WhatIf</span></span>
<span data-ttu-id="8c0b0-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8c0b0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c0b0-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c0b0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c0b0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c0b0-132">CommonParameters</span></span>
<span data-ttu-id="8c0b0-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c0b0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c0b0-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c0b0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c0b0-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c0b0-135">INPUTS</span></span>

### <span data-ttu-id="8c0b0-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="8c0b0-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="8c0b0-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c0b0-137">OUTPUTS</span></span>

### <span data-ttu-id="8c0b0-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="8c0b0-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="8c0b0-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8c0b0-139">NOTES</span></span>

## <span data-ttu-id="8c0b0-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c0b0-140">RELATED LINKS</span></span>
