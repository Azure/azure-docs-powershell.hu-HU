---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/restart-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudService.md
ms.openlocfilehash: e61eea1d00468937a46f90fdd6a995f5f53ff468
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920834"
---
# <span data-ttu-id="53702-101">Restart-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="53702-101">Restart-AzCloudService</span></span>

## <span data-ttu-id="53702-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53702-102">SYNOPSIS</span></span>
<span data-ttu-id="53702-103">Egy vagy több szerepkörpéldány újraindítása egy felhőszolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="53702-103">Restarts one or more role instances in a cloud service.</span></span>

## <span data-ttu-id="53702-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="53702-104">SYNTAX</span></span>

### <span data-ttu-id="53702-105">RestartExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="53702-105">RestartExpanded (Default)</span></span>
```
Restart-AzCloudService -Name <String> -ResourceGroupName <String> -RoleInstance <String[]>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="53702-106">RestartViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="53702-106">RestartViaIdentityExpanded</span></span>
```
Restart-AzCloudService -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="53702-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="53702-107">DESCRIPTION</span></span>
<span data-ttu-id="53702-108">Egy vagy több szerepkörpéldány újraindítása egy felhőszolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="53702-108">Restarts one or more role instances in a cloud service.</span></span>

## <span data-ttu-id="53702-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="53702-109">EXAMPLES</span></span>

### <span data-ttu-id="53702-110">1. példa: A felhőszolgáltatás szerepkörpéldányainak újraindítása</span><span class="sxs-lookup"><span data-stu-id="53702-110">Example 1: Restart role instances of cloud service</span></span>
```powershell
PS C:\> $roleInstances = @("ContosoFrontEnd_IN_0", "ContosoBackEnd_IN_1")
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance $roleInstances
```

<span data-ttu-id="53702-111">Ez a parancs 2 szerepkörpéldányt ContosoFrontEnd_IN_0 és ContosoBackEnd_IN_1 ContosoCS nevű felhőszolgáltatást, amely a ContosOrg nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="53702-111">This command restarts 2 role instances ContosoFrontEnd_IN_0 and ContosoBackEnd_IN_1 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="53702-112">2. példa: A felhőszolgáltatás összes szerepkörének újraindítása</span><span class="sxs-lookup"><span data-stu-id="53702-112">Example 2: Restart all roles of cloud service</span></span>
```powershell
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "*"
```

<span data-ttu-id="53702-113">Ez a parancs újraindítja a ContosoCS nevű felhőszolgáltatás összes olyan szerepkörpéldányát, amely a ContosOrg nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="53702-113">This command restarts all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="53702-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53702-114">PARAMETERS</span></span>

### <span data-ttu-id="53702-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53702-115">-AsJob</span></span>
<span data-ttu-id="53702-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="53702-116">Run the command as a job</span></span>

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

### <span data-ttu-id="53702-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53702-117">-DefaultProfile</span></span>
<span data-ttu-id="53702-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53702-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53702-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53702-119">-InputObject</span></span>
<span data-ttu-id="53702-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="53702-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RestartViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53702-121">-Name</span><span class="sxs-lookup"><span data-stu-id="53702-121">-Name</span></span>
<span data-ttu-id="53702-122">A felhőszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="53702-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53702-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="53702-123">-NoWait</span></span>
<span data-ttu-id="53702-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="53702-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="53702-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53702-125">-PassThru</span></span>
<span data-ttu-id="53702-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="53702-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="53702-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53702-127">-ResourceGroupName</span></span>
<span data-ttu-id="53702-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="53702-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53702-129">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="53702-129">-RoleInstance</span></span>
<span data-ttu-id="53702-130">A felhőbeli szolgáltatási szerepkör példánynevének listája.</span><span class="sxs-lookup"><span data-stu-id="53702-130">List of cloud service role instance names.</span></span>
<span data-ttu-id="53702-131">A "\*" érték a felhőszolgáltatás összes szerepkörpéldányát alá fogja írni.</span><span class="sxs-lookup"><span data-stu-id="53702-131">Value of '\*' will signify all role instances of the cloud service.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53702-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="53702-132">-SubscriptionId</span></span>
<span data-ttu-id="53702-133">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="53702-133">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="53702-134">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="53702-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53702-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53702-135">-Confirm</span></span>
<span data-ttu-id="53702-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="53702-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53702-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53702-137">-WhatIf</span></span>
<span data-ttu-id="53702-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="53702-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53702-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="53702-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53702-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53702-140">CommonParameters</span></span>
<span data-ttu-id="53702-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53702-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53702-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53702-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53702-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53702-143">INPUTS</span></span>

### <span data-ttu-id="53702-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="53702-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="53702-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53702-145">OUTPUTS</span></span>

### <span data-ttu-id="53702-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="53702-146">System.Boolean</span></span>

## <span data-ttu-id="53702-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="53702-147">NOTES</span></span>

<span data-ttu-id="53702-148">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="53702-148">ALIASES</span></span>

<span data-ttu-id="53702-149">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="53702-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="53702-150">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="53702-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="53702-151">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="53702-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="53702-152">INPUTOBJECT: <ICloudServiceIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="53702-152">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="53702-153">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="53702-153">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="53702-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="53702-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="53702-155">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="53702-155">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="53702-156">`[RoleInstanceName <String>]`: A szerepkörpéldány neve.</span><span class="sxs-lookup"><span data-stu-id="53702-156">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="53702-157">`[RoleName <String>]`: A szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="53702-157">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="53702-158">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="53702-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="53702-159">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="53702-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="53702-160">`[UpdateDomain <Int32?>]`: A frissítő tartományt azonosító egész értéket ad meg.</span><span class="sxs-lookup"><span data-stu-id="53702-160">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="53702-161">A frissítési tartományokat nulla alapú index azonosítja: az első frissítési tartomány azonosítója 0, a második 1 és így tovább.</span><span class="sxs-lookup"><span data-stu-id="53702-161">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="53702-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53702-162">RELATED LINKS</span></span>

