---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/stop-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Stop-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Stop-AzCloudService.md
ms.openlocfilehash: 1417cc797935a532decf886f0c814ef32deee3aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166634"
---
# <span data-ttu-id="3eccf-101">Stop-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="3eccf-101">Stop-AzCloudService</span></span>

## <span data-ttu-id="3eccf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3eccf-102">SYNOPSIS</span></span>
<span data-ttu-id="3eccf-103">Kikapcsolja a felhőszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="3eccf-103">Power off the cloud service.</span></span>
<span data-ttu-id="3eccf-104">Felhívjuk a figyelmét arra, hogy az erőforrások továbbra is csatolva vannak, és az erőforrásokért díjat számítunk fel.</span><span class="sxs-lookup"><span data-stu-id="3eccf-104">Note that resources are still attached and you are getting charged for the resources.</span></span>

## <span data-ttu-id="3eccf-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3eccf-105">SYNTAX</span></span>

### <span data-ttu-id="3eccf-106">PowerOff (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3eccf-106">PowerOff (Default)</span></span>
```
Stop-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3eccf-107">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3eccf-107">PowerOffViaIdentity</span></span>
```
Stop-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3eccf-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3eccf-108">DESCRIPTION</span></span>
<span data-ttu-id="3eccf-109">Kikapcsolja a felhőszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="3eccf-109">Power off the cloud service.</span></span>
<span data-ttu-id="3eccf-110">Felhívjuk a figyelmét arra, hogy az erőforrások továbbra is csatolva vannak, és az erőforrásokért díjat számítunk fel.</span><span class="sxs-lookup"><span data-stu-id="3eccf-110">Note that resources are still attached and you are getting charged for the resources.</span></span>

## <span data-ttu-id="3eccf-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3eccf-111">EXAMPLES</span></span>

### <span data-ttu-id="3eccf-112">1. példa: A felhőszolgáltatás leállítása</span><span class="sxs-lookup"><span data-stu-id="3eccf-112">Example 1: Stop cloud service</span></span>
```powershell
PS C:\> Stop-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"
```

<span data-ttu-id="3eccf-113">Ez a parancs leállítja a ContosoCS nevű felhőszolgáltatáshoz tartozó összes szerepkörpéldányt.</span><span class="sxs-lookup"><span data-stu-id="3eccf-113">This command stops all the role instances that belong to the the cloud service named ContosoCS.</span></span>

## <span data-ttu-id="3eccf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3eccf-114">PARAMETERS</span></span>

### <span data-ttu-id="3eccf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3eccf-115">-AsJob</span></span>
<span data-ttu-id="3eccf-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="3eccf-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3eccf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eccf-117">-DefaultProfile</span></span>
<span data-ttu-id="3eccf-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3eccf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3eccf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3eccf-119">-InputObject</span></span>
<span data-ttu-id="3eccf-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="3eccf-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: PowerOffViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3eccf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3eccf-121">-Name</span></span>
<span data-ttu-id="3eccf-122">A felhőszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="3eccf-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eccf-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3eccf-123">-NoWait</span></span>
<span data-ttu-id="3eccf-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="3eccf-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3eccf-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3eccf-125">-PassThru</span></span>
<span data-ttu-id="3eccf-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="3eccf-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3eccf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eccf-127">-ResourceGroupName</span></span>
<span data-ttu-id="3eccf-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3eccf-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eccf-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3eccf-129">-SubscriptionId</span></span>
<span data-ttu-id="3eccf-130">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="3eccf-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3eccf-131">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="3eccf-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eccf-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3eccf-132">-Confirm</span></span>
<span data-ttu-id="3eccf-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3eccf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eccf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eccf-134">-WhatIf</span></span>
<span data-ttu-id="3eccf-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3eccf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3eccf-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3eccf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eccf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eccf-137">CommonParameters</span></span>
<span data-ttu-id="3eccf-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eccf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eccf-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3eccf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eccf-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3eccf-140">INPUTS</span></span>

### <span data-ttu-id="3eccf-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="3eccf-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="3eccf-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3eccf-142">OUTPUTS</span></span>

### <span data-ttu-id="3eccf-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3eccf-143">System.Boolean</span></span>

## <span data-ttu-id="3eccf-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3eccf-144">NOTES</span></span>

<span data-ttu-id="3eccf-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3eccf-145">ALIASES</span></span>

<span data-ttu-id="3eccf-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="3eccf-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3eccf-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="3eccf-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3eccf-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3eccf-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3eccf-149">INPUTOBJECT: <ICloudServiceIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="3eccf-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3eccf-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="3eccf-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="3eccf-151">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="3eccf-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3eccf-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="3eccf-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="3eccf-153">`[RoleInstanceName <String>]`: A szerepkörpéldány neve.</span><span class="sxs-lookup"><span data-stu-id="3eccf-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="3eccf-154">`[RoleName <String>]`: A szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="3eccf-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="3eccf-155">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="3eccf-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3eccf-156">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="3eccf-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3eccf-157">`[UpdateDomain <Int32?>]`: A frissítő tartományt azonosító egész értéket ad meg.</span><span class="sxs-lookup"><span data-stu-id="3eccf-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="3eccf-158">A frissítési tartományokat nulla alapú index azonosítja: az első frissítési tartomány azonosítója 0, a második 1 és így tovább.</span><span class="sxs-lookup"><span data-stu-id="3eccf-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="3eccf-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3eccf-159">RELATED LINKS</span></span>

