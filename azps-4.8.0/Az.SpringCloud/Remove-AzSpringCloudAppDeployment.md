---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
ms.openlocfilehash: f91747d7c48521a9a14906cd873df564fadc4aa7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025972"
---
# <span data-ttu-id="d6c08-101">Remove-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="d6c08-101">Remove-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="d6c08-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6c08-102">SYNOPSIS</span></span>
<span data-ttu-id="d6c08-103">Művelet a központi telepítő törléséhez.</span><span class="sxs-lookup"><span data-stu-id="d6c08-103">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="d6c08-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6c08-104">SYNTAX</span></span>

### <span data-ttu-id="d6c08-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d6c08-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d6c08-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d6c08-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d6c08-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6c08-107">DESCRIPTION</span></span>
<span data-ttu-id="d6c08-108">Művelet a központi telepítő törléséhez.</span><span class="sxs-lookup"><span data-stu-id="d6c08-108">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="d6c08-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d6c08-109">EXAMPLES</span></span>

### <span data-ttu-id="d6c08-110">1. példa: a tavaszi Felhőbeli bevezetést eltávolíthatja név szerint.</span><span class="sxs-lookup"><span data-stu-id="d6c08-110">Example 1: Remove Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="d6c08-111">A tavaszi Felhőbeli bevezetést eltávolíthatja név szerint.</span><span class="sxs-lookup"><span data-stu-id="d6c08-111">Remove Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="d6c08-112">2. példa: a tavaszi Felhőbeli központi telepítő eltávolítása a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="d6c08-112">Example 2: Remove Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Remove-AzSpringCloudAppDeployment
```

<span data-ttu-id="d6c08-113">A tavaszi Felhőbeli központi telepítések eltávolítása a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="d6c08-113">Remove Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="d6c08-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6c08-114">PARAMETERS</span></span>

### <span data-ttu-id="d6c08-115">-Appnév</span><span class="sxs-lookup"><span data-stu-id="d6c08-115">-AppName</span></span>
<span data-ttu-id="d6c08-116">Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d6c08-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6c08-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6c08-117">-DefaultProfile</span></span>
<span data-ttu-id="d6c08-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6c08-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6c08-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6c08-119">-InputObject</span></span>
<span data-ttu-id="d6c08-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d6c08-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6c08-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d6c08-121">-Name</span></span>
<span data-ttu-id="d6c08-122">A központi telepítő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d6c08-122">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6c08-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6c08-123">-PassThru</span></span>
<span data-ttu-id="d6c08-124">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="d6c08-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d6c08-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6c08-125">-ResourceGroupName</span></span>
<span data-ttu-id="d6c08-126">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d6c08-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d6c08-127">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="d6c08-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6c08-128">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="d6c08-128">-ServiceName</span></span>
<span data-ttu-id="d6c08-129">A szolgáltatás erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="d6c08-129">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6c08-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d6c08-130">-SubscriptionId</span></span>
<span data-ttu-id="d6c08-131">Megkapja az előfizetés AZONOSÍTÓját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="d6c08-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d6c08-132">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d6c08-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6c08-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d6c08-133">-Confirm</span></span>
<span data-ttu-id="d6c08-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d6c08-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6c08-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6c08-135">-WhatIf</span></span>
<span data-ttu-id="d6c08-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d6c08-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6c08-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6c08-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6c08-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6c08-138">CommonParameters</span></span>
<span data-ttu-id="d6c08-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6c08-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6c08-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d6c08-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6c08-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6c08-141">INPUTS</span></span>

### <span data-ttu-id="d6c08-142">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="d6c08-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="d6c08-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6c08-143">OUTPUTS</span></span>

### <span data-ttu-id="d6c08-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d6c08-144">System.Boolean</span></span>

## <span data-ttu-id="d6c08-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6c08-145">NOTES</span></span>

<span data-ttu-id="d6c08-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d6c08-146">ALIASES</span></span>

<span data-ttu-id="d6c08-147">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="d6c08-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d6c08-148">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d6c08-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d6c08-149">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="d6c08-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d6c08-150">INPUTOBJECT <ISpringCloudIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="d6c08-150">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d6c08-151">`[AppName <String>]`: Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d6c08-151">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="d6c08-152">`[BindingName <String>]`: A kötési erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d6c08-152">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="d6c08-153">`[CertificateName <String>]`: A tanúsítvány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d6c08-153">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="d6c08-154">`[DeploymentName <String>]`: A telepítő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d6c08-154">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="d6c08-155">`[DomainName <String>]`: Az egyéni tartomány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d6c08-155">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="d6c08-156">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d6c08-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d6c08-157">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="d6c08-157">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="d6c08-158">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d6c08-158">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d6c08-159">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="d6c08-159">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d6c08-160">`[ServiceName <String>]`: A szolgáltatás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d6c08-160">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="d6c08-161">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót kapja.</span><span class="sxs-lookup"><span data-stu-id="d6c08-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="d6c08-162">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d6c08-162">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d6c08-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6c08-163">RELATED LINKS</span></span>

