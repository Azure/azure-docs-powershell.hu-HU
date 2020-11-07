---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/stop-azurermdeployment
schema: 2.0.0
ms.openlocfilehash: 49ea711740eff624a9560b6d70239edb476dc989
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849025"
---
# <span data-ttu-id="5be8f-101">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="5be8f-101">Stop-AzureRmDeployment</span></span>

## <span data-ttu-id="5be8f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5be8f-102">SYNOPSIS</span></span>
<span data-ttu-id="5be8f-103">Cancal futó példány létrehozása</span><span class="sxs-lookup"><span data-stu-id="5be8f-103">Cancal a running deployment</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5be8f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5be8f-104">SYNTAX</span></span>

### <span data-ttu-id="5be8f-105">StopByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5be8f-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzureRmDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5be8f-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="5be8f-106">StopByDeploymentId</span></span>
```
Stop-AzureRmDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5be8f-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="5be8f-107">StopByInputObject</span></span>
```
Stop-AzureRmDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5be8f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5be8f-108">DESCRIPTION</span></span>
<span data-ttu-id="5be8f-109">A **stop-AzureRmDeployment** parancsmag lemondja az előfizetéses hatókört, amely a kezdést, de nem fejeződött be.</span><span class="sxs-lookup"><span data-stu-id="5be8f-109">The **Stop-AzureRmDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="5be8f-110">Ha meg szeretné szüntetni egy központi üzembe állítást, akkor a bevezetésnek hiányos kitöltési állapottal kell rendelkeznie (például kiépítési vagy sikertelen).</span><span class="sxs-lookup"><span data-stu-id="5be8f-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="5be8f-111">Az előfizetéses hatókörben az New-AzureRmDeployment parancsmagot használva hozhat létre központi telepítőt.</span><span class="sxs-lookup"><span data-stu-id="5be8f-111">To create a deployment at subscription scope, use the New-AzureRmDeployment cmdlet.</span></span>

<span data-ttu-id="5be8f-112">Ez a parancsmag csak egy futó központi telepítőt állít le.</span><span class="sxs-lookup"><span data-stu-id="5be8f-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="5be8f-113">Egy adott példány leállításához használja a *Name (név* ) paramétert.</span><span class="sxs-lookup"><span data-stu-id="5be8f-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="5be8f-114">Példák</span><span class="sxs-lookup"><span data-stu-id="5be8f-114">EXAMPLES</span></span>

### <span data-ttu-id="5be8f-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5be8f-115">Example 1</span></span>
```
PS C:\>Stop-AzureRmDeployment -Name "deployment01"
```

<span data-ttu-id="5be8f-116">Ez a parancs lemondja az aktuális előfizetési tartomány "deployment01" futó példányát.</span><span class="sxs-lookup"><span data-stu-id="5be8f-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="5be8f-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="5be8f-117">Example 2</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "deployment01" | Stop-AzureRmDeployment
```

<span data-ttu-id="5be8f-118">Ez a parancs beilleszti a "deployment01" üzembe állítást az aktuális előfizetési tartományba, és lemondja azt.</span><span class="sxs-lookup"><span data-stu-id="5be8f-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="5be8f-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5be8f-119">PARAMETERS</span></span>

### <span data-ttu-id="5be8f-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5be8f-120">-ApiVersion</span></span>
<span data-ttu-id="5be8f-121">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5be8f-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="5be8f-122">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="5be8f-122">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="5be8f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5be8f-123">-DefaultProfile</span></span>
<span data-ttu-id="5be8f-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5be8f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5be8f-125">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="5be8f-125">-Id</span></span>
<span data-ttu-id="5be8f-126">A központi telepítő teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5be8f-126">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="5be8f-127">Példa:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="5be8f-127">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="5be8f-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5be8f-128">-InputObject</span></span>
<span data-ttu-id="5be8f-129">A központi telepítő objektum.</span><span class="sxs-lookup"><span data-stu-id="5be8f-129">The deployment object.</span></span>

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

### <span data-ttu-id="5be8f-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5be8f-130">-Name</span></span>
<span data-ttu-id="5be8f-131">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="5be8f-131">The name of the deployment.</span></span>

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

### <span data-ttu-id="5be8f-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5be8f-132">-PassThru</span></span>
<span data-ttu-id="5be8f-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5be8f-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5be8f-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="5be8f-134">-Pre</span></span>
<span data-ttu-id="5be8f-135">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="5be8f-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5be8f-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5be8f-136">-Confirm</span></span>
<span data-ttu-id="5be8f-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5be8f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5be8f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5be8f-138">-WhatIf</span></span>
<span data-ttu-id="5be8f-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5be8f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5be8f-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5be8f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5be8f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5be8f-141">CommonParameters</span></span>
<span data-ttu-id="5be8f-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5be8f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5be8f-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5be8f-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5be8f-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5be8f-144">INPUTS</span></span>

### <span data-ttu-id="5be8f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="5be8f-145">System.String</span></span>

## <span data-ttu-id="5be8f-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5be8f-146">OUTPUTS</span></span>

### <span data-ttu-id="5be8f-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5be8f-147">System.Boolean</span></span>

## <span data-ttu-id="5be8f-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5be8f-148">NOTES</span></span>

## <span data-ttu-id="5be8f-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5be8f-149">RELATED LINKS</span></span>
