---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 2013f1722ee246db023f4d26d456eafffa8f40eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670991"
---
# <span data-ttu-id="f98e9-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="f98e9-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="f98e9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f98e9-102">SYNOPSIS</span></span>
<span data-ttu-id="f98e9-103">Lépéseket hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f98e9-103">Creates a step.</span></span>

## <span data-ttu-id="f98e9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f98e9-104">SYNTAX</span></span>

```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f98e9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f98e9-105">DESCRIPTION</span></span>
<span data-ttu-id="f98e9-106">A **New-AzDeploymentManagerStep** parancsmag létrehoz egy központi kivezetési lépést, amelyre hivatkozhat a kivezetésben.</span><span class="sxs-lookup"><span data-stu-id="f98e9-106">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="f98e9-107">Adja meg a *nevet* , a *ResourceGroupName* és a szükséges tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="f98e9-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="f98e9-108">A visszaadott objektumot helyileg módosíthatja, majd az Set-AzDeploymentManagerStep parancsmag használatával alkalmazhatja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="f98e9-108">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="f98e9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f98e9-109">EXAMPLES</span></span>

### <span data-ttu-id="f98e9-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f98e9-110">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="f98e9-111">Egy lépést hoz létre a ContosoResourceGroup, amelynek a neve ContosoService1WaitStep a közép-amerikai névvel, az erőforrás helyére.</span><span class="sxs-lookup"><span data-stu-id="f98e9-111">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="f98e9-112">Az időtartam tulajdonság azt az időtartamot adja meg, ameddig a bevezetést a következő lépés futtatása előtt meg kell várni.</span><span class="sxs-lookup"><span data-stu-id="f98e9-112">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="f98e9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f98e9-113">PARAMETERS</span></span>

### <span data-ttu-id="f98e9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f98e9-114">-DefaultProfile</span></span>
<span data-ttu-id="f98e9-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f98e9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f98e9-116">-Időtartam</span><span class="sxs-lookup"><span data-stu-id="f98e9-116">-Duration</span></span>
<span data-ttu-id="f98e9-117">A várakozási idő az ISO 8601 formátumában.</span><span class="sxs-lookup"><span data-stu-id="f98e9-117">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="f98e9-118">Például: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="f98e9-118">E.g.: PT30M, PT1H</span></span>

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

### <span data-ttu-id="f98e9-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="f98e9-119">-Location</span></span>
<span data-ttu-id="f98e9-120">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="f98e9-120">The location of the resource.</span></span>

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

### <span data-ttu-id="f98e9-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f98e9-121">-Name</span></span>
<span data-ttu-id="f98e9-122">A lépéshez tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f98e9-122">The name of the step.</span></span>

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

### <span data-ttu-id="f98e9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f98e9-123">-ResourceGroupName</span></span>
<span data-ttu-id="f98e9-124">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="f98e9-124">The resource group.</span></span>

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

### <span data-ttu-id="f98e9-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="f98e9-125">-Tag</span></span>
<span data-ttu-id="f98e9-126">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="f98e9-126">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="f98e9-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f98e9-127">-Confirm</span></span>
<span data-ttu-id="f98e9-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f98e9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f98e9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f98e9-129">-WhatIf</span></span>
<span data-ttu-id="f98e9-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f98e9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f98e9-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f98e9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f98e9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f98e9-132">CommonParameters</span></span>
<span data-ttu-id="f98e9-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f98e9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f98e9-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f98e9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f98e9-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f98e9-135">INPUTS</span></span>

### <span data-ttu-id="f98e9-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f98e9-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f98e9-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f98e9-137">OUTPUTS</span></span>

### <span data-ttu-id="f98e9-138">Microsoft. Azure. Command. DeploymentManager. models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="f98e9-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="f98e9-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f98e9-139">NOTES</span></span>

## <span data-ttu-id="f98e9-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f98e9-140">RELATED LINKS</span></span>
