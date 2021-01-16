---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
ms.openlocfilehash: 647fd1f2f36d052d4d116f090fc438aa22dcc862
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466412"
---
# <span data-ttu-id="7a983-101">Remove-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="7a983-101">Remove-AzDeploymentScript</span></span>

## <span data-ttu-id="7a983-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a983-102">SYNOPSIS</span></span>
<span data-ttu-id="7a983-103">Eltávolít egy telepítési parancsfájlt és a hozzá tartozó erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="7a983-103">Removes a deployment script and its associated resources.</span></span>


## <span data-ttu-id="7a983-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7a983-104">SYNTAX</span></span>

### <span data-ttu-id="7a983-105">RemoveDeploymentScriptLogByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7a983-105">RemoveDeploymentScriptLogByName (Default)</span></span>
```
Remove-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a983-106">RemoveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="7a983-106">RemoveDeploymentScriptLogByResourceId</span></span>
```
Remove-AzDeploymentScript [-Id] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a983-107">RemoveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="7a983-107">RemoveDeploymentScriptLogByInputObject</span></span>
```
Remove-AzDeploymentScript [-InputObject] <PsDeploymentScript> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a983-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7a983-108">DESCRIPTION</span></span>
<span data-ttu-id="7a983-109">A **Remove-AzDeploymentScript** parancsmag eltávolítja a telepítési parancsfájlt és a hozzá tartozó erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="7a983-109">The **Remove-AzDeploymentScript** cmdlet removes a deployment script and its associated resources.</span></span>

## <span data-ttu-id="7a983-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7a983-110">EXAMPLES</span></span>

### <span data-ttu-id="7a983-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7a983-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="7a983-112">Törli a MyDeploymentScript nevű telepítési parancsfájlt a DS-TestRG erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="7a983-112">Deletes a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

## <span data-ttu-id="7a983-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a983-113">PARAMETERS</span></span>

### <span data-ttu-id="7a983-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a983-114">-Confirm</span></span>
<span data-ttu-id="7a983-115">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7a983-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a983-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a983-116">-DefaultProfile</span></span>
<span data-ttu-id="7a983-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a983-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a983-118">-Id</span><span class="sxs-lookup"><span data-stu-id="7a983-118">-Id</span></span>
<span data-ttu-id="7a983-119">A telepítési parancsfájl teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7a983-119">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="7a983-120">Példa: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="7a983-120">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a983-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a983-121">-InputObject</span></span>
<span data-ttu-id="7a983-122">A telepítési parancsfájl PowerShell-objektuma.</span><span class="sxs-lookup"><span data-stu-id="7a983-122">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: RemoveDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a983-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7a983-123">-Name</span></span>
<span data-ttu-id="7a983-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7a983-124">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a983-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a983-125">-PassThru</span></span>
<span data-ttu-id="7a983-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7a983-126">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a983-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a983-127">-ResourceGroupName</span></span>
<span data-ttu-id="7a983-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7a983-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a983-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a983-129">-WhatIf</span></span>
<span data-ttu-id="7a983-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7a983-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a983-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7a983-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a983-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a983-132">CommonParameters</span></span>
<span data-ttu-id="7a983-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a983-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7a983-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a983-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a983-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a983-135">INPUTS</span></span>

### <span data-ttu-id="7a983-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7a983-136">System.String</span></span>

### <span data-ttu-id="7a983-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="7a983-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="7a983-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a983-138">OUTPUTS</span></span>

### <span data-ttu-id="7a983-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="7a983-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="7a983-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7a983-140">NOTES</span></span>

## <span data-ttu-id="7a983-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a983-141">RELATED LINKS</span></span>