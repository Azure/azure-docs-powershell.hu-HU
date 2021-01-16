---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
ms.openlocfilehash: fa189637c9c2c1b63ab0e8dd0b00fab3f4505da0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382561"
---
# <span data-ttu-id="8157b-101">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8157b-101">Stop-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="8157b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8157b-102">SYNOPSIS</span></span>
<span data-ttu-id="8157b-103">Erőforráscsoport-telepítés megszakítása.</span><span class="sxs-lookup"><span data-stu-id="8157b-103">Cancels a resource group deployment.</span></span>

## <span data-ttu-id="8157b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8157b-104">SYNTAX</span></span>

### <span data-ttu-id="8157b-105">StopByResourceGroupDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8157b-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8157b-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="8157b-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8157b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8157b-107">DESCRIPTION</span></span>
<span data-ttu-id="8157b-108">A **Stop-AzResourceGroupDeployment** parancsmag megszakít egy Olyan Azure-erőforráscsoport-telepítést, amely elkezdődött, de nem fejeződött be.</span><span class="sxs-lookup"><span data-stu-id="8157b-108">The **Stop-AzResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="8157b-109">Az üzembe helyezés befejezéséhez a központi telepítésnek hiányos kiépítési állapotnak (például Provisioning) kell lennie, nem pedig befejezettnek (például Kiépítve vagy Sikertelen).</span><span class="sxs-lookup"><span data-stu-id="8157b-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="8157b-110">Az Azure-erőforrás egy felhasználó által felügyelt entitás, például egy webhely, adatbázis vagy adatbázis-kiszolgáló.</span><span class="sxs-lookup"><span data-stu-id="8157b-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="8157b-111">Az erőforráscsoportok erőforrás-gyűjtemények, amelyek egységként vannak üzembe telepítve.</span><span class="sxs-lookup"><span data-stu-id="8157b-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="8157b-112">Erőforráscsoport telepítéséhez használja a New-AzResourceGroupDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8157b-112">To deploy a resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="8157b-113">A New-AzResource parancsmag létrehoz egy új erőforrást, de nem indít el olyan erőforráscsoport-telepítési műveletet, amely leállhat.</span><span class="sxs-lookup"><span data-stu-id="8157b-113">The New-AzResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="8157b-114">Ez a parancsmag csak egy futó telepítést leállít.</span><span class="sxs-lookup"><span data-stu-id="8157b-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="8157b-115">A Name *paraméter* használatával leállíthatja az adott telepítést.</span><span class="sxs-lookup"><span data-stu-id="8157b-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="8157b-116">Ha kihagyja a *Name* paramétert, a **Stop-AzResourceGroupDeployment** megkeres egy futó telepítést, és leállítja azt.</span><span class="sxs-lookup"><span data-stu-id="8157b-116">If you omit the *Name* parameter, **Stop-AzResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="8157b-117">Ha a parancsmag több futó telepítést talál, a parancs nem fog sikerülni.</span><span class="sxs-lookup"><span data-stu-id="8157b-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="8157b-118">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8157b-118">EXAMPLES</span></span>

### <span data-ttu-id="8157b-119">1. példa: Erőforráscsoport üzembe helyezésének indítása és leállítása</span><span class="sxs-lookup"><span data-stu-id="8157b-119">Example 1: Starting and stopping a resource group deployment</span></span>

```powershell
PS C:\> New-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg -TemplateFile .\storage-account-create-azdeploy.json -TemplateParameterFile .\storage-account-create-azdeploy.parameters.json -AsJob

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            New-AzResourceGro...

PS C:\> Stop-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg
True

PS C:\> Get-Job 1

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Failed        True            localhost            New-AzResourceGro...
```

## <span data-ttu-id="8157b-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8157b-120">PARAMETERS</span></span>

### <span data-ttu-id="8157b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8157b-121">-DefaultProfile</span></span>
<span data-ttu-id="8157b-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8157b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8157b-123">-Id</span><span class="sxs-lookup"><span data-stu-id="8157b-123">-Id</span></span>
<span data-ttu-id="8157b-124">A leállíthatja az erőforráscsoport-telepítés azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8157b-124">Specifies the ID of the resource group deployment to stop.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8157b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8157b-125">-Name</span></span>
<span data-ttu-id="8157b-126">A leállíthatja az erőforráscsoport-telepítés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8157b-126">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="8157b-127">Ha nem adja meg ezt a paramétert, ez a parancsmag megkeres egy futó telepítést az erőforráscsoportban, és leállítja azt.</span><span class="sxs-lookup"><span data-stu-id="8157b-127">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="8157b-128">Ha egynél több futó telepítést talál, a parancs nem működik.</span><span class="sxs-lookup"><span data-stu-id="8157b-128">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="8157b-129">A központi telepítés nevének lekértérte a Get-AzResourceGroupDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8157b-129">To get the deployment name, use the Get-AzResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8157b-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="8157b-130">-Pre</span></span>
<span data-ttu-id="8157b-131">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="8157b-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8157b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8157b-132">-ResourceGroupName</span></span>
<span data-ttu-id="8157b-133">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8157b-133">Specifies the name of the resource group.</span></span>
<span data-ttu-id="8157b-134">Ez a parancsmag leállítja a paraméter által megadott erőforráscsoport telepítését.</span><span class="sxs-lookup"><span data-stu-id="8157b-134">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8157b-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8157b-135">-Confirm</span></span>
<span data-ttu-id="8157b-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8157b-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8157b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8157b-137">-WhatIf</span></span>
<span data-ttu-id="8157b-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8157b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8157b-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8157b-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8157b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8157b-140">CommonParameters</span></span>
<span data-ttu-id="8157b-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8157b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8157b-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8157b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8157b-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8157b-143">INPUTS</span></span>

### <span data-ttu-id="8157b-144">System.String</span><span class="sxs-lookup"><span data-stu-id="8157b-144">System.String</span></span>

## <span data-ttu-id="8157b-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8157b-145">OUTPUTS</span></span>

### <span data-ttu-id="8157b-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8157b-146">System.Boolean</span></span>

## <span data-ttu-id="8157b-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8157b-147">NOTES</span></span>

## <span data-ttu-id="8157b-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8157b-148">RELATED LINKS</span></span>

[<span data-ttu-id="8157b-149">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8157b-149">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="8157b-150">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="8157b-150">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="8157b-151">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8157b-151">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="8157b-152">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8157b-152">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="8157b-153">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8157b-153">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="8157b-154">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8157b-154">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


