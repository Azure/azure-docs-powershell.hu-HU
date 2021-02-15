---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/start-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Start-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Start-AzCloudService.md
ms.openlocfilehash: 2e2fe8534c1af369a8d095ba4ba3d74106700297
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166643"
---
# <span data-ttu-id="bdbe2-101">Start-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="bdbe2-101">Start-AzCloudService</span></span>

## <span data-ttu-id="bdbe2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdbe2-102">SYNOPSIS</span></span>
<span data-ttu-id="bdbe2-103">Elindítja a felhőszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="bdbe2-103">Starts the cloud service.</span></span>

## <span data-ttu-id="bdbe2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bdbe2-104">SYNTAX</span></span>

### <span data-ttu-id="bdbe2-105">Start (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bdbe2-105">Start (Default)</span></span>
```
Start-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bdbe2-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bdbe2-106">StartViaIdentity</span></span>
```
Start-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bdbe2-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bdbe2-107">DESCRIPTION</span></span>
<span data-ttu-id="bdbe2-108">Elindítja a felhőszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="bdbe2-108">Starts the cloud service.</span></span>

## <span data-ttu-id="bdbe2-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bdbe2-109">EXAMPLES</span></span>

### <span data-ttu-id="bdbe2-110">1. példa: Felhőszolgáltatás kezdése</span><span class="sxs-lookup"><span data-stu-id="bdbe2-110">Example 1: Start cloud service</span></span>
```powershell
PS C:\> Start-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"
```

<span data-ttu-id="bdbe2-111">Ez a parancs elindítja a ContosoCS nevű felhőszolgáltatáshoz tartozó összes szerepkörpéldányt.</span><span class="sxs-lookup"><span data-stu-id="bdbe2-111">This command starts all the role instances that belong to the the cloud service named ContosoCS.</span></span>

## <span data-ttu-id="bdbe2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdbe2-112">PARAMETERS</span></span>

### <span data-ttu-id="bdbe2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdbe2-113">-AsJob</span></span>
<span data-ttu-id="bdbe2-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="bdbe2-114">Run the command as a job</span></span>

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

### <span data-ttu-id="bdbe2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdbe2-115">-DefaultProfile</span></span>
<span data-ttu-id="bdbe2-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bdbe2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdbe2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdbe2-117">-InputObject</span></span>
<span data-ttu-id="bdbe2-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="bdbe2-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdbe2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bdbe2-119">-Name</span></span>
<span data-ttu-id="bdbe2-120">A felhőszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="bdbe2-120">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbe2-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bdbe2-121">-NoWait</span></span>
<span data-ttu-id="bdbe2-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="bdbe2-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bdbe2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bdbe2-123">-PassThru</span></span>
<span data-ttu-id="bdbe2-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="bdbe2-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bdbe2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdbe2-125">-ResourceGroupName</span></span>
<span data-ttu-id="bdbe2-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bdbe2-126">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbe2-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bdbe2-127">-SubscriptionId</span></span>
<span data-ttu-id="bdbe2-128">Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="bdbe2-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bdbe2-129">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="bdbe2-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbe2-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bdbe2-130">-Confirm</span></span>
<span data-ttu-id="bdbe2-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bdbe2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdbe2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdbe2-132">-WhatIf</span></span>
<span data-ttu-id="bdbe2-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bdbe2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdbe2-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bdbe2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdbe2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdbe2-135">CommonParameters</span></span>
<span data-ttu-id="bdbe2-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdbe2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdbe2-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bdbe2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdbe2-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bdbe2-138">INPUTS</span></span>

### <span data-ttu-id="bdbe2-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="bdbe2-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="bdbe2-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdbe2-140">OUTPUTS</span></span>

### <span data-ttu-id="bdbe2-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bdbe2-141">System.Boolean</span></span>

## <span data-ttu-id="bdbe2-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bdbe2-142">NOTES</span></span>

<span data-ttu-id="bdbe2-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="bdbe2-143">ALIASES</span></span>

<span data-ttu-id="bdbe2-144">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="bdbe2-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bdbe2-145">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="bdbe2-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bdbe2-146">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bdbe2-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bdbe2-147">INPUTOBJECT: <ICloudServiceIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="bdbe2-147">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bdbe2-148">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="bdbe2-148">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="bdbe2-149">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="bdbe2-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bdbe2-150">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="bdbe2-150">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="bdbe2-151">`[RoleInstanceName <String>]`: A szerepkörpéldány neve.</span><span class="sxs-lookup"><span data-stu-id="bdbe2-151">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="bdbe2-152">`[RoleName <String>]`: A szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="bdbe2-152">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="bdbe2-153">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="bdbe2-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="bdbe2-154">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="bdbe2-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="bdbe2-155">`[UpdateDomain <Int32?>]`: A frissítő tartományt azonosító egész számértéket ad meg.</span><span class="sxs-lookup"><span data-stu-id="bdbe2-155">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="bdbe2-156">A frissítési tartományokat nulla alapú index azonosítja: az első frissítési tartomány azonosítója 0, a második 1 és így tovább.</span><span class="sxs-lookup"><span data-stu-id="bdbe2-156">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="bdbe2-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bdbe2-157">RELATED LINKS</span></span>

