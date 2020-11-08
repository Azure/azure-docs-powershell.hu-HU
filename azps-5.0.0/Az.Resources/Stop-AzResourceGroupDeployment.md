---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
ms.openlocfilehash: fa189637c9c2c1b63ab0e8dd0b00fab3f4505da0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185691"
---
# <span data-ttu-id="ce9b4-101">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ce9b4-101">Stop-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="ce9b4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ce9b4-102">SYNOPSIS</span></span>
<span data-ttu-id="ce9b4-103">Erőforráscsoport-telepítő lemondása</span><span class="sxs-lookup"><span data-stu-id="ce9b4-103">Cancels a resource group deployment.</span></span>

## <span data-ttu-id="ce9b4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ce9b4-104">SYNTAX</span></span>

### <span data-ttu-id="ce9b4-105">StopByResourceGroupDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ce9b4-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce9b4-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ce9b4-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce9b4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ce9b4-107">DESCRIPTION</span></span>
<span data-ttu-id="ce9b4-108">A **stop-AzResourceGroupDeployment** parancsmag lemond egy olyan Azure-erőforráscsoport-telepítőt, amely már nem fejeződött be.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-108">The **Stop-AzResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="ce9b4-109">Ha meg szeretné szüntetni egy központi üzembe állítást, akkor a bevezetésnek hiányos kitöltési állapottal kell rendelkeznie (például kiépítési vagy sikertelen).</span><span class="sxs-lookup"><span data-stu-id="ce9b4-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="ce9b4-110">Az Azure-erőforrás egy felhasználó által felügyelt entitás, például webhely, adatbázis vagy adatbázis-kiszolgáló.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="ce9b4-111">Az erőforráscsoport olyan erőforrások gyűjteménye, amelyek egységként települnek.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="ce9b4-112">Erőforráscsoport telepítéséhez használja az New-AzResourceGroupDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-112">To deploy a resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="ce9b4-113">Az New-AzResource parancsmag új erőforrást hoz létre, de nem hoz létre erőforráscsoport-telepítő műveletet, amely a parancsmagot leállíthatja.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-113">The New-AzResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="ce9b4-114">Ez a parancsmag csak egy futó központi telepítőt állít le.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="ce9b4-115">Egy adott példány leállításához használja a *Name (név* ) paramétert.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="ce9b4-116">Ha elmulasztja a *Name* paramétert, a **stop-AzResourceGroupDeployment** keres egy futó példányban, és leállítja.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-116">If you omit the *Name* parameter, **Stop-AzResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="ce9b4-117">Ha a parancsmag egynél több futó bevezetést talál, a parancs nem hajtható végre.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="ce9b4-118">Példák</span><span class="sxs-lookup"><span data-stu-id="ce9b4-118">EXAMPLES</span></span>

### <span data-ttu-id="ce9b4-119">Példa 1: erőforráscsoport-telepítő indítása és leállítása</span><span class="sxs-lookup"><span data-stu-id="ce9b4-119">Example 1: Starting and stopping a resource group deployment</span></span>

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

## <span data-ttu-id="ce9b4-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ce9b4-120">PARAMETERS</span></span>

### <span data-ttu-id="ce9b4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce9b4-121">-DefaultProfile</span></span>
<span data-ttu-id="ce9b4-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ce9b4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce9b4-123">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="ce9b4-123">-Id</span></span>
<span data-ttu-id="ce9b4-124">A leállításhoz az erőforráscsoport-telepítő AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-124">Specifies the ID of the resource group deployment to stop.</span></span>

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

### <span data-ttu-id="ce9b4-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ce9b4-125">-Name</span></span>
<span data-ttu-id="ce9b4-126">A leállításhoz az erőforráscsoport-telepítő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-126">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="ce9b4-127">Ha nem adja meg ezt a paramétert, ez a parancsmag az erőforráscsoport futó példányát keresi, és leállítja.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-127">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="ce9b4-128">Ha egynél több futó telepítőt talál, a parancs nem hajtható végre.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-128">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="ce9b4-129">A központi telepítő nevének beszerzéséhez használja az Get-AzResourceGroupDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-129">To get the deployment name, use the Get-AzResourceGroupDeployment cmdlet.</span></span>

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

### <span data-ttu-id="ce9b4-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="ce9b4-130">-Pre</span></span>
<span data-ttu-id="ce9b4-131">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ce9b4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce9b4-132">-ResourceGroupName</span></span>
<span data-ttu-id="ce9b4-133">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-133">Specifies the name of the resource group.</span></span>
<span data-ttu-id="ce9b4-134">Ez a parancsmag leállítja a paraméter által megadott erőforráscsoport telepítését.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-134">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ce9b4-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ce9b4-135">-Confirm</span></span>
<span data-ttu-id="ce9b4-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce9b4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce9b4-137">-WhatIf</span></span>
<span data-ttu-id="ce9b4-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce9b4-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce9b4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce9b4-140">CommonParameters</span></span>
<span data-ttu-id="ce9b4-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ce9b4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce9b4-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce9b4-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce9b4-143">INPUTS</span></span>

### <span data-ttu-id="ce9b4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ce9b4-144">System.String</span></span>

## <span data-ttu-id="ce9b4-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce9b4-145">OUTPUTS</span></span>

### <span data-ttu-id="ce9b4-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ce9b4-146">System.Boolean</span></span>

## <span data-ttu-id="ce9b4-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ce9b4-147">NOTES</span></span>

## <span data-ttu-id="ce9b4-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce9b4-148">RELATED LINKS</span></span>

[<span data-ttu-id="ce9b4-149">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ce9b4-149">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="ce9b4-150">Új – AzResource</span><span class="sxs-lookup"><span data-stu-id="ce9b4-150">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="ce9b4-151">Új – AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ce9b4-151">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="ce9b4-152">Új – AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ce9b4-152">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="ce9b4-153">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ce9b4-153">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="ce9b4-154">Teszt-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ce9b4-154">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


