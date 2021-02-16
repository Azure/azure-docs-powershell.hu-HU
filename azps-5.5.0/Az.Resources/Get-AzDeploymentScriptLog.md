---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 608450112b7cd4f54ee0f08f0f29c3aa707fff9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146066"
---
# <span data-ttu-id="f310e-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="f310e-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="f310e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f310e-102">SYNOPSIS</span></span>
<span data-ttu-id="f310e-103">Az üzembe helyezési parancsfájl végrehajtásának naplóját kapja.</span><span class="sxs-lookup"><span data-stu-id="f310e-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="f310e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f310e-104">SYNTAX</span></span>

### <span data-ttu-id="f310e-105">GetDeploymentScriptLogByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f310e-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f310e-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="f310e-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f310e-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="f310e-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f310e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f310e-108">DESCRIPTION</span></span>
<span data-ttu-id="f310e-109">A **Get-AzDeploymentScriptLog parancsmag** megkapja a telepítési parancsfájl végrehajtásának naplóját.</span><span class="sxs-lookup"><span data-stu-id="f310e-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="f310e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f310e-110">EXAMPLES</span></span>

### <span data-ttu-id="f310e-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="f310e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="f310e-112">Egy MyDeploymentScript nevű telepítési parancsfájl naplóját kapja a DS-TestRG erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="f310e-112">Gets the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="f310e-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="f310e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -Tail 3
```

<span data-ttu-id="f310e-114">Egy telepítési parancsfájl naplójának utolsó 3 sorát kapja meg MyDeploymentScript néven a DS-TestRG erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="f310e-114">Gets the last 3 lines of the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="f310e-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="f310e-115">Example 3</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="f310e-116">Az első parancs egy MyDeploymentScript nevű telepítési parancsfájlt kap a DS-TestRG erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="f310e-116">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="f310e-117">A második parancs az adott telepítési parancsfájl naplóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f310e-117">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="f310e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f310e-118">PARAMETERS</span></span>

### <span data-ttu-id="f310e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f310e-119">-DefaultProfile</span></span>
<span data-ttu-id="f310e-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f310e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f310e-121">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="f310e-121">-DeploymentScriptObject</span></span>
<span data-ttu-id="f310e-122">A telepítési parancsfájl PowerShell-objektuma.</span><span class="sxs-lookup"><span data-stu-id="f310e-122">The deployment script PowerShell object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript
Parameter Sets: GetDeploymentScriptLogByInputObject
Aliases: DeploymentScriptInputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f310e-123">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="f310e-123">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="f310e-124">A telepítési parancsfájl teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f310e-124">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="f310e-125">Példa: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="f310e-125">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f310e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f310e-126">-Name</span></span>
<span data-ttu-id="f310e-127">A telepítési parancsfájl neve.</span><span class="sxs-lookup"><span data-stu-id="f310e-127">The name of the deployment script.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f310e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f310e-128">-ResourceGroupName</span></span>
<span data-ttu-id="f310e-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f310e-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f310e-130">-Tail</span><span class="sxs-lookup"><span data-stu-id="f310e-130">-Tail</span></span>
<span data-ttu-id="f310e-131">Kimenet korlátozása az utolsó n sorra</span><span class="sxs-lookup"><span data-stu-id="f310e-131">Limit output to last n lines</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f310e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f310e-132">CommonParameters</span></span>
<span data-ttu-id="f310e-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f310e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f310e-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f310e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f310e-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f310e-135">INPUTS</span></span>

### <span data-ttu-id="f310e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f310e-136">System.String</span></span>

### <span data-ttu-id="f310e-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="f310e-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="f310e-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f310e-138">OUTPUTS</span></span>

### <span data-ttu-id="f310e-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="f310e-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="f310e-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f310e-140">NOTES</span></span>

## <span data-ttu-id="f310e-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f310e-141">RELATED LINKS</span></span>
