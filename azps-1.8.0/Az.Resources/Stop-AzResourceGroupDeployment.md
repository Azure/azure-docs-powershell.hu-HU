---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
ms.openlocfilehash: 2daec87c79e02d6aa4d2720bb20cac5194d1a752
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669299"
---
# <span data-ttu-id="310bc-101">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="310bc-101">Stop-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="310bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="310bc-102">SYNOPSIS</span></span>
<span data-ttu-id="310bc-103">Erőforráscsoport-telepítő lemondása</span><span class="sxs-lookup"><span data-stu-id="310bc-103">Cancels a resource group deployment.</span></span>

## <span data-ttu-id="310bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="310bc-104">SYNTAX</span></span>

### <span data-ttu-id="310bc-105">StopByResourceGroupDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="310bc-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="310bc-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="310bc-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="310bc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="310bc-107">DESCRIPTION</span></span>
<span data-ttu-id="310bc-108">A **stop-AzResourceGroupDeployment** parancsmag lemond egy olyan Azure-erőforráscsoport-telepítőt, amely már nem fejeződött be.</span><span class="sxs-lookup"><span data-stu-id="310bc-108">The **Stop-AzResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="310bc-109">Ha meg szeretné szüntetni egy központi üzembe állítást, akkor a bevezetésnek hiányos kitöltési állapottal kell rendelkeznie (például kiépítési vagy sikertelen).</span><span class="sxs-lookup"><span data-stu-id="310bc-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="310bc-110">Az Azure-erőforrás egy felhasználó által felügyelt entitás, például webhely, adatbázis vagy adatbázis-kiszolgáló.</span><span class="sxs-lookup"><span data-stu-id="310bc-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="310bc-111">Az erőforráscsoport olyan erőforrások gyűjteménye, amelyek egységként települnek.</span><span class="sxs-lookup"><span data-stu-id="310bc-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="310bc-112">Erőforráscsoport telepítéséhez használja az New-AzResourceGroupDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="310bc-112">To deploy a resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="310bc-113">Az New-AzResource parancsmag új erőforrást hoz létre, de nem hoz létre erőforráscsoport-telepítő műveletet, amely a parancsmagot leállíthatja.</span><span class="sxs-lookup"><span data-stu-id="310bc-113">The New-AzResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="310bc-114">Ez a parancsmag csak egy futó központi telepítőt állít le.</span><span class="sxs-lookup"><span data-stu-id="310bc-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="310bc-115">Egy adott példány leállításához használja a *Name (név* ) paramétert.</span><span class="sxs-lookup"><span data-stu-id="310bc-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="310bc-116">Ha elmulasztja a *Name* paramétert, a **stop-AzResourceGroupDeployment** keres egy futó példányban, és leállítja.</span><span class="sxs-lookup"><span data-stu-id="310bc-116">If you omit the *Name* parameter, **Stop-AzResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="310bc-117">Ha a parancsmag egynél több futó bevezetést talál, a parancs nem hajtható végre.</span><span class="sxs-lookup"><span data-stu-id="310bc-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="310bc-118">Példák</span><span class="sxs-lookup"><span data-stu-id="310bc-118">EXAMPLES</span></span>

### <span data-ttu-id="310bc-119">Példa 1: erőforráscsoport-telepítő indítása és leállítása</span><span class="sxs-lookup"><span data-stu-id="310bc-119">Example 1: Starting and stopping a resource group deployment</span></span>

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

## <span data-ttu-id="310bc-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="310bc-120">PARAMETERS</span></span>

### <span data-ttu-id="310bc-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="310bc-121">-ApiVersion</span></span>
<span data-ttu-id="310bc-122">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="310bc-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="310bc-123">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="310bc-123">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="310bc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="310bc-124">-DefaultProfile</span></span>
<span data-ttu-id="310bc-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="310bc-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="310bc-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="310bc-126">-Id</span></span>
<span data-ttu-id="310bc-127">A leállításhoz az erőforráscsoport-telepítő AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="310bc-127">Specifies the ID of the resource group deployment to stop.</span></span>

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

### <span data-ttu-id="310bc-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="310bc-128">-Name</span></span>
<span data-ttu-id="310bc-129">A leállításhoz az erőforráscsoport-telepítő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="310bc-129">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="310bc-130">Ha nem adja meg ezt a paramétert, ez a parancsmag az erőforráscsoport futó példányát keresi, és leállítja.</span><span class="sxs-lookup"><span data-stu-id="310bc-130">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="310bc-131">Ha egynél több futó telepítőt talál, a parancs nem hajtható végre.</span><span class="sxs-lookup"><span data-stu-id="310bc-131">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="310bc-132">A központi telepítő nevének beszerzéséhez használja az Get-AzResourceGroupDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="310bc-132">To get the deployment name, use the Get-AzResourceGroupDeployment cmdlet.</span></span>

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

### <span data-ttu-id="310bc-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="310bc-133">-Pre</span></span>
<span data-ttu-id="310bc-134">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="310bc-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="310bc-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="310bc-135">-ResourceGroupName</span></span>
<span data-ttu-id="310bc-136">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="310bc-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="310bc-137">Ez a parancsmag leállítja a paraméter által megadott erőforráscsoport telepítését.</span><span class="sxs-lookup"><span data-stu-id="310bc-137">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="310bc-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="310bc-138">-Confirm</span></span>
<span data-ttu-id="310bc-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="310bc-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="310bc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="310bc-140">-WhatIf</span></span>
<span data-ttu-id="310bc-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="310bc-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="310bc-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="310bc-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="310bc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="310bc-143">CommonParameters</span></span>
<span data-ttu-id="310bc-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="310bc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="310bc-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="310bc-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="310bc-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="310bc-146">INPUTS</span></span>

### <span data-ttu-id="310bc-147">System. String</span><span class="sxs-lookup"><span data-stu-id="310bc-147">System.String</span></span>

## <span data-ttu-id="310bc-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="310bc-148">OUTPUTS</span></span>

### <span data-ttu-id="310bc-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="310bc-149">System.Boolean</span></span>

## <span data-ttu-id="310bc-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="310bc-150">NOTES</span></span>

## <span data-ttu-id="310bc-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="310bc-151">RELATED LINKS</span></span>

[<span data-ttu-id="310bc-152">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="310bc-152">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="310bc-153">Új – AzResource</span><span class="sxs-lookup"><span data-stu-id="310bc-153">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="310bc-154">Új – AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="310bc-154">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="310bc-155">Új – AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="310bc-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="310bc-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="310bc-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="310bc-157">Teszt-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="310bc-157">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


