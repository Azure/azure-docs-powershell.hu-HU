---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 608450112b7cd4f54ee0f08f0f29c3aa707fff9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185902"
---
# <span data-ttu-id="1cceb-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="1cceb-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="1cceb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1cceb-102">SYNOPSIS</span></span>
<span data-ttu-id="1cceb-103">Beolvassa a központi telepítő parancsfájl-végrehajtás naplózását.</span><span class="sxs-lookup"><span data-stu-id="1cceb-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="1cceb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1cceb-104">SYNTAX</span></span>

### <span data-ttu-id="1cceb-105">GetDeploymentScriptLogByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1cceb-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cceb-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="1cceb-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cceb-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="1cceb-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cceb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1cceb-108">DESCRIPTION</span></span>
<span data-ttu-id="1cceb-109">A **Get-AzDeploymentScriptLog** parancsmag a telepítő parancsfájl-végrehajtás naplózását kapja.</span><span class="sxs-lookup"><span data-stu-id="1cceb-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="1cceb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1cceb-110">EXAMPLES</span></span>

### <span data-ttu-id="1cceb-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1cceb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="1cceb-112">Beolvassa a MyDeploymentScript nevű központi telepítő parancsfájl naplóját, és az TestRG-ban az erőforráscsoport DS-.</span><span class="sxs-lookup"><span data-stu-id="1cceb-112">Gets the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="1cceb-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="1cceb-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -Tail 3
```

<span data-ttu-id="1cceb-114">Beilleszti egy központi telepítő parancsfájl naplójának utolsó 3 sorát, az MyDeploymentScript Name (erőforráscsoport DS-TestRG) néven.</span><span class="sxs-lookup"><span data-stu-id="1cceb-114">Gets the last 3 lines of the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="1cceb-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="1cceb-115">Example 3</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="1cceb-116">Az első parancs beolvassa a MyDeploymentScript nevű központi telepítő parancsfájlt az erőforráscsoport DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="1cceb-116">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="1cceb-117">A második parancs a központi telepítő parancsfájl naplójába kerül.</span><span class="sxs-lookup"><span data-stu-id="1cceb-117">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="1cceb-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1cceb-118">PARAMETERS</span></span>

### <span data-ttu-id="1cceb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cceb-119">-DefaultProfile</span></span>
<span data-ttu-id="1cceb-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1cceb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cceb-121">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="1cceb-121">-DeploymentScriptObject</span></span>
<span data-ttu-id="1cceb-122">A telepítő parancsfájl PowerShell-objektuma.</span><span class="sxs-lookup"><span data-stu-id="1cceb-122">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="1cceb-123">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="1cceb-123">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="1cceb-124">A telepítő parancsfájl teljes mértékben minősített erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1cceb-124">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="1cceb-125">Példa:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="1cceb-125">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="1cceb-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1cceb-126">-Name</span></span>
<span data-ttu-id="1cceb-127">A telepítő parancsfájl neve.</span><span class="sxs-lookup"><span data-stu-id="1cceb-127">The name of the deployment script.</span></span>

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

### <span data-ttu-id="1cceb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cceb-128">-ResourceGroupName</span></span>
<span data-ttu-id="1cceb-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1cceb-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="1cceb-130">-Farok</span><span class="sxs-lookup"><span data-stu-id="1cceb-130">-Tail</span></span>
<span data-ttu-id="1cceb-131">A kimenet korlátozása az utolsó n sorra</span><span class="sxs-lookup"><span data-stu-id="1cceb-131">Limit output to last n lines</span></span>

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

### <span data-ttu-id="1cceb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cceb-132">CommonParameters</span></span>
<span data-ttu-id="1cceb-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1cceb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cceb-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1cceb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cceb-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cceb-135">INPUTS</span></span>

### <span data-ttu-id="1cceb-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1cceb-136">System.String</span></span>

### <span data-ttu-id="1cceb-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="1cceb-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="1cceb-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cceb-138">OUTPUTS</span></span>

### <span data-ttu-id="1cceb-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="1cceb-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="1cceb-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1cceb-140">NOTES</span></span>

## <span data-ttu-id="1cceb-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1cceb-141">RELATED LINKS</span></span>