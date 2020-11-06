---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: 7b04fc95af1ee340e87fa5ed46cbba9f1956d9e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490852"
---
# <span data-ttu-id="f544f-101">New-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="f544f-101">New-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="f544f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f544f-102">SYNOPSIS</span></span>
<span data-ttu-id="f544f-103">Új központi lépés létrehozása</span><span class="sxs-lookup"><span data-stu-id="f544f-103">Creates a new deployment step.</span></span>

## <span data-ttu-id="f544f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f544f-104">SYNTAX</span></span>

```
New-AzureRmDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -Duration <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f544f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f544f-105">DESCRIPTION</span></span>
<span data-ttu-id="f544f-106">A **New-AzureRmDeploymentManagerStep** parancsmag létrehoz egy központi kivezetési lépést, amelyre hivatkozhat a kivezetésben.</span><span class="sxs-lookup"><span data-stu-id="f544f-106">The **New-AzureRmDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="f544f-107">Adja meg a *nevet* , a *ResourceGroupName* és a szükséges tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="f544f-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="f544f-108">A visszaadott objektumot helyileg módosíthatja, majd az Set-AzureRmDeploymentManagerStep parancsmag használatával alkalmazhatja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="f544f-108">You can modify the returned object locally and then apply the changes to the step by using the Set-AzureRmDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="f544f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f544f-109">EXAMPLES</span></span>

### <span data-ttu-id="f544f-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f544f-110">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="f544f-111">Egy lépést hoz létre a ContosoResourceGroup, amelynek a neve ContosoService1WaitStep a közép-amerikai névvel, az erőforrás helyére.</span><span class="sxs-lookup"><span data-stu-id="f544f-111">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="f544f-112">Az időtartam tulajdonság azt az időtartamot adja meg, ameddig a bevezetést a következő lépés futtatása előtt meg kell várni.</span><span class="sxs-lookup"><span data-stu-id="f544f-112">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="f544f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f544f-113">PARAMETERS</span></span>

### <span data-ttu-id="f544f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f544f-114">-DefaultProfile</span></span>
<span data-ttu-id="f544f-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f544f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f544f-116">-Időtartam</span><span class="sxs-lookup"><span data-stu-id="f544f-116">-Duration</span></span>
<span data-ttu-id="f544f-117">A várakozási idő az ISO 8601 formátumában.</span><span class="sxs-lookup"><span data-stu-id="f544f-117">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="f544f-118">Például: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="f544f-118">E.g.: PT30M, PT1H</span></span>

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

### <span data-ttu-id="f544f-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="f544f-119">-Location</span></span>
<span data-ttu-id="f544f-120">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="f544f-120">The location of the resource.</span></span>

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

### <span data-ttu-id="f544f-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f544f-121">-Name</span></span>
<span data-ttu-id="f544f-122">A lépéshez tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f544f-122">The name of the step.</span></span>

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

### <span data-ttu-id="f544f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f544f-123">-ResourceGroupName</span></span>
<span data-ttu-id="f544f-124">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="f544f-124">The resource group.</span></span>

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

### <span data-ttu-id="f544f-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="f544f-125">-Tag</span></span>
<span data-ttu-id="f544f-126">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="f544f-126">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f544f-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f544f-127">-Confirm</span></span>
<span data-ttu-id="f544f-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f544f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f544f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f544f-129">-WhatIf</span></span>
<span data-ttu-id="f544f-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f544f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f544f-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f544f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f544f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f544f-132">CommonParameters</span></span>
<span data-ttu-id="f544f-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f544f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f544f-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f544f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f544f-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f544f-135">INPUTS</span></span>

### <span data-ttu-id="f544f-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f544f-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f544f-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f544f-137">OUTPUTS</span></span>

### <span data-ttu-id="f544f-138">Microsoft. Azure. Command. DeploymentManager. models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="f544f-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="f544f-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f544f-139">NOTES</span></span>

## <span data-ttu-id="f544f-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f544f-140">RELATED LINKS</span></span>
