---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudService.md
ms.openlocfilehash: 31683a7f8d0bea3a2e21588b0451275c74d52e97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012709"
---
# <span data-ttu-id="da440-101">Get-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="da440-101">Get-AzCloudService</span></span>

## <span data-ttu-id="da440-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da440-102">SYNOPSIS</span></span>
<span data-ttu-id="da440-103">Adatok megjelenítése a felhőszolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="da440-103">Display information about a cloud service.</span></span>

## <span data-ttu-id="da440-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="da440-104">SYNTAX</span></span>

### <span data-ttu-id="da440-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="da440-105">List (Default)</span></span>
```
Get-AzCloudService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="da440-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="da440-106">Get</span></span>
```
Get-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="da440-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="da440-107">GetViaIdentity</span></span>
```
Get-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="da440-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="da440-108">List1</span></span>
```
Get-AzCloudService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="da440-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="da440-109">DESCRIPTION</span></span>
<span data-ttu-id="da440-110">Adatok megjelenítése a felhőszolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="da440-110">Display information about a cloud service.</span></span>

## <span data-ttu-id="da440-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="da440-111">EXAMPLES</span></span>

### <span data-ttu-id="da440-112">1. példa: Az összes felhőszolgáltatás lekérte egy erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="da440-112">Example 1: Get all cloud service under a resource group</span></span>
```powershell
PS C:\> Get-AzCloudService -ResourceGroupName "ContosOrg"

ResourceGroupName Name              Location    ProvisioningState
----------------- ----              --------    -----------------
ContosOrg         ContosoCS         eastus2euap Succeeded
ContosOrg         ContosoCSTest     eastus2euap Failed
```

<span data-ttu-id="da440-113">Ez a parancs a ContosOrg nevű erőforráscsoport összes felhőszolgáltatását lekérte</span><span class="sxs-lookup"><span data-stu-id="da440-113">This command gets all cloud services in resource group named ContosOrg</span></span>

### <span data-ttu-id="da440-114">2. példa: Felhőszolgáltatás lekérte</span><span class="sxs-lookup"><span data-stu-id="da440-114">Example 2: Get cloud service</span></span>
```powershell
PS C:\> Get-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

ResourceGroupName Name              Location    ProvisioningState
----------------- ----              --------    -----------------
ContosOrg         ContosoCS         eastus2euap Succeeded

PS C:\> $cloudService = Get-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"
PS C:\> $cloudService | Format-List
ResourceGroupName : ContosOrg
Configuration     : xxxxxxxx
ConfigurationUrl  :
ExtensionProfile  : xxxxxxxx
Id                : xxxxxxxx
Location          : East US
Name              : ContosoCS
NetworkProfile    : xxxxxxxx
OSProfile         : xxxxxxxx
PackageUrl        : xxxxxxxx
ProvisioningState : Succeeded
RoleProfile       : xxxxxxxx
StartCloudService :
Tag               : {
                      "Owner": "Contos"
                    }
Type              : Microsoft.Compute/cloudServices
UniqueId          : xxxxxxxx
UpgradeMode       : Auto

```

<span data-ttu-id="da440-115">Ez a parancs a ContosoCS nevű felhőszolgáltatást kapja meg, amely a ContosOrg nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="da440-115">This command gets cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="da440-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da440-116">PARAMETERS</span></span>

### <span data-ttu-id="da440-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da440-117">-DefaultProfile</span></span>
<span data-ttu-id="da440-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da440-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da440-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da440-119">-InputObject</span></span>
<span data-ttu-id="da440-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="da440-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="da440-121">-Name</span><span class="sxs-lookup"><span data-stu-id="da440-121">-Name</span></span>
<span data-ttu-id="da440-122">A felhőszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="da440-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da440-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da440-123">-ResourceGroupName</span></span>
<span data-ttu-id="da440-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="da440-124">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da440-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da440-125">-SubscriptionId</span></span>
<span data-ttu-id="da440-126">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="da440-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="da440-127">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="da440-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da440-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da440-128">CommonParameters</span></span>
<span data-ttu-id="da440-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da440-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da440-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da440-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da440-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da440-131">INPUTS</span></span>

### <span data-ttu-id="da440-132">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="da440-132">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="da440-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da440-133">OUTPUTS</span></span>

### <span data-ttu-id="da440-134">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="da440-134">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="da440-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="da440-135">NOTES</span></span>

<span data-ttu-id="da440-136">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="da440-136">ALIASES</span></span>

<span data-ttu-id="da440-137">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="da440-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="da440-138">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="da440-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="da440-139">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="da440-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="da440-140">INPUTOBJECT: <ICloudServiceIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="da440-140">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="da440-141">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="da440-141">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="da440-142">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="da440-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="da440-143">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="da440-143">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="da440-144">`[RoleInstanceName <String>]`: A szerepkörpéldány neve.</span><span class="sxs-lookup"><span data-stu-id="da440-144">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="da440-145">`[RoleName <String>]`: A szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="da440-145">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="da440-146">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="da440-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="da440-147">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="da440-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="da440-148">`[UpdateDomain <Int32?>]`: A frissítő tartományt azonosító egész értéket ad meg.</span><span class="sxs-lookup"><span data-stu-id="da440-148">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="da440-149">A frissítési tartományokat nulla alapú index azonosítja: az első frissítési tartomány azonosítója 0, a második 1 és így tovább.</span><span class="sxs-lookup"><span data-stu-id="da440-149">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="da440-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da440-150">RELATED LINKS</span></span>

