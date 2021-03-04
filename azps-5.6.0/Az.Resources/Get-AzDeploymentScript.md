---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
ms.openlocfilehash: 7b61444bb4f3a23e1611e90b79545e1c174b0437
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920937"
---
# <span data-ttu-id="10de8-101">Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="10de8-101">Get-AzDeploymentScript</span></span>

## <span data-ttu-id="10de8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10de8-102">SYNOPSIS</span></span>
<span data-ttu-id="10de8-103">Telepítési parancsfájlokat kap vagy sorol fel.</span><span class="sxs-lookup"><span data-stu-id="10de8-103">Gets or lists deployment scripts.</span></span>

## <span data-ttu-id="10de8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="10de8-104">SYNTAX</span></span>

### <span data-ttu-id="10de8-105">ListDeploymentScript (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="10de8-105">ListDeploymentScript (Default)</span></span>
```
Get-AzDeploymentScript [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10de8-106">GetDeploymentScriptByName</span><span class="sxs-lookup"><span data-stu-id="10de8-106">GetDeploymentScriptByName</span></span>
```
Get-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10de8-107">GetDeploymentScriptByResourceId</span><span class="sxs-lookup"><span data-stu-id="10de8-107">GetDeploymentScriptByResourceId</span></span>
```
Get-AzDeploymentScript [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10de8-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="10de8-108">DESCRIPTION</span></span>
<span data-ttu-id="10de8-109">A **Get-AzDeploymentScript** parancsmag egyetlen telepítési parancsfájlt vagy a telepítési parancsfájlok listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="10de8-109">The **Get-AzDeploymentScript** cmdlet gets a single deployment script or a list of deployment scripts.</span></span>

## <span data-ttu-id="10de8-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="10de8-110">EXAMPLES</span></span>

### <span data-ttu-id="10de8-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="10de8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScript
```

<span data-ttu-id="10de8-112">Az aktuális felhasználó környezetében felsorolja az előfizetésben lévő telepítési parancsfájlokat.</span><span class="sxs-lookup"><span data-stu-id="10de8-112">Lists deployment scripts in the subscription in current user's context.</span></span>

### <span data-ttu-id="10de8-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="10de8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="10de8-114">A DS-TestRg erőforráscsoport telepítési parancsprogramjait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="10de8-114">Lists deployment scripts in resource group DS-TestRg.</span></span>

### <span data-ttu-id="10de8-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="10de8-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="10de8-116">A DS-TestRG erőforráscsoportban a MyDeploymentScript nevű telepítési parancsfájlt kap.</span><span class="sxs-lookup"><span data-stu-id="10de8-116">Gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="10de8-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="10de8-117">Example 4</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Id "/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}"
```

<span data-ttu-id="10de8-118">Telepítési parancsfájlt kap a megadott erőforrás-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="10de8-118">Gets a deployment script with the given resource Id.</span></span> 

## <span data-ttu-id="10de8-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10de8-119">PARAMETERS</span></span>

### <span data-ttu-id="10de8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10de8-120">-DefaultProfile</span></span>
<span data-ttu-id="10de8-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="10de8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10de8-122">-Id</span><span class="sxs-lookup"><span data-stu-id="10de8-122">-Id</span></span>
<span data-ttu-id="10de8-123">A telepítési parancsfájl teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="10de8-123">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="10de8-124">Példa: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="10de8-124">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10de8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="10de8-125">-Name</span></span>
<span data-ttu-id="10de8-126">A telepítési parancsfájl neve</span><span class="sxs-lookup"><span data-stu-id="10de8-126">The name of the deployment script</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10de8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10de8-127">-ResourceGroupName</span></span>
<span data-ttu-id="10de8-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="10de8-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListDeploymentScript
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10de8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10de8-129">CommonParameters</span></span>
<span data-ttu-id="10de8-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10de8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="10de8-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10de8-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10de8-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10de8-132">INPUTS</span></span>

### <span data-ttu-id="10de8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="10de8-133">System.String</span></span>

## <span data-ttu-id="10de8-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10de8-134">OUTPUTS</span></span>

### <span data-ttu-id="10de8-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="10de8-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="10de8-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="10de8-136">NOTES</span></span>

## <span data-ttu-id="10de8-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10de8-137">RELATED LINKS</span></span>