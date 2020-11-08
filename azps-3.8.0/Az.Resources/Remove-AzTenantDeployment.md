---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: b232a3a487994fdc74fb3df4b0cf384e5e73fe32
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011786"
---
# <span data-ttu-id="4ebde-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="4ebde-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="4ebde-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ebde-102">SYNOPSIS</span></span>
<span data-ttu-id="4ebde-103">A bevezetést eltávolítja a bérlői hatókörben és az esetleges kapcsolódó műveletekben</span><span class="sxs-lookup"><span data-stu-id="4ebde-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="4ebde-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ebde-104">SYNTAX</span></span>

### <span data-ttu-id="4ebde-105">RemoveByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4ebde-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ebde-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="4ebde-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ebde-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="4ebde-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ebde-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ebde-108">DESCRIPTION</span></span>
<span data-ttu-id="4ebde-109">A **Remove-AzTenantDeployment** parancsmag a jelenlegi bérlői hatókör és az ahhoz kapcsolódó műveletek Azure-telepítését távolítja el.</span><span class="sxs-lookup"><span data-stu-id="4ebde-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="4ebde-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4ebde-110">EXAMPLES</span></span>

### <span data-ttu-id="4ebde-111">1. példa: a példány eltávolítása adott névvel</span><span class="sxs-lookup"><span data-stu-id="4ebde-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="4ebde-112">Ez a parancs eltávolítja a "RolesDeployment" telepítőt az aktuális bérlői hatókörben.</span><span class="sxs-lookup"><span data-stu-id="4ebde-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="4ebde-113">2. példa: központi üzembe állítás és eltávolítás</span><span class="sxs-lookup"><span data-stu-id="4ebde-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="4ebde-114">Ez a parancs a "RolesDeployment" üzembe helyezi az aktuális bérlői hatókört, és eltávolítja azt.</span><span class="sxs-lookup"><span data-stu-id="4ebde-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="4ebde-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ebde-115">PARAMETERS</span></span>

### <span data-ttu-id="4ebde-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4ebde-116">-ApiVersion</span></span>
<span data-ttu-id="4ebde-117">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ebde-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4ebde-118">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="4ebde-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="4ebde-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ebde-119">-AsJob</span></span>
<span data-ttu-id="4ebde-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4ebde-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ebde-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ebde-121">-DefaultProfile</span></span>
<span data-ttu-id="4ebde-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ebde-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ebde-123">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="4ebde-123">-Id</span></span>
<span data-ttu-id="4ebde-124">A központi telepítő teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4ebde-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="4ebde-125">Példa:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="4ebde-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="4ebde-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ebde-126">-InputObject</span></span>
<span data-ttu-id="4ebde-127">A központi telepítő objektum.</span><span class="sxs-lookup"><span data-stu-id="4ebde-127">The deployment object.</span></span>

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

### <span data-ttu-id="4ebde-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4ebde-128">-Name</span></span>
<span data-ttu-id="4ebde-129">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="4ebde-129">The name of the deployment.</span></span>

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

### <span data-ttu-id="4ebde-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ebde-130">-PassThru</span></span>
<span data-ttu-id="4ebde-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4ebde-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="4ebde-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="4ebde-132">-Pre</span></span>
<span data-ttu-id="4ebde-133">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="4ebde-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4ebde-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4ebde-134">-Confirm</span></span>
<span data-ttu-id="4ebde-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4ebde-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ebde-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ebde-136">-WhatIf</span></span>
<span data-ttu-id="4ebde-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4ebde-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ebde-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4ebde-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ebde-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ebde-139">CommonParameters</span></span>
<span data-ttu-id="4ebde-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ebde-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ebde-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4ebde-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ebde-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ebde-142">INPUTS</span></span>

### <span data-ttu-id="4ebde-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="4ebde-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="4ebde-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ebde-144">OUTPUTS</span></span>

### <span data-ttu-id="4ebde-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4ebde-145">System.Boolean</span></span>

## <span data-ttu-id="4ebde-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ebde-146">NOTES</span></span>

## <span data-ttu-id="4ebde-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ebde-147">RELATED LINKS</span></span>
