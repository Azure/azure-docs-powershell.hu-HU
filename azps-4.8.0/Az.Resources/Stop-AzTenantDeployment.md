---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: 6c79d4b8d853d629a3b8e0422efb6a86eee18e34
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180923"
---
# <span data-ttu-id="b01c7-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="b01c7-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="b01c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b01c7-102">SYNOPSIS</span></span>
<span data-ttu-id="b01c7-103">Futó telepített példány lemondása a bérlői hatókörben</span><span class="sxs-lookup"><span data-stu-id="b01c7-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="b01c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b01c7-104">SYNTAX</span></span>

### <span data-ttu-id="b01c7-105">StopByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b01c7-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b01c7-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="b01c7-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b01c7-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="b01c7-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b01c7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b01c7-108">DESCRIPTION</span></span>
<span data-ttu-id="b01c7-109">A **stop-AzTenantDeployment** parancsmag lemondja azokat a telepített példányokat, amelyek a jelenlegi bérlői hatókörben nem fejeződött be.</span><span class="sxs-lookup"><span data-stu-id="b01c7-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="b01c7-110">Ha meg szeretné szüntetni egy központi üzembe állítást, akkor a bevezetésnek hiányos kitöltési állapottal kell rendelkeznie (például kiépítési vagy sikertelen).</span><span class="sxs-lookup"><span data-stu-id="b01c7-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="b01c7-111">Ha a bérlői hatókörben szeretne bevezetést létrehozni, használja az New-AzTenantDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b01c7-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="b01c7-112">Példák</span><span class="sxs-lookup"><span data-stu-id="b01c7-112">EXAMPLES</span></span>

### <span data-ttu-id="b01c7-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b01c7-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="b01c7-114">A parancs a jelenlegi bérlői hatókörben lemondja a "deployment01" futó központi telepítőt.</span><span class="sxs-lookup"><span data-stu-id="b01c7-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="b01c7-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="b01c7-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="b01c7-116">Ez a parancs beilleszti a "deployment01" üzembe állítást az aktuális bérlői tartományba, és lemondja azt.</span><span class="sxs-lookup"><span data-stu-id="b01c7-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="b01c7-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b01c7-117">PARAMETERS</span></span>

### <span data-ttu-id="b01c7-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b01c7-118">-ApiVersion</span></span>
<span data-ttu-id="b01c7-119">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b01c7-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b01c7-120">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b01c7-120">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b01c7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b01c7-121">-DefaultProfile</span></span>
<span data-ttu-id="b01c7-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b01c7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b01c7-123">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="b01c7-123">-Id</span></span>
<span data-ttu-id="b01c7-124">A központi telepítő teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b01c7-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="b01c7-125">Példa:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="b01c7-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b01c7-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b01c7-126">-InputObject</span></span>
<span data-ttu-id="b01c7-127">A központi telepítő objektum.</span><span class="sxs-lookup"><span data-stu-id="b01c7-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b01c7-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b01c7-128">-Name</span></span>
<span data-ttu-id="b01c7-129">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="b01c7-129">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b01c7-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b01c7-130">-PassThru</span></span>
<span data-ttu-id="b01c7-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b01c7-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="b01c7-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="b01c7-132">-Pre</span></span>
<span data-ttu-id="b01c7-133">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="b01c7-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b01c7-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b01c7-134">-Confirm</span></span>
<span data-ttu-id="b01c7-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b01c7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b01c7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b01c7-136">-WhatIf</span></span>
<span data-ttu-id="b01c7-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b01c7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b01c7-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b01c7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b01c7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b01c7-139">CommonParameters</span></span>
<span data-ttu-id="b01c7-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b01c7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b01c7-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b01c7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b01c7-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b01c7-142">INPUTS</span></span>

### <span data-ttu-id="b01c7-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="b01c7-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="b01c7-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b01c7-144">OUTPUTS</span></span>

### <span data-ttu-id="b01c7-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b01c7-145">System.Boolean</span></span>

## <span data-ttu-id="b01c7-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b01c7-146">NOTES</span></span>

## <span data-ttu-id="b01c7-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b01c7-147">RELATED LINKS</span></span>
