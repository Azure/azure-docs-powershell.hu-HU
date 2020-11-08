---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 077cdeef04e9a7b0eeec80e6d6ce4c17717826ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017802"
---
# <span data-ttu-id="21a9c-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="21a9c-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="21a9c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="21a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="21a9c-103">Lépéseket hoz létre.</span><span class="sxs-lookup"><span data-stu-id="21a9c-103">Creates a step.</span></span>

## <span data-ttu-id="21a9c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="21a9c-104">SYNTAX</span></span>

### <span data-ttu-id="21a9c-105">Várakozás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="21a9c-105">Wait (Default)</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21a9c-106">HealthCheckFile</span><span class="sxs-lookup"><span data-stu-id="21a9c-106">HealthCheckFile</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckPropertiesFile <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21a9c-107">HealthCheckObject</span><span class="sxs-lookup"><span data-stu-id="21a9c-107">HealthCheckObject</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckProperties <PSHealthCheckStepProperties> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21a9c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="21a9c-108">DESCRIPTION</span></span>
<span data-ttu-id="21a9c-109">A **New-AzDeploymentManagerStep** parancsmag létrehoz egy központi kivezetési lépést, amelyre hivatkozhat a kivezetésben.</span><span class="sxs-lookup"><span data-stu-id="21a9c-109">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="21a9c-110">Adja meg a *nevet* , a *ResourceGroupName* és a szükséges tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="21a9c-110">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="21a9c-111">A visszaadott objektumot helyileg módosíthatja, majd az Set-AzDeploymentManagerStep parancsmag használatával alkalmazhatja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="21a9c-111">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="21a9c-112">Példák</span><span class="sxs-lookup"><span data-stu-id="21a9c-112">EXAMPLES</span></span>

### <span data-ttu-id="21a9c-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="21a9c-113">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="21a9c-114">Egy lépést hoz létre a ContosoResourceGroup, amelynek a neve ContosoService1WaitStep a közép-amerikai névvel, az erőforrás helyére.</span><span class="sxs-lookup"><span data-stu-id="21a9c-114">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="21a9c-115">Az időtartam tulajdonság azt az időtartamot adja meg, ameddig a bevezetést a következő lépés futtatása előtt meg kell várni.</span><span class="sxs-lookup"><span data-stu-id="21a9c-115">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="21a9c-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="21a9c-116">PARAMETERS</span></span>

### <span data-ttu-id="21a9c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a9c-117">-DefaultProfile</span></span>
<span data-ttu-id="21a9c-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21a9c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21a9c-119">-Időtartam</span><span class="sxs-lookup"><span data-stu-id="21a9c-119">-Duration</span></span>
<span data-ttu-id="21a9c-120">A várakozási idő az ISO 8601 formátumában.</span><span class="sxs-lookup"><span data-stu-id="21a9c-120">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="21a9c-121">Például: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="21a9c-121">E.g.: PT30M, PT1H</span></span>

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

### <span data-ttu-id="21a9c-122">-HealthCheckProperties</span><span class="sxs-lookup"><span data-stu-id="21a9c-122">-HealthCheckProperties</span></span>
<span data-ttu-id="21a9c-123">Az állapot-ellenőrzés tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="21a9c-123">The health check properties.</span></span>

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

### <span data-ttu-id="21a9c-124">-HealthCheckPropertiesFile</span><span class="sxs-lookup"><span data-stu-id="21a9c-124">-HealthCheckPropertiesFile</span></span>
<span data-ttu-id="21a9c-125">Annak a fájlnak az elérési útvonala, ahol az állapot-ellenőrzés tulajdonságai meg vannak határozva.</span><span class="sxs-lookup"><span data-stu-id="21a9c-125">The path to the file where health check properties are defined.</span></span>

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

### <span data-ttu-id="21a9c-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="21a9c-126">-Location</span></span>
<span data-ttu-id="21a9c-127">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="21a9c-127">The location of the resource.</span></span>

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

### <span data-ttu-id="21a9c-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="21a9c-128">-Name</span></span>
<span data-ttu-id="21a9c-129">A lépéshez tartozó név.</span><span class="sxs-lookup"><span data-stu-id="21a9c-129">The name of the step.</span></span>

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

### <span data-ttu-id="21a9c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21a9c-130">-ResourceGroupName</span></span>
<span data-ttu-id="21a9c-131">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="21a9c-131">The resource group.</span></span>

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

### <span data-ttu-id="21a9c-132">-Címke</span><span class="sxs-lookup"><span data-stu-id="21a9c-132">-Tag</span></span>
<span data-ttu-id="21a9c-133">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="21a9c-133">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="21a9c-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="21a9c-134">-Confirm</span></span>
<span data-ttu-id="21a9c-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="21a9c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21a9c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21a9c-136">-WhatIf</span></span>
<span data-ttu-id="21a9c-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="21a9c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21a9c-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="21a9c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21a9c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a9c-139">CommonParameters</span></span>
<span data-ttu-id="21a9c-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="21a9c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21a9c-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="21a9c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a9c-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="21a9c-142">INPUTS</span></span>

### <span data-ttu-id="21a9c-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="21a9c-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="21a9c-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21a9c-144">OUTPUTS</span></span>

### <span data-ttu-id="21a9c-145">Microsoft. Azure. Command. DeploymentManager. models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="21a9c-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="21a9c-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="21a9c-146">NOTES</span></span>

## <span data-ttu-id="21a9c-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21a9c-147">RELATED LINKS</span></span>
