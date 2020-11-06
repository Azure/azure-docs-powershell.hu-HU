---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/stop-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 4cdc70928f2b27ae1e1604c52e5703798a302a66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502452"
---
# <span data-ttu-id="e0d94-101">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e0d94-101">Stop-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="e0d94-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0d94-102">SYNOPSIS</span></span>
<span data-ttu-id="e0d94-103">Erőforráscsoport-telepítő lemondása</span><span class="sxs-lookup"><span data-stu-id="e0d94-103">Cancels a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0d94-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0d94-104">SYNTAX</span></span>

### <span data-ttu-id="e0d94-105">StopByResourceGroupDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e0d94-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0d94-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="e0d94-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0d94-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0d94-107">DESCRIPTION</span></span>
<span data-ttu-id="e0d94-108">A **stop-AzureRmResourceGroupDeployment** parancsmag lemond egy olyan Azure-erőforráscsoport-telepítőt, amely már nem fejeződött be.</span><span class="sxs-lookup"><span data-stu-id="e0d94-108">The **Stop-AzureRmResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="e0d94-109">Ha meg szeretné szüntetni egy központi üzembe állítást, akkor a bevezetésnek hiányos kitöltési állapottal kell rendelkeznie (például kiépítési vagy sikertelen).</span><span class="sxs-lookup"><span data-stu-id="e0d94-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="e0d94-110">Az Azure-erőforrás egy felhasználó által felügyelt entitás, például webhely, adatbázis vagy adatbázis-kiszolgáló.</span><span class="sxs-lookup"><span data-stu-id="e0d94-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="e0d94-111">Az erőforráscsoport olyan erőforrások gyűjteménye, amelyek egységként települnek.</span><span class="sxs-lookup"><span data-stu-id="e0d94-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="e0d94-112">Erőforráscsoport telepítéséhez használja az New-AzureRmResourceGroupDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e0d94-112">To deploy a resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span>

<span data-ttu-id="e0d94-113">Az New-AzureRmResource parancsmag új erőforrást hoz létre, de nem hoz létre erőforráscsoport-telepítő műveletet, amely a parancsmagot leállíthatja.</span><span class="sxs-lookup"><span data-stu-id="e0d94-113">The New-AzureRmResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="e0d94-114">Ez a parancsmag csak egy futó központi telepítőt állít le.</span><span class="sxs-lookup"><span data-stu-id="e0d94-114">This cmdlet stops only one running deployment.</span></span>

<span data-ttu-id="e0d94-115">Egy adott példány leállításához használja a *Name (név* ) paramétert.</span><span class="sxs-lookup"><span data-stu-id="e0d94-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="e0d94-116">Ha elmulasztja a *Name* paramétert, a **stop-AzureRmResourceGroupDeployment** keres egy futó példányban, és leállítja.</span><span class="sxs-lookup"><span data-stu-id="e0d94-116">If you omit the *Name* parameter, **Stop-AzureRmResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="e0d94-117">Ha a parancsmag egynél több futó bevezetést talál, a parancs nem hajtható végre.</span><span class="sxs-lookup"><span data-stu-id="e0d94-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="e0d94-118">Példák</span><span class="sxs-lookup"><span data-stu-id="e0d94-118">EXAMPLES</span></span>

## <span data-ttu-id="e0d94-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0d94-119">PARAMETERS</span></span>

### <span data-ttu-id="e0d94-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e0d94-120">-ApiVersion</span></span>
<span data-ttu-id="e0d94-121">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0d94-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e0d94-122">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="e0d94-122">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e0d94-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0d94-123">-DefaultProfile</span></span>
<span data-ttu-id="e0d94-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e0d94-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0d94-125">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="e0d94-125">-Id</span></span>
<span data-ttu-id="e0d94-126">A leállításhoz az erőforráscsoport-telepítő AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0d94-126">Specifies the ID of the resource group deployment to stop.</span></span>

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d94-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e0d94-127">-Name</span></span>
<span data-ttu-id="e0d94-128">A leállításhoz az erőforráscsoport-telepítő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0d94-128">Specifies the name of the resource group deployment to stop.</span></span>

<span data-ttu-id="e0d94-129">Ha nem adja meg ezt a paramétert, ez a parancsmag az erőforráscsoport futó példányát keresi, és leállítja.</span><span class="sxs-lookup"><span data-stu-id="e0d94-129">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="e0d94-130">Ha egynél több futó telepítőt talál, a parancs nem hajtható végre.</span><span class="sxs-lookup"><span data-stu-id="e0d94-130">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="e0d94-131">A központi telepítő nevének beszerzéséhez használja az Get-AzureRmResourceGroupDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e0d94-131">To get the deployment name, use the Get-AzureRmResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0d94-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="e0d94-132">-Pre</span></span>
<span data-ttu-id="e0d94-133">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="e0d94-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e0d94-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0d94-134">-ResourceGroupName</span></span>
<span data-ttu-id="e0d94-135">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0d94-135">Specifies the name of the resource group.</span></span>
<span data-ttu-id="e0d94-136">Ez a parancsmag leállítja a paraméter által megadott erőforráscsoport telepítését.</span><span class="sxs-lookup"><span data-stu-id="e0d94-136">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0d94-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e0d94-137">-Confirm</span></span>
<span data-ttu-id="e0d94-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e0d94-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d94-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0d94-139">-WhatIf</span></span>
<span data-ttu-id="e0d94-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e0d94-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0d94-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e0d94-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d94-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0d94-142">CommonParameters</span></span>
<span data-ttu-id="e0d94-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0d94-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0d94-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0d94-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0d94-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0d94-145">INPUTS</span></span>

### <span data-ttu-id="e0d94-146">Nincs</span><span class="sxs-lookup"><span data-stu-id="e0d94-146">None</span></span>

## <span data-ttu-id="e0d94-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0d94-147">OUTPUTS</span></span>

### <span data-ttu-id="e0d94-148">Logikai</span><span class="sxs-lookup"><span data-stu-id="e0d94-148">Boolean</span></span>

## <span data-ttu-id="e0d94-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0d94-149">NOTES</span></span>

## <span data-ttu-id="e0d94-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0d94-150">RELATED LINKS</span></span>

[<span data-ttu-id="e0d94-151">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e0d94-151">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e0d94-152">Új – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e0d94-152">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="e0d94-153">Új – AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e0d94-153">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="e0d94-154">Új – AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e0d94-154">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e0d94-155">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e0d94-155">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e0d94-156">Teszt-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e0d94-156">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


