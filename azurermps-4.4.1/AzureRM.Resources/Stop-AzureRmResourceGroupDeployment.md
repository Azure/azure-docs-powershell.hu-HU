---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: f07b2f59f1a38aca780e1e869bb3904725df6dcd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680487"
---
# <span data-ttu-id="ea4b8-101">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ea4b8-101">Stop-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="ea4b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ea4b8-102">SYNOPSIS</span></span>
<span data-ttu-id="ea4b8-103">Erőforráscsoport-telepítő lemondása</span><span class="sxs-lookup"><span data-stu-id="ea4b8-103">Cancels a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea4b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ea4b8-104">SYNTAX</span></span>

### <span data-ttu-id="ea4b8-105">A telepítő név paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-105">The deployment name parameter set.</span></span> <span data-ttu-id="ea4b8-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="ea4b8-106">(Default)</span></span>
```
Stop-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea4b8-107">A telepítő-azonosító paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-107">The deployment Id parameter set.</span></span>
```
Stop-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea4b8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ea4b8-108">DESCRIPTION</span></span>
<span data-ttu-id="ea4b8-109">A **stop-AzureRmResourceGroupDeployment** parancsmag lemond egy olyan Azure-erőforráscsoport-telepítőt, amely már nem fejeződött be.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-109">The **Stop-AzureRmResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="ea4b8-110">Ha meg szeretné szüntetni egy központi üzembe állítást, akkor a bevezetésnek hiányos kitöltési állapottal kell rendelkeznie (például kiépítési vagy sikertelen).</span><span class="sxs-lookup"><span data-stu-id="ea4b8-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="ea4b8-111">Az Azure-erőforrás egy felhasználó által felügyelt entitás, például webhely, adatbázis vagy adatbázis-kiszolgáló.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-111">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="ea4b8-112">Az erőforráscsoport olyan erőforrások gyűjteménye, amelyek egységként települnek.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-112">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="ea4b8-113">Erőforráscsoport telepítéséhez használja az New-AzureRmResourceGroupDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-113">To deploy a resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span>

<span data-ttu-id="ea4b8-114">Az New-AzureRmResource parancsmag új erőforrást hoz létre, de nem hoz létre erőforráscsoport-telepítő műveletet, amely a parancsmagot leállíthatja.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-114">The New-AzureRmResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="ea4b8-115">Ez a parancsmag csak egy futó központi telepítőt állít le.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-115">This cmdlet stops only one running deployment.</span></span>

<span data-ttu-id="ea4b8-116">Egy adott példány leállításához használja a *Name (név* ) paramétert.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-116">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="ea4b8-117">Ha elmulasztja a *Name* paramétert, a **stop-AzureRmResourceGroupDeployment** keres egy futó példányban, és leállítja.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-117">If you omit the *Name* parameter, **Stop-AzureRmResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="ea4b8-118">Ha a parancsmag egynél több futó bevezetést talál, a parancs nem hajtható végre.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-118">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="ea4b8-119">Példák</span><span class="sxs-lookup"><span data-stu-id="ea4b8-119">EXAMPLES</span></span>

## <span data-ttu-id="ea4b8-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ea4b8-120">PARAMETERS</span></span>

### <span data-ttu-id="ea4b8-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ea4b8-121">-ApiVersion</span></span>
<span data-ttu-id="ea4b8-122">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="ea4b8-123">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="ea4b8-124">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="ea4b8-124">-Id</span></span>
<span data-ttu-id="ea4b8-125">A leállításhoz az erőforráscsoport-telepítő AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-125">Specifies the ID of the resource group deployment to stop.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment Id parameter set.
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea4b8-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ea4b8-126">-Name</span></span>
<span data-ttu-id="ea4b8-127">A leállításhoz az erőforráscsoport-telepítő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-127">Specifies the name of the resource group deployment to stop.</span></span>

<span data-ttu-id="ea4b8-128">Ha nem adja meg ezt a paramétert, ez a parancsmag az erőforráscsoport futó példányát keresi, és leállítja.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-128">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="ea4b8-129">Ha egynél több futó telepítőt talál, a parancs nem hajtható végre.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-129">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="ea4b8-130">A központi telepítő nevének beszerzéséhez használja az Get-AzureRmResourceGroupDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-130">To get the deployment name, use the Get-AzureRmResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea4b8-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="ea4b8-131">-Pre</span></span>
<span data-ttu-id="ea4b8-132">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ea4b8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea4b8-133">-ResourceGroupName</span></span>
<span data-ttu-id="ea4b8-134">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-134">Specifies the name of the resource group.</span></span>
<span data-ttu-id="ea4b8-135">Ez a parancsmag leállítja a paraméter által megadott erőforráscsoport telepítését.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-135">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea4b8-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ea4b8-136">-Confirm</span></span>
<span data-ttu-id="ea4b8-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea4b8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea4b8-138">-WhatIf</span></span>
<span data-ttu-id="ea4b8-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea4b8-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea4b8-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea4b8-141">-DefaultProfile</span></span>
<span data-ttu-id="ea4b8-142">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea4b8-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea4b8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea4b8-143">CommonParameters</span></span>
<span data-ttu-id="ea4b8-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ea4b8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea4b8-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea4b8-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea4b8-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea4b8-146">INPUTS</span></span>

### <span data-ttu-id="ea4b8-147">Nincs</span><span class="sxs-lookup"><span data-stu-id="ea4b8-147">None</span></span>

## <span data-ttu-id="ea4b8-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea4b8-148">OUTPUTS</span></span>

### <span data-ttu-id="ea4b8-149">Logikai</span><span class="sxs-lookup"><span data-stu-id="ea4b8-149">Boolean</span></span>

## <span data-ttu-id="ea4b8-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ea4b8-150">NOTES</span></span>

## <span data-ttu-id="ea4b8-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea4b8-151">RELATED LINKS</span></span>

[<span data-ttu-id="ea4b8-152">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ea4b8-152">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="ea4b8-153">Új – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ea4b8-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="ea4b8-154">Új – AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ea4b8-154">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="ea4b8-155">Új – AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ea4b8-155">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="ea4b8-156">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ea4b8-156">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="ea4b8-157">Teszt-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ea4b8-157">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


