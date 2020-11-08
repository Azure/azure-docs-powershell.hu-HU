---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: ace761bfd329c756baa27d1bff6300f2e030f377
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183928"
---
# <span data-ttu-id="f4f43-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="f4f43-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="f4f43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4f43-102">SYNOPSIS</span></span>
<span data-ttu-id="f4f43-103">Műveletet törölhet egy alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="f4f43-103">Operation to delete an App.</span></span>

## <span data-ttu-id="f4f43-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4f43-104">SYNTAX</span></span>

### <span data-ttu-id="f4f43-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f4f43-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f4f43-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f4f43-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f4f43-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4f43-107">DESCRIPTION</span></span>
<span data-ttu-id="f4f43-108">Műveletet törölhet egy alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="f4f43-108">Operation to delete an App.</span></span>

## <span data-ttu-id="f4f43-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f4f43-109">EXAMPLES</span></span>

### <span data-ttu-id="f4f43-110">1. példa: a tavaszi felhő alkalmazás eltávolítása név szerint.</span><span class="sxs-lookup"><span data-stu-id="f4f43-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="f4f43-111">A tavaszi felhő alkalmazás eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="f4f43-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="f4f43-112">2. példa: a tavaszi felhő alkalmazás eltávolítása a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="f4f43-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="f4f43-113">A tavaszi felhő alkalmazás eltávolítása a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="f4f43-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="f4f43-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4f43-114">PARAMETERS</span></span>

### <span data-ttu-id="f4f43-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4f43-115">-DefaultProfile</span></span>
<span data-ttu-id="f4f43-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4f43-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4f43-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4f43-117">-InputObject</span></span>
<span data-ttu-id="f4f43-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f4f43-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f4f43-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f4f43-119">-Name</span></span>
<span data-ttu-id="f4f43-120">Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f4f43-120">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4f43-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4f43-121">-PassThru</span></span>
<span data-ttu-id="f4f43-122">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="f4f43-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f4f43-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4f43-123">-ResourceGroupName</span></span>
<span data-ttu-id="f4f43-124">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f4f43-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f4f43-125">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="f4f43-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f4f43-126">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="f4f43-126">-ServiceName</span></span>
<span data-ttu-id="f4f43-127">A szolgáltatás erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="f4f43-127">The name of the Service resource.</span></span>

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

### <span data-ttu-id="f4f43-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4f43-128">-SubscriptionId</span></span>
<span data-ttu-id="f4f43-129">Megkapja az előfizetés AZONOSÍTÓját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="f4f43-129">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f4f43-130">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f4f43-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f4f43-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f4f43-131">-Confirm</span></span>
<span data-ttu-id="f4f43-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f4f43-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4f43-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4f43-133">-WhatIf</span></span>
<span data-ttu-id="f4f43-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f4f43-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4f43-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f4f43-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4f43-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4f43-136">CommonParameters</span></span>
<span data-ttu-id="f4f43-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4f43-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4f43-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f4f43-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4f43-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4f43-139">INPUTS</span></span>

### <span data-ttu-id="f4f43-140">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="f4f43-140">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="f4f43-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4f43-141">OUTPUTS</span></span>

### <span data-ttu-id="f4f43-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4f43-142">System.Boolean</span></span>

## <span data-ttu-id="f4f43-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4f43-143">NOTES</span></span>

<span data-ttu-id="f4f43-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f4f43-144">ALIASES</span></span>

<span data-ttu-id="f4f43-145">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="f4f43-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f4f43-146">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="f4f43-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f4f43-147">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="f4f43-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f4f43-148">INPUTOBJECT <ISpringCloudIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="f4f43-148">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f4f43-149">`[AppName <String>]`: Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f4f43-149">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="f4f43-150">`[BindingName <String>]`: A kötési erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f4f43-150">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="f4f43-151">`[CertificateName <String>]`: A tanúsítvány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f4f43-151">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="f4f43-152">`[DeploymentName <String>]`: A telepítő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f4f43-152">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="f4f43-153">`[DomainName <String>]`: Az egyéni tartomány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f4f43-153">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="f4f43-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f4f43-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f4f43-155">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="f4f43-155">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="f4f43-156">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f4f43-156">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="f4f43-157">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="f4f43-157">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="f4f43-158">`[ServiceName <String>]`: A szolgáltatás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f4f43-158">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="f4f43-159">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót kapja.</span><span class="sxs-lookup"><span data-stu-id="f4f43-159">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="f4f43-160">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f4f43-160">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f4f43-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4f43-161">RELATED LINKS</span></span>

