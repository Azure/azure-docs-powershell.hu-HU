---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzDeployment.md
ms.openlocfilehash: 3db7d3b0b27cd49207871ba7b9d47d5b79e661fc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843262"
---
# <span data-ttu-id="f0fd4-101">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f0fd4-101">Remove-AzDeployment</span></span>

## <span data-ttu-id="f0fd4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f0fd4-102">SYNOPSIS</span></span>
<span data-ttu-id="f0fd4-103">A telepített példányok és a hozzájuk kapcsolódó műveletek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f0fd4-103">Removes a deployment and any associated operations</span></span>

## <span data-ttu-id="f0fd4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f0fd4-104">SYNTAX</span></span>

### <span data-ttu-id="f0fd4-105">RemoveByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f0fd4-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzDeployment [-Name] <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0fd4-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="f0fd4-106">RemoveByDeploymentId</span></span>
```
Remove-AzDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0fd4-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="f0fd4-107">RemoveByInputObject</span></span>
```
Remove-AzDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0fd4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f0fd4-108">DESCRIPTION</span></span>
<span data-ttu-id="f0fd4-109">A **Remove-AzDeployment** parancsmag az Azure-üzembe helyezi az előfizetéses hatókört, valamint bármely kapcsolódó műveletet.</span><span class="sxs-lookup"><span data-stu-id="f0fd4-109">The **Remove-AzDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="f0fd4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f0fd4-110">EXAMPLES</span></span>

### <span data-ttu-id="f0fd4-111">1. példa: a példány eltávolítása adott névvel</span><span class="sxs-lookup"><span data-stu-id="f0fd4-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzDeployment -Name "RolesDeployment"
```

<span data-ttu-id="f0fd4-112">Ez a parancs eltávolítja a "RolesDeployment" telepítőt az aktuális előfizetési tartományon.</span><span class="sxs-lookup"><span data-stu-id="f0fd4-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="f0fd4-113">2. példa: központi üzembe állítás és eltávolítás</span><span class="sxs-lookup"><span data-stu-id="f0fd4-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Remove-AzDeployment
```

<span data-ttu-id="f0fd4-114">A parancs a jelenlegi előfizetési tartomány "RolesDeployment" beállítását kapja, és eltávolítja azt.</span><span class="sxs-lookup"><span data-stu-id="f0fd4-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="f0fd4-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f0fd4-115">PARAMETERS</span></span>

### <span data-ttu-id="f0fd4-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f0fd4-116">-ApiVersion</span></span>
<span data-ttu-id="f0fd4-117">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f0fd4-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f0fd4-118">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="f0fd4-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f0fd4-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0fd4-119">-AsJob</span></span>
<span data-ttu-id="f0fd4-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f0fd4-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0fd4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0fd4-121">-DefaultProfile</span></span>
<span data-ttu-id="f0fd4-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f0fd4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0fd4-123">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="f0fd4-123">-Id</span></span>
<span data-ttu-id="f0fd4-124">A központi telepítő teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f0fd4-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="f0fd4-125">Példa:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="f0fd4-125">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0fd4-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0fd4-126">-InputObject</span></span>
<span data-ttu-id="f0fd4-127">A központi telepítő objektum.</span><span class="sxs-lookup"><span data-stu-id="f0fd4-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0fd4-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f0fd4-128">-Name</span></span>
<span data-ttu-id="f0fd4-129">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="f0fd4-129">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0fd4-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0fd4-130">-PassThru</span></span>
<span data-ttu-id="f0fd4-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f0fd4-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f0fd4-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="f0fd4-132">-Pre</span></span>
<span data-ttu-id="f0fd4-133">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="f0fd4-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f0fd4-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f0fd4-134">-Confirm</span></span>
<span data-ttu-id="f0fd4-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f0fd4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0fd4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0fd4-136">-WhatIf</span></span>
<span data-ttu-id="f0fd4-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f0fd4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0fd4-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f0fd4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0fd4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0fd4-139">CommonParameters</span></span>
<span data-ttu-id="f0fd4-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f0fd4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0fd4-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0fd4-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0fd4-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0fd4-142">INPUTS</span></span>

### <span data-ttu-id="f0fd4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f0fd4-143">System.String</span></span>

## <span data-ttu-id="f0fd4-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0fd4-144">OUTPUTS</span></span>

### <span data-ttu-id="f0fd4-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f0fd4-145">System.Boolean</span></span>

## <span data-ttu-id="f0fd4-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f0fd4-146">NOTES</span></span>

## <span data-ttu-id="f0fd4-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f0fd4-147">RELATED LINKS</span></span>
