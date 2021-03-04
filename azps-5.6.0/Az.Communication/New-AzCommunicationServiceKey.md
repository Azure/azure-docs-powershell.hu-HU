---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/new-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
ms.openlocfilehash: 4b9186265287c52c27cff6cb1a7f0d0570949e76
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938938"
---
# <span data-ttu-id="3e4f0-101">New-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="3e4f0-101">New-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="3e4f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e4f0-102">SYNOPSIS</span></span>
<span data-ttu-id="3e4f0-103">A CommunicationService hozzáférési kulcs újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-103">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="3e4f0-104">A PrimaryKey és a SecondaryKey nem lehet egyszerre újragenerálni.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-104">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="3e4f0-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3e4f0-105">SYNTAX</span></span>

### <span data-ttu-id="3e4f0-106">RegenerateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3e4f0-106">RegenerateExpanded (Default)</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyType <KeyType>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3e4f0-107">Regenerálás</span><span class="sxs-lookup"><span data-stu-id="3e4f0-107">Regenerate</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 -Parameter <IRegenerateKeyParameters> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3e4f0-108">RegenerateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3e4f0-108">RegenerateViaIdentity</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> -Parameter <IRegenerateKeyParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3e4f0-109">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3e4f0-109">RegenerateViaIdentityExpanded</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> [-KeyType <KeyType>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3e4f0-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3e4f0-110">DESCRIPTION</span></span>
<span data-ttu-id="3e4f0-111">A CommunicationService hozzáférési kulcs újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-111">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="3e4f0-112">A PrimaryKey és a SecondaryKey nem lehet egyszerre újragenerálni.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-112">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="3e4f0-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3e4f0-113">EXAMPLES</span></span>

### <span data-ttu-id="3e4f0-114">1. példa: Az Elsődleges kulcs újragenerálása IRegenerateKeyParameters hashtable segítségével</span><span class="sxs-lookup"><span data-stu-id="3e4f0-114">Example 1: Regenerates the Primary key using a IRegenerateKeyParameters hashtable</span></span>
```powershell
PS > New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Parameter @{KeyType="Primary"}

PrimaryConnectionString              PrimaryKey
-----------------------              ----------
endpoint=<example-primary-endpoint>  <example-primarykey>
```

<span data-ttu-id="3e4f0-115">Érvényteleníti az előző Elsődleges kulcsot, újat hoz létre, és visszaadja azt.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-115">Invalidates the previous Primary key, regenerate a new one and return it.</span></span>

### <span data-ttu-id="3e4f0-116">2. példa: A Másodlagos kulcs újragenerálása egy kulcstípussal</span><span class="sxs-lookup"><span data-stu-id="3e4f0-116">Example 2: Regenerates the Secondary key using a KeyType</span></span>
```powershell
PS C:\> New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -KeyType Secondary

SecondaryConnectionString               SecondaryKey
-----------------------                 ----------
endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="3e4f0-117">Érvényteleníti az előző másodlagos kulcsot, újat hoz létre, és visszaadja azt.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-117">Invalidates the previous Secondary key, regenerate a new one and return it.</span></span>

## <span data-ttu-id="3e4f0-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e4f0-118">PARAMETERS</span></span>

### <span data-ttu-id="3e4f0-119">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="3e4f0-119">-CommunicationServiceName</span></span>
<span data-ttu-id="3e4f0-120">A CommunicationService erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e4f0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e4f0-121">-DefaultProfile</span></span>
<span data-ttu-id="3e4f0-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e4f0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e4f0-123">-InputObject</span></span>
<span data-ttu-id="3e4f0-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: RegenerateViaIdentity, RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e4f0-125">-KeyType</span><span class="sxs-lookup"><span data-stu-id="3e4f0-125">-KeyType</span></span>
<span data-ttu-id="3e4f0-126">Az újragenerálni megfelelő kulcstípus.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-126">The keyType to regenerate.</span></span>
<span data-ttu-id="3e4f0-127">"primary" (elsődleges) vagy "secondary" (case-insensitive) kell lennie.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-127">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Support.KeyType
Parameter Sets: RegenerateExpanded, RegenerateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e4f0-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="3e4f0-128">-Parameter</span></span>
<span data-ttu-id="3e4f0-129">A paraméterek ismertetik a konstrukcióhoz szükséges hozzáférési kulcsok újragenerálására vonatkozó kérést, a NOTES szakaszt a PARAMETER tulajdonságokhoz és egy kivonattábla létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-129">Parameters describes the request to regenerate access keys To construct, see NOTES section for PARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters
Parameter Sets: Regenerate, RegenerateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e4f0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e4f0-130">-ResourceGroupName</span></span>
<span data-ttu-id="3e4f0-131">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-131">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3e4f0-132">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-132">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e4f0-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3e4f0-133">-SubscriptionId</span></span>
<span data-ttu-id="3e4f0-134">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-134">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3e4f0-135">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-135">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e4f0-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e4f0-136">-Confirm</span></span>
<span data-ttu-id="3e4f0-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e4f0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e4f0-138">-WhatIf</span></span>
<span data-ttu-id="3e4f0-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e4f0-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e4f0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e4f0-141">CommonParameters</span></span>
<span data-ttu-id="3e4f0-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e4f0-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e4f0-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e4f0-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e4f0-144">INPUTS</span></span>

### <span data-ttu-id="3e4f0-145">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters</span><span class="sxs-lookup"><span data-stu-id="3e4f0-145">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters</span></span>

### <span data-ttu-id="3e4f0-146">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="3e4f0-146">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="3e4f0-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e4f0-147">OUTPUTS</span></span>

### <span data-ttu-id="3e4f0-148">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="3e4f0-148">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="3e4f0-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3e4f0-149">NOTES</span></span>

<span data-ttu-id="3e4f0-150">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3e4f0-150">ALIASES</span></span>

<span data-ttu-id="3e4f0-151">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="3e4f0-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3e4f0-152">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3e4f0-153">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3e4f0-154">INPUTOBJECT: <ICommunicationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="3e4f0-154">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3e4f0-155">`[CommunicationServiceName <String>]`: A CommunicationService erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-155">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="3e4f0-156">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="3e4f0-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3e4f0-157">`[Location <String>]`: Az Azure régió</span><span class="sxs-lookup"><span data-stu-id="3e4f0-157">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="3e4f0-158">`[OperationId <String>]`: Folyamatban lévő async-művelet azonosítója</span><span class="sxs-lookup"><span data-stu-id="3e4f0-158">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="3e4f0-159">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="3e4f0-160">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="3e4f0-161">`[SubscriptionId <String>]`: Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="3e4f0-162">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-162">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="3e4f0-163">PARAMÉTER: A paraméterek a hozzáférési <IRegenerateKeyParameters> kulcsok újragenerálására vonatkozó kérést írják le.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-163">PARAMETER <IRegenerateKeyParameters>: Parameters describes the request to regenerate access keys</span></span>
  - <span data-ttu-id="3e4f0-164">`[KeyType <KeyType?>]`: Az újragenerálni megfelelő kulcstípus.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-164">`[KeyType <KeyType?>]`: The keyType to regenerate.</span></span> <span data-ttu-id="3e4f0-165">"primary" (elsődleges) vagy "secondary" (case-insensitive) kell lennie.</span><span class="sxs-lookup"><span data-stu-id="3e4f0-165">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

## <span data-ttu-id="3e4f0-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e4f0-166">RELATED LINKS</span></span>

