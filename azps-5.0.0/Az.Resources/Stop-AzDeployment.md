---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: fd3fc9b254fab2044ad955d7b4aeb43783d5a907
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187034"
---
# <span data-ttu-id="66d23-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="66d23-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="66d23-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66d23-102">SYNOPSIS</span></span>
<span data-ttu-id="66d23-103">Futó példány visszavonása</span><span class="sxs-lookup"><span data-stu-id="66d23-103">Cancel a running deployment</span></span>

## <span data-ttu-id="66d23-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66d23-104">SYNTAX</span></span>

### <span data-ttu-id="66d23-105">StopByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="66d23-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66d23-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="66d23-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66d23-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="66d23-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66d23-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="66d23-108">DESCRIPTION</span></span>
<span data-ttu-id="66d23-109">A **stop-AzDeployment** parancsmag lemondja az előfizetéses hatókört, amely a kezdést, de nem fejeződött be.</span><span class="sxs-lookup"><span data-stu-id="66d23-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="66d23-110">Ha meg szeretné szüntetni egy központi üzembe állítást, akkor a bevezetésnek hiányos kitöltési állapottal kell rendelkeznie (például kiépítési vagy sikertelen).</span><span class="sxs-lookup"><span data-stu-id="66d23-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="66d23-111">Az előfizetéses hatókörben az New-AzDeployment parancsmagot használva hozhat létre központi telepítőt.</span><span class="sxs-lookup"><span data-stu-id="66d23-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="66d23-112">Ez a parancsmag csak egy futó központi telepítőt állít le.</span><span class="sxs-lookup"><span data-stu-id="66d23-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="66d23-113">Egy adott példány leállításához használja a *Name (név* ) paramétert.</span><span class="sxs-lookup"><span data-stu-id="66d23-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="66d23-114">Példák</span><span class="sxs-lookup"><span data-stu-id="66d23-114">EXAMPLES</span></span>

### <span data-ttu-id="66d23-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="66d23-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="66d23-116">Ez a parancs lemondja az aktuális előfizetési tartomány "deployment01" futó példányát.</span><span class="sxs-lookup"><span data-stu-id="66d23-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="66d23-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="66d23-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="66d23-118">Ez a parancs beilleszti a "deployment01" üzembe állítást az aktuális előfizetési tartományba, és lemondja azt.</span><span class="sxs-lookup"><span data-stu-id="66d23-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="66d23-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66d23-119">PARAMETERS</span></span>

### <span data-ttu-id="66d23-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66d23-120">-DefaultProfile</span></span>
<span data-ttu-id="66d23-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66d23-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66d23-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="66d23-122">-Id</span></span>
<span data-ttu-id="66d23-123">A központi telepítő teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="66d23-123">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="66d23-124">Példa:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="66d23-124">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66d23-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66d23-125">-InputObject</span></span>
<span data-ttu-id="66d23-126">A központi telepítő objektum.</span><span class="sxs-lookup"><span data-stu-id="66d23-126">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66d23-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="66d23-127">-Name</span></span>
<span data-ttu-id="66d23-128">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="66d23-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66d23-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66d23-129">-PassThru</span></span>
<span data-ttu-id="66d23-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="66d23-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="66d23-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="66d23-131">-Pre</span></span>
<span data-ttu-id="66d23-132">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="66d23-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="66d23-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="66d23-133">-Confirm</span></span>
<span data-ttu-id="66d23-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="66d23-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66d23-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66d23-135">-WhatIf</span></span>
<span data-ttu-id="66d23-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="66d23-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66d23-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="66d23-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66d23-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66d23-138">CommonParameters</span></span>
<span data-ttu-id="66d23-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="66d23-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66d23-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="66d23-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66d23-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66d23-141">INPUTS</span></span>

### <span data-ttu-id="66d23-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="66d23-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="66d23-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66d23-143">OUTPUTS</span></span>

### <span data-ttu-id="66d23-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66d23-144">System.Boolean</span></span>

## <span data-ttu-id="66d23-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66d23-145">NOTES</span></span>

## <span data-ttu-id="66d23-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66d23-146">RELATED LINKS</span></span>
