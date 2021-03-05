---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/save-azmanagementgroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
ms.openlocfilehash: c5d01afa5cd583ac0d356913dc3633cfddba6204
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016022"
---
# <span data-ttu-id="62837-101">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="62837-101">Save-AzManagementGroupDeploymentTemplate</span></span>

## <span data-ttu-id="62837-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62837-102">SYNOPSIS</span></span>
<span data-ttu-id="62837-103">Egy telepítősablont fájlba ment.</span><span class="sxs-lookup"><span data-stu-id="62837-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="62837-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="62837-104">SYNTAX</span></span>

### <span data-ttu-id="62837-105">SaveByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="62837-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzManagementGroupDeploymentTemplate -ManagementGroupId <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62837-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="62837-106">SaveByDeploymentObject</span></span>
```
Save-AzManagementGroupDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62837-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="62837-107">DESCRIPTION</span></span>
<span data-ttu-id="62837-108">A **Save-AzManagementGroupDeploymentTemplate**  parancsmag JSON-fájlba menti a telepítősablont egy felügyeleti csoport központi telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="62837-108">The **Save-AzManagementGroupDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at a management group.</span></span>

## <span data-ttu-id="62837-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="62837-109">EXAMPLES</span></span>

### <span data-ttu-id="62837-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="62837-110">Example 1</span></span>
```powershell
PS C:\> Save-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -DeploymentName "TestDeployment"
```

<span data-ttu-id="62837-111">Ez a parancs lekérte a telepítési sablont a TestDeploymentből, és JSON-fájlként menti azt az aktuális címtárba.</span><span class="sxs-lookup"><span data-stu-id="62837-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="62837-112">2. példa: Üzembe helyezés és sablon mentése</span><span class="sxs-lookup"><span data-stu-id="62837-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -Name "RolesDeployment" | Save-AzManagementGroupDeploymentTemplate
```

<span data-ttu-id="62837-113">Ez a parancs a "RolesDeployment" központi telepítést a "myMG" felügyeleti csoportban kapja meg, és menti a sablonját.</span><span class="sxs-lookup"><span data-stu-id="62837-113">This command gets the deployment "RolesDeployment" at the management group "myMG" and saves its template.</span></span>

## <span data-ttu-id="62837-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62837-114">PARAMETERS</span></span>

### <span data-ttu-id="62837-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62837-115">-DefaultProfile</span></span>
<span data-ttu-id="62837-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62837-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62837-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="62837-117">-DeploymentName</span></span>
<span data-ttu-id="62837-118">A telepítés neve.</span><span class="sxs-lookup"><span data-stu-id="62837-118">The deployment name.</span></span>

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

### <span data-ttu-id="62837-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="62837-119">-DeploymentObject</span></span>
<span data-ttu-id="62837-120">A telepítőobjektum.</span><span class="sxs-lookup"><span data-stu-id="62837-120">The deployment object.</span></span>

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

### <span data-ttu-id="62837-121">-Force</span><span class="sxs-lookup"><span data-stu-id="62837-121">-Force</span></span>
<span data-ttu-id="62837-122">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="62837-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="62837-123">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="62837-123">-ManagementGroupId</span></span>
<span data-ttu-id="62837-124">A felügyeleti csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="62837-124">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62837-125">-Path</span><span class="sxs-lookup"><span data-stu-id="62837-125">-Path</span></span>
<span data-ttu-id="62837-126">A sablonfájl kimeneti útvonala.</span><span class="sxs-lookup"><span data-stu-id="62837-126">The output path of the template file.</span></span>

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

### <span data-ttu-id="62837-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="62837-127">-Pre</span></span>
<span data-ttu-id="62837-128">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="62837-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="62837-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62837-129">-Confirm</span></span>
<span data-ttu-id="62837-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="62837-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62837-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62837-131">-WhatIf</span></span>
<span data-ttu-id="62837-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="62837-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62837-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="62837-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62837-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62837-134">CommonParameters</span></span>
<span data-ttu-id="62837-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62837-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62837-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62837-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62837-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62837-137">INPUTS</span></span>

### <span data-ttu-id="62837-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="62837-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="62837-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62837-139">OUTPUTS</span></span>

### <span data-ttu-id="62837-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="62837-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="62837-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="62837-141">NOTES</span></span>

## <span data-ttu-id="62837-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62837-142">RELATED LINKS</span></span>
