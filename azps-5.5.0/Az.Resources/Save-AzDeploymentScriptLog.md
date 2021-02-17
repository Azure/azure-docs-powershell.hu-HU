---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 25f20b56ef7da59851d4726ad573c07d4da259e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156442"
---
# <span data-ttu-id="fa2b3-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="fa2b3-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="fa2b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa2b3-102">SYNOPSIS</span></span>
<span data-ttu-id="fa2b3-103">Az üzembe helyezési parancsfájl végrehajtásának naplóját lemezre menti.</span><span class="sxs-lookup"><span data-stu-id="fa2b3-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="fa2b3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fa2b3-104">SYNTAX</span></span>

### <span data-ttu-id="fa2b3-105">SaveDeploymentScriptLogByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fa2b3-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa2b3-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="fa2b3-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [[-Tail] <Int32>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa2b3-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="fa2b3-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa2b3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fa2b3-108">DESCRIPTION</span></span>
<span data-ttu-id="fa2b3-109">A **Save-AzDeploymentScriptLog** a telepítőprogram végrehajtásának naplóját lemezre menti.</span><span class="sxs-lookup"><span data-stu-id="fa2b3-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="fa2b3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fa2b3-110">EXAMPLES</span></span>

### <span data-ttu-id="fa2b3-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="fa2b3-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="fa2b3-112">Menti egy telepítési parancsfájl naplóját a megadott néven és erőforráscsoporttal.</span><span class="sxs-lookup"><span data-stu-id="fa2b3-112">Saves the log of a deployment script with the given name and resource group.</span></span>

### <span data-ttu-id="fa2b3-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="fa2b3-113">Example 2</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace -Tail 3
```

<span data-ttu-id="fa2b3-114">Menti a telepítési parancsfájl naplójának utolsó 3 sorát a megadott névvel és erőforráscsoporttal.</span><span class="sxs-lookup"><span data-stu-id="fa2b3-114">Saves the last 3 lines of the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="fa2b3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa2b3-115">PARAMETERS</span></span>

### <span data-ttu-id="fa2b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa2b3-116">-DefaultProfile</span></span>
<span data-ttu-id="fa2b3-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fa2b3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa2b3-118">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="fa2b3-118">-DeploymentScriptObject</span></span>
<span data-ttu-id="fa2b3-119">A telepítési parancsfájl PowerShell-objektuma.</span><span class="sxs-lookup"><span data-stu-id="fa2b3-119">The deployment script PowerShell object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript
Parameter Sets: SaveDeploymentScriptLogByInputObject
Aliases: DeploymentScriptInputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa2b3-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="fa2b3-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="fa2b3-121">A telepítési parancsfájl teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fa2b3-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="fa2b3-122">Példa: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="fa2b3-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa2b3-123">-Force</span><span class="sxs-lookup"><span data-stu-id="fa2b3-123">-Force</span></span>
<span data-ttu-id="fa2b3-124">A meglévő fájl felülírása.</span><span class="sxs-lookup"><span data-stu-id="fa2b3-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="fa2b3-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fa2b3-125">-Name</span></span>
<span data-ttu-id="fa2b3-126">A telepítési parancsfájl neve.</span><span class="sxs-lookup"><span data-stu-id="fa2b3-126">The name of the deployment script.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa2b3-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="fa2b3-127">-OutputPath</span></span>
<span data-ttu-id="fa2b3-128">A telepítési parancsfájlnapló mentésének könyvtár elérési útja.</span><span class="sxs-lookup"><span data-stu-id="fa2b3-128">The directory path to save deployment script log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2b3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa2b3-129">-ResourceGroupName</span></span>
<span data-ttu-id="fa2b3-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fa2b3-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa2b3-131">-Tail</span><span class="sxs-lookup"><span data-stu-id="fa2b3-131">-Tail</span></span>
<span data-ttu-id="fa2b3-132">Kimenet korlátozása az utolsó n sorra</span><span class="sxs-lookup"><span data-stu-id="fa2b3-132">Limit output to last n lines</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2b3-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa2b3-133">-Confirm</span></span>
<span data-ttu-id="fa2b3-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fa2b3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa2b3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa2b3-135">-WhatIf</span></span>
<span data-ttu-id="fa2b3-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fa2b3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa2b3-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fa2b3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa2b3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa2b3-138">CommonParameters</span></span>
<span data-ttu-id="fa2b3-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa2b3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa2b3-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa2b3-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa2b3-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa2b3-141">INPUTS</span></span>

### <span data-ttu-id="fa2b3-142">System.String</span><span class="sxs-lookup"><span data-stu-id="fa2b3-142">System.String</span></span>

## <span data-ttu-id="fa2b3-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa2b3-143">OUTPUTS</span></span>

### <span data-ttu-id="fa2b3-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="fa2b3-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="fa2b3-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fa2b3-145">NOTES</span></span>

## <span data-ttu-id="fa2b3-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa2b3-146">RELATED LINKS</span></span>
