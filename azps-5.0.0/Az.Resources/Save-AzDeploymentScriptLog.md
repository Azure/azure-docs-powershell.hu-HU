---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 25f20b56ef7da59851d4726ad573c07d4da259e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195530"
---
# <span data-ttu-id="fe40c-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="fe40c-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="fe40c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe40c-102">SYNOPSIS</span></span>
<span data-ttu-id="fe40c-103">Menti a telepítő parancsfájl-végrehajtás naplóját a lemezre.</span><span class="sxs-lookup"><span data-stu-id="fe40c-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="fe40c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe40c-104">SYNTAX</span></span>

### <span data-ttu-id="fe40c-105">SaveDeploymentScriptLogByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fe40c-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe40c-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="fe40c-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [[-Tail] <Int32>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe40c-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="fe40c-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe40c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe40c-108">DESCRIPTION</span></span>
<span data-ttu-id="fe40c-109">A **Save-AzDeploymentScriptLog** a telepítő parancsfájl-végrehajtás naplóját menti a lemezre.</span><span class="sxs-lookup"><span data-stu-id="fe40c-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="fe40c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fe40c-110">EXAMPLES</span></span>

### <span data-ttu-id="fe40c-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fe40c-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="fe40c-112">Menti a központi telepítő parancsfájl naplóját a megadott névvel és erőforrás csoporttal.</span><span class="sxs-lookup"><span data-stu-id="fe40c-112">Saves the log of a deployment script with the given name and resource group.</span></span>

### <span data-ttu-id="fe40c-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="fe40c-113">Example 2</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace -Tail 3
```

<span data-ttu-id="fe40c-114">Menti a központi telepítő parancsfájl naplójának utolsó 3 sorát a megadott névvel és erőforrás csoporttal.</span><span class="sxs-lookup"><span data-stu-id="fe40c-114">Saves the last 3 lines of the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="fe40c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe40c-115">PARAMETERS</span></span>

### <span data-ttu-id="fe40c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe40c-116">-DefaultProfile</span></span>
<span data-ttu-id="fe40c-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe40c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe40c-118">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="fe40c-118">-DeploymentScriptObject</span></span>
<span data-ttu-id="fe40c-119">A telepítő parancsfájl PowerShell-objektuma.</span><span class="sxs-lookup"><span data-stu-id="fe40c-119">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="fe40c-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="fe40c-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="fe40c-121">A telepítő parancsfájl teljes mértékben minősített erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fe40c-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="fe40c-122">Példa:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="fe40c-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="fe40c-123">-Force</span><span class="sxs-lookup"><span data-stu-id="fe40c-123">-Force</span></span>
<span data-ttu-id="fe40c-124">A meglévő fájl felülírását kényszeríti.</span><span class="sxs-lookup"><span data-stu-id="fe40c-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="fe40c-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fe40c-125">-Name</span></span>
<span data-ttu-id="fe40c-126">A telepítő parancsfájl neve.</span><span class="sxs-lookup"><span data-stu-id="fe40c-126">The name of the deployment script.</span></span>

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

### <span data-ttu-id="fe40c-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="fe40c-127">-OutputPath</span></span>
<span data-ttu-id="fe40c-128">A központi telepítő parancsfájl mentési mappájának elérési útja.</span><span class="sxs-lookup"><span data-stu-id="fe40c-128">The directory path to save deployment script log.</span></span>

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

### <span data-ttu-id="fe40c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe40c-129">-ResourceGroupName</span></span>
<span data-ttu-id="fe40c-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fe40c-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="fe40c-131">-Farok</span><span class="sxs-lookup"><span data-stu-id="fe40c-131">-Tail</span></span>
<span data-ttu-id="fe40c-132">A kimenet korlátozása az utolsó n sorra</span><span class="sxs-lookup"><span data-stu-id="fe40c-132">Limit output to last n lines</span></span>

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

### <span data-ttu-id="fe40c-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fe40c-133">-Confirm</span></span>
<span data-ttu-id="fe40c-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fe40c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe40c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe40c-135">-WhatIf</span></span>
<span data-ttu-id="fe40c-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fe40c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe40c-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fe40c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe40c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe40c-138">CommonParameters</span></span>
<span data-ttu-id="fe40c-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe40c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe40c-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fe40c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe40c-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe40c-141">INPUTS</span></span>

### <span data-ttu-id="fe40c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="fe40c-142">System.String</span></span>

## <span data-ttu-id="fe40c-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe40c-143">OUTPUTS</span></span>

### <span data-ttu-id="fe40c-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="fe40c-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="fe40c-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe40c-145">NOTES</span></span>

## <span data-ttu-id="fe40c-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe40c-146">RELATED LINKS</span></span>
