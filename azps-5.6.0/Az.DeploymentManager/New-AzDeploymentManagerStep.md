---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 08cde5aed74b194ede03f695eaf071d18467cb1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923681"
---
# <span data-ttu-id="339be-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="339be-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="339be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="339be-102">SYNOPSIS</span></span>
<span data-ttu-id="339be-103">Létrehoz egy lépést.</span><span class="sxs-lookup"><span data-stu-id="339be-103">Creates a step.</span></span>

## <span data-ttu-id="339be-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="339be-104">SYNTAX</span></span>

### <span data-ttu-id="339be-105">Várakozás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="339be-105">Wait (Default)</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="339be-106">HealthCheckFile</span><span class="sxs-lookup"><span data-stu-id="339be-106">HealthCheckFile</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckPropertiesFile <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="339be-107">HealthCheckObject</span><span class="sxs-lookup"><span data-stu-id="339be-107">HealthCheckObject</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckProperties <PSHealthCheckStepProperties> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="339be-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="339be-108">DESCRIPTION</span></span>
<span data-ttu-id="339be-109">A **New-AzDeploymentManagerStep** parancsmag létrehoz egy üzembe helyezési lépést, amely az üzembe helyezések során hivatkozhat rá.</span><span class="sxs-lookup"><span data-stu-id="339be-109">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="339be-110">Adja meg *a Name*, *ResourceGroupName és* a kötelező tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="339be-110">Specify the *Name*, *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="339be-111">A visszaadott objektumot helyben módosíthatja, majd a lépés módosításait alkalmazhatja a Set-AzDeploymentManagerStep parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="339be-111">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="339be-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="339be-112">EXAMPLES</span></span>

### <span data-ttu-id="339be-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="339be-113">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="339be-114">Létrehoz egy lépést a ContosoResourceGroup csoportban, ahol a ContosoService1WaitStep név szerepel az erőforrás helyeként.</span><span class="sxs-lookup"><span data-stu-id="339be-114">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="339be-115">Az Időtartam tulajdonság azt az időtartamot biztosítja, amíg a bevezetés a következő lépés futtatása előtt meg fog várni.</span><span class="sxs-lookup"><span data-stu-id="339be-115">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="339be-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="339be-116">PARAMETERS</span></span>

### <span data-ttu-id="339be-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="339be-117">-DefaultProfile</span></span>
<span data-ttu-id="339be-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="339be-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="339be-119">-Időtartam</span><span class="sxs-lookup"><span data-stu-id="339be-119">-Duration</span></span>
<span data-ttu-id="339be-120">A várakozás időtartama ISO 8601 formátumban.</span><span class="sxs-lookup"><span data-stu-id="339be-120">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="339be-121">Pl.: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="339be-121">E.g.: PT30M, PT1H</span></span>

```yaml
Type: System.String
Parameter Sets: Wait
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339be-122">-HealthCheckProperties</span><span class="sxs-lookup"><span data-stu-id="339be-122">-HealthCheckProperties</span></span>
<span data-ttu-id="339be-123">Az állapot-ellenőrzés tulajdonságai.</span><span class="sxs-lookup"><span data-stu-id="339be-123">The health check properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSHealthCheckStepProperties
Parameter Sets: HealthCheckObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339be-124">-HealthCheckPropertiesFile</span><span class="sxs-lookup"><span data-stu-id="339be-124">-HealthCheckPropertiesFile</span></span>
<span data-ttu-id="339be-125">Annak a fájlnak az elérési útja, amelyben az állapot-ellenőrzés tulajdonságai meg vannak adva.</span><span class="sxs-lookup"><span data-stu-id="339be-125">The path to the file where health check properties are defined.</span></span>

```yaml
Type: System.String
Parameter Sets: HealthCheckFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339be-126">-Location</span><span class="sxs-lookup"><span data-stu-id="339be-126">-Location</span></span>
<span data-ttu-id="339be-127">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="339be-127">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339be-128">-Name</span><span class="sxs-lookup"><span data-stu-id="339be-128">-Name</span></span>
<span data-ttu-id="339be-129">A lépés neve.</span><span class="sxs-lookup"><span data-stu-id="339be-129">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339be-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="339be-130">-ResourceGroupName</span></span>
<span data-ttu-id="339be-131">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="339be-131">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339be-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="339be-132">-Tag</span></span>
<span data-ttu-id="339be-133">A hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="339be-133">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339be-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="339be-134">-Confirm</span></span>
<span data-ttu-id="339be-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="339be-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="339be-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="339be-136">-WhatIf</span></span>
<span data-ttu-id="339be-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="339be-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="339be-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="339be-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="339be-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="339be-139">CommonParameters</span></span>
<span data-ttu-id="339be-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="339be-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="339be-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="339be-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="339be-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="339be-142">INPUTS</span></span>

### <span data-ttu-id="339be-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="339be-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="339be-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="339be-144">OUTPUTS</span></span>

### <span data-ttu-id="339be-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="339be-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="339be-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="339be-146">NOTES</span></span>

## <span data-ttu-id="339be-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="339be-147">RELATED LINKS</span></span>
