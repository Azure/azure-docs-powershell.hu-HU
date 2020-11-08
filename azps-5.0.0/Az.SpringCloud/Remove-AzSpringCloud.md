---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
ms.openlocfilehash: 913011a9230b70c59b772eae306913c1e1e87432
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185229"
---
# <span data-ttu-id="387e1-101">Remove-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="387e1-101">Remove-AzSpringCloud</span></span>

## <span data-ttu-id="387e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="387e1-102">SYNOPSIS</span></span>
<span data-ttu-id="387e1-103">A szolgáltatás törlésére szolgáló művelet.</span><span class="sxs-lookup"><span data-stu-id="387e1-103">Operation to delete a Service.</span></span>

## <span data-ttu-id="387e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="387e1-104">SYNTAX</span></span>

### <span data-ttu-id="387e1-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="387e1-105">Delete (Default)</span></span>
```
Remove-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="387e1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="387e1-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="387e1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="387e1-107">DESCRIPTION</span></span>
<span data-ttu-id="387e1-108">A szolgáltatás törlésére szolgáló művelet.</span><span class="sxs-lookup"><span data-stu-id="387e1-108">Operation to delete a Service.</span></span>

## <span data-ttu-id="387e1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="387e1-109">EXAMPLES</span></span>

### <span data-ttu-id="387e1-110">1. példa: a tavaszi Felhőbeli szolgáltatás eltávolítása név szerint.</span><span class="sxs-lookup"><span data-stu-id="387e1-110">Example 1: Remove Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
```

<span data-ttu-id="387e1-111">A tavaszi felhő szolgáltatás eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="387e1-111">Remove Spring Cloud Service by name.</span></span>

### <span data-ttu-id="387e1-112">2. példa: a tavaszi felhő szolgáltatás eltávolítása a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="387e1-112">Example 2: Remove Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Remove-AzSpringCloud
```

<span data-ttu-id="387e1-113">A tavaszi felhő szolgáltatás eltávolítása a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="387e1-113">Remove Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="387e1-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="387e1-114">PARAMETERS</span></span>

### <span data-ttu-id="387e1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="387e1-115">-AsJob</span></span>
<span data-ttu-id="387e1-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="387e1-116">Run the command as a job</span></span>

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

### <span data-ttu-id="387e1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="387e1-117">-DefaultProfile</span></span>
<span data-ttu-id="387e1-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="387e1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="387e1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="387e1-119">-InputObject</span></span>
<span data-ttu-id="387e1-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="387e1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="387e1-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="387e1-121">-Name</span></span>
<span data-ttu-id="387e1-122">A szolgáltatás erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="387e1-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387e1-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="387e1-123">-NoWait</span></span>
<span data-ttu-id="387e1-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="387e1-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="387e1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="387e1-125">-PassThru</span></span>
<span data-ttu-id="387e1-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="387e1-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="387e1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="387e1-127">-ResourceGroupName</span></span>
<span data-ttu-id="387e1-128">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="387e1-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="387e1-129">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="387e1-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="387e1-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="387e1-130">-SubscriptionId</span></span>
<span data-ttu-id="387e1-131">Megkapja az előfizetés AZONOSÍTÓját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="387e1-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="387e1-132">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="387e1-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="387e1-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="387e1-133">-Confirm</span></span>
<span data-ttu-id="387e1-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="387e1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="387e1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="387e1-135">-WhatIf</span></span>
<span data-ttu-id="387e1-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="387e1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="387e1-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="387e1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="387e1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="387e1-138">CommonParameters</span></span>
<span data-ttu-id="387e1-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="387e1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="387e1-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="387e1-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="387e1-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="387e1-141">INPUTS</span></span>

### <span data-ttu-id="387e1-142">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="387e1-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="387e1-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="387e1-143">OUTPUTS</span></span>

### <span data-ttu-id="387e1-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="387e1-144">System.Boolean</span></span>

## <span data-ttu-id="387e1-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="387e1-145">NOTES</span></span>

<span data-ttu-id="387e1-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="387e1-146">ALIASES</span></span>

<span data-ttu-id="387e1-147">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="387e1-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="387e1-148">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="387e1-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="387e1-149">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="387e1-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="387e1-150">INPUTOBJECT <ISpringCloudIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="387e1-150">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="387e1-151">`[AppName <String>]`: Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="387e1-151">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="387e1-152">`[BindingName <String>]`: A kötési erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="387e1-152">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="387e1-153">`[CertificateName <String>]`: A tanúsítvány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="387e1-153">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="387e1-154">`[DeploymentName <String>]`: A telepítő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="387e1-154">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="387e1-155">`[DomainName <String>]`: Az egyéni tartomány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="387e1-155">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="387e1-156">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="387e1-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="387e1-157">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="387e1-157">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="387e1-158">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="387e1-158">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="387e1-159">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="387e1-159">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="387e1-160">`[ServiceName <String>]`: A szolgáltatás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="387e1-160">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="387e1-161">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót kapja.</span><span class="sxs-lookup"><span data-stu-id="387e1-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="387e1-162">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="387e1-162">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="387e1-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="387e1-163">RELATED LINKS</span></span>

