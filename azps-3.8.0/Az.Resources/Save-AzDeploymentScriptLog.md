---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 4e32726b3e7af6608092d29fd52f7a41be042d42
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011787"
---
# <span data-ttu-id="b7165-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="b7165-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="b7165-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7165-102">SYNOPSIS</span></span>
<span data-ttu-id="b7165-103">Menti a telepítő parancsfájl-végrehajtás naplóját a lemezre.</span><span class="sxs-lookup"><span data-stu-id="b7165-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="b7165-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7165-104">SYNTAX</span></span>

### <span data-ttu-id="b7165-105">SaveDeploymentScriptLogByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b7165-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7165-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="b7165-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7165-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="b7165-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptInputObject] <PsDeploymentScript> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7165-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7165-108">DESCRIPTION</span></span>
<span data-ttu-id="b7165-109">A **Save-AzDeploymentScriptLog** a telepítő parancsfájl-végrehajtás naplóját menti a lemezre.</span><span class="sxs-lookup"><span data-stu-id="b7165-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="b7165-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b7165-110">EXAMPLES</span></span>

### <span data-ttu-id="b7165-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b7165-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="b7165-112">Menti a központi telepítő parancsfájl naplóját a megadott névvel és erőforrás csoporttal.</span><span class="sxs-lookup"><span data-stu-id="b7165-112">Saves the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="b7165-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7165-113">PARAMETERS</span></span>

### <span data-ttu-id="b7165-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b7165-114">-Confirm</span></span>
<span data-ttu-id="b7165-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b7165-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7165-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7165-116">-DefaultProfile</span></span>
<span data-ttu-id="b7165-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7165-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7165-118">-DeploymentScriptInputObject</span><span class="sxs-lookup"><span data-stu-id="b7165-118">-DeploymentScriptInputObject</span></span>
<span data-ttu-id="b7165-119">A telepítő parancsfájl PowerShell-objektuma.</span><span class="sxs-lookup"><span data-stu-id="b7165-119">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: SaveDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7165-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="b7165-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="b7165-121">A telepítő parancsfájl teljes mértékben minősített erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b7165-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="b7165-122">Példa:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="b7165-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7165-123">-Force</span><span class="sxs-lookup"><span data-stu-id="b7165-123">-Force</span></span>
<span data-ttu-id="b7165-124">A meglévő fájl felülírását kényszeríti.</span><span class="sxs-lookup"><span data-stu-id="b7165-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="b7165-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b7165-125">-Name</span></span>
<span data-ttu-id="b7165-126">A telepítő parancsfájl neve.</span><span class="sxs-lookup"><span data-stu-id="b7165-126">The name of the deployment script.</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7165-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="b7165-127">-OutputPath</span></span>
<span data-ttu-id="b7165-128">A központi telepítő parancsfájl mentési mappájának elérési útja.</span><span class="sxs-lookup"><span data-stu-id="b7165-128">The directory path to save deployment script log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7165-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7165-129">-ResourceGroupName</span></span>
<span data-ttu-id="b7165-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b7165-130">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7165-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7165-131">-WhatIf</span></span>
<span data-ttu-id="b7165-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b7165-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7165-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b7165-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7165-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7165-134">CommonParameters</span></span>
<span data-ttu-id="b7165-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b7165-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b7165-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7165-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7165-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7165-137">INPUTS</span></span>

### <span data-ttu-id="b7165-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b7165-138">System.String</span></span>

## <span data-ttu-id="b7165-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7165-139">OUTPUTS</span></span>

### <span data-ttu-id="b7165-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="b7165-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="b7165-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7165-141">NOTES</span></span>

## <span data-ttu-id="b7165-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7165-142">RELATED LINKS</span></span>
