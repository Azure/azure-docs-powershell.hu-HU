---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
ms.openlocfilehash: a15804d0af664c46d443128e940e3b9f2c8a1acc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010800"
---
# <span data-ttu-id="6c982-101">Remove-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="6c982-101">Remove-AzDeploymentScript</span></span>

## <span data-ttu-id="6c982-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6c982-102">SYNOPSIS</span></span>
<span data-ttu-id="6c982-103">Eltávolítja a telepítő parancsfájlt és a hozzá tartozó erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="6c982-103">Removes a deployment script and its associated resources.</span></span>


## <span data-ttu-id="6c982-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6c982-104">SYNTAX</span></span>

### <span data-ttu-id="6c982-105">RemoveDeploymentScriptLogByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6c982-105">RemoveDeploymentScriptLogByName (Default)</span></span>
```
Remove-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c982-106">RemoveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="6c982-106">RemoveDeploymentScriptLogByResourceId</span></span>
```
Remove-AzDeploymentScript [-Id] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c982-107">RemoveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="6c982-107">RemoveDeploymentScriptLogByInputObject</span></span>
```
Remove-AzDeploymentScript [-InputObject] <PsDeploymentScript> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c982-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6c982-108">DESCRIPTION</span></span>
<span data-ttu-id="6c982-109">A **Remove-AzDeploymentScript** parancsmag eltávolítja a telepítő parancsfájlt és a hozzá tartozó erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="6c982-109">The **Remove-AzDeploymentScript** cmdlet removes a deployment script and its associated resources.</span></span>

## <span data-ttu-id="6c982-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6c982-110">EXAMPLES</span></span>

### <span data-ttu-id="6c982-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6c982-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="6c982-112">Törli a MyDeploymentScript nevű telepítő parancsfájlt az erőforráscsoport DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="6c982-112">Deletes a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

## <span data-ttu-id="6c982-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6c982-113">PARAMETERS</span></span>

### <span data-ttu-id="6c982-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6c982-114">-Confirm</span></span>
<span data-ttu-id="6c982-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6c982-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c982-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c982-116">-DefaultProfile</span></span>
<span data-ttu-id="6c982-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6c982-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c982-118">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="6c982-118">-Id</span></span>
<span data-ttu-id="6c982-119">A telepítő parancsfájl teljes mértékben minősített erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6c982-119">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="6c982-120">Példa:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="6c982-120">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="6c982-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c982-121">-InputObject</span></span>
<span data-ttu-id="6c982-122">A telepítő parancsfájl PowerShell-objektuma.</span><span class="sxs-lookup"><span data-stu-id="6c982-122">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="6c982-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6c982-123">-Name</span></span>
<span data-ttu-id="6c982-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6c982-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="6c982-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c982-125">-PassThru</span></span>
<span data-ttu-id="6c982-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6c982-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6c982-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c982-127">-ResourceGroupName</span></span>
<span data-ttu-id="6c982-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6c982-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="6c982-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c982-129">-WhatIf</span></span>
<span data-ttu-id="6c982-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6c982-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c982-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6c982-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c982-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c982-132">CommonParameters</span></span>
<span data-ttu-id="6c982-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6c982-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6c982-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c982-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c982-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c982-135">INPUTS</span></span>

### <span data-ttu-id="6c982-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6c982-136">System.String</span></span>

### <span data-ttu-id="6c982-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="6c982-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="6c982-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c982-138">OUTPUTS</span></span>

### <span data-ttu-id="6c982-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="6c982-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="6c982-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6c982-140">NOTES</span></span>

## <span data-ttu-id="6c982-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c982-141">RELATED LINKS</span></span>
