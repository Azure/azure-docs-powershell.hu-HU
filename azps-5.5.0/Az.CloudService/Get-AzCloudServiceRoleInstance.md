---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 55416adbd2ffbcb816e5652ad33e1777594fdcb6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149034"
---
# <span data-ttu-id="b9ad1-101">Get-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="b9ad1-101">Get-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="b9ad1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9ad1-102">SYNOPSIS</span></span>
<span data-ttu-id="b9ad1-103">Szerepkörpéldányt kap egy felhőszolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="b9ad1-103">Gets a role instance from a cloud service.</span></span>

## <span data-ttu-id="b9ad1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b9ad1-104">SYNTAX</span></span>

### <span data-ttu-id="b9ad1-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9ad1-105">List (Default)</span></span>
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b9ad1-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="b9ad1-106">Get</span></span>
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b9ad1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b9ad1-107">GetViaIdentity</span></span>
```
Get-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b9ad1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b9ad1-108">DESCRIPTION</span></span>
<span data-ttu-id="b9ad1-109">Szerepkörpéldányt kap egy felhőszolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="b9ad1-109">Gets a role instance from a cloud service.</span></span>

## <span data-ttu-id="b9ad1-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b9ad1-110">EXAMPLES</span></span>

### <span data-ttu-id="b9ad1-111">1. példa: Az összes szerepkörpéldány lekérte</span><span class="sxs-lookup"><span data-stu-id="b9ad1-111">Example 1: Get all role instances</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard
ContosoFrontEnd_IN_1    eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard

```

<span data-ttu-id="b9ad1-112">Ez a parancs a ContosoCS nevű felhőszolgáltatás összes olyan szerepkörpéldányának tulajdonságait beszerzi, amely a ContosOrg nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="b9ad1-112">This command gets the properties of all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="b9ad1-113">2. példa: Az egy szerepkörpéldány tulajdonságainak lekérte</span><span class="sxs-lookup"><span data-stu-id="b9ad1-113">Example 2: Get properties for single role instance</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard

```

<span data-ttu-id="b9ad1-114">Ez a parancs a ContosOrg nevű erőforráscsoporthoz tartozó ContosoFrontEnd_IN_0 nevű felhőszolgáltatás szerepkörpéldányának tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b9ad1-114">This command gets the properties of the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="b9ad1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9ad1-115">PARAMETERS</span></span>

### <span data-ttu-id="b9ad1-116">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="b9ad1-116">-CloudServiceName</span></span>
<span data-ttu-id="b9ad1-117">.</span><span class="sxs-lookup"><span data-stu-id="b9ad1-117">.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ad1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9ad1-118">-DefaultProfile</span></span>
<span data-ttu-id="b9ad1-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9ad1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9ad1-120">-Kibontás</span><span class="sxs-lookup"><span data-stu-id="b9ad1-120">-Expand</span></span>
<span data-ttu-id="b9ad1-121">A műveletre alkalmazandó kibontó kifejezés.</span><span class="sxs-lookup"><span data-stu-id="b9ad1-121">The expand expression to apply to the operation.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Support.InstanceViewTypes
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ad1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9ad1-122">-InputObject</span></span>
<span data-ttu-id="b9ad1-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b9ad1-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9ad1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9ad1-124">-ResourceGroupName</span></span>
<span data-ttu-id="b9ad1-125">.</span><span class="sxs-lookup"><span data-stu-id="b9ad1-125">.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ad1-126">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="b9ad1-126">-RoleInstanceName</span></span>
<span data-ttu-id="b9ad1-127">A szerepkörpéldány neve.</span><span class="sxs-lookup"><span data-stu-id="b9ad1-127">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ad1-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b9ad1-128">-SubscriptionId</span></span>
<span data-ttu-id="b9ad1-129">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="b9ad1-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b9ad1-130">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b9ad1-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ad1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9ad1-131">CommonParameters</span></span>
<span data-ttu-id="b9ad1-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9ad1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9ad1-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9ad1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9ad1-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9ad1-134">INPUTS</span></span>

### <span data-ttu-id="b9ad1-135">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="b9ad1-135">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="b9ad1-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9ad1-136">OUTPUTS</span></span>

### <span data-ttu-id="b9ad1-137">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstance</span><span class="sxs-lookup"><span data-stu-id="b9ad1-137">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstance</span></span>

## <span data-ttu-id="b9ad1-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b9ad1-138">NOTES</span></span>

<span data-ttu-id="b9ad1-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b9ad1-139">ALIASES</span></span>

<span data-ttu-id="b9ad1-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="b9ad1-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b9ad1-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="b9ad1-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b9ad1-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b9ad1-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b9ad1-143">INPUTOBJECT: <ICloudServiceIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="b9ad1-143">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b9ad1-144">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="b9ad1-144">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="b9ad1-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="b9ad1-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b9ad1-146">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="b9ad1-146">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="b9ad1-147">`[RoleInstanceName <String>]`: A szerepkörpéldány neve.</span><span class="sxs-lookup"><span data-stu-id="b9ad1-147">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="b9ad1-148">`[RoleName <String>]`: A szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="b9ad1-148">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="b9ad1-149">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="b9ad1-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b9ad1-150">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b9ad1-150">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b9ad1-151">`[UpdateDomain <Int32?>]`: A frissítő tartományt azonosító egész számértéket ad meg.</span><span class="sxs-lookup"><span data-stu-id="b9ad1-151">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="b9ad1-152">A frissítési tartományokat nulla alapú index azonosítja: az első frissítési tartomány azonosítója 0, a második 1 és így tovább.</span><span class="sxs-lookup"><span data-stu-id="b9ad1-152">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="b9ad1-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9ad1-153">RELATED LINKS</span></span>

