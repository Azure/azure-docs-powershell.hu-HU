---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: cd4cb9f7137d0e6cdd91222c278b6e59c04d7e3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667649"
---
# <span data-ttu-id="0cdd5-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="0cdd5-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="0cdd5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0cdd5-102">SYNOPSIS</span></span>
<span data-ttu-id="0cdd5-103">Szerezzen be egy vagy több tervrajz meghatározását.</span><span class="sxs-lookup"><span data-stu-id="0cdd5-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="0cdd5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0cdd5-104">SYNTAX</span></span>

### <span data-ttu-id="0cdd5-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0cdd5-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cdd5-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="0cdd5-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0cdd5-107">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="0cdd5-107">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cdd5-108">BySubscriptionNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="0cdd5-108">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cdd5-109">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="0cdd5-109">ManagementGroupScope</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cdd5-110">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="0cdd5-110">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0cdd5-111">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="0cdd5-111">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cdd5-112">ByManagementGroupNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="0cdd5-112">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cdd5-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="0cdd5-113">DESCRIPTION</span></span>
<span data-ttu-id="0cdd5-114">Szerezzen be egy vagy több tervrajz meghatározását.</span><span class="sxs-lookup"><span data-stu-id="0cdd5-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="0cdd5-115">A terv definíciói a kezelési csoportban vagy az előfizetési tartományban találhatók.</span><span class="sxs-lookup"><span data-stu-id="0cdd5-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="0cdd5-116">Példák</span><span class="sxs-lookup"><span data-stu-id="0cdd5-116">EXAMPLES</span></span>

### <span data-ttu-id="0cdd5-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0cdd5-117">Example 1</span></span>
```powershell
PS> Get-AzBlueprint

Name                 : PS-BlueprintDefinition
Id                   : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprints/PS-BlueprintDefinition
SubscriptionId       : 00000000-1111-0000-1111-000000000000
Versions             : {1.0}
Description          : Powershell test blueprint
TimeCreated          : 2019-02-01
TargetScope          : Subscription
Parameters           : {storageData_storageAccountType, storageData_location, allowedlocations_listOfAllowedLocations}
ResourceGroups       : ResourceGroup
```

<span data-ttu-id="0cdd5-118">A tervezet definíciójának beszerzése az aktuális előfizetésben és az előfizetés felügyeleti csoport hierarchiájában</span><span class="sxs-lookup"><span data-stu-id="0cdd5-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="0cdd5-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="0cdd5-119">Example 2</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId"

Name                 : PS-MG-BlueprintDefinition
Id                   : /providers/Microsoft.Management/managementGroups/myManagementGroupId/providers/Microsoft.Blueprint/blueprints/PS-MG-BlueprintDefinition
ManagementGroupId    : myManagementGroupId
Versions             : {1.0, 2.0, 3.0, 4.0}
TimeCreated          : 2019-03-04
TargetScope          : Subscription
Parameters           : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue, [Usergrouporapplicationname]:Contributor_RoleAssignmentName,
                       [Usergrouporapplicationname]:Owner_RoleAssignmentName}
ResourceGroups       : {ResourceGroup, ResourceGroup2}
```

<span data-ttu-id="0cdd5-120">A terv definíciójának beszerzése a megadott felügyeleti csoporton belül</span><span class="sxs-lookup"><span data-stu-id="0cdd5-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="0cdd5-121">3. példa</span><span class="sxs-lookup"><span data-stu-id="0cdd5-121">Example 3</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000"

Name                 : PS-BlueprintDefinition
Id                   : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprints/PS-BlueprintDefinition
SubscriptionId       : 00000000-1111-0000-1111-000000000000
Versions             : {1.0}
Description          : Powershell test blueprint
TimeCreated          : 2019-02-01
TargetScope          : Subscription
Parameters           : {storageData_storageAccountType, storageData_location, allowedlocations_listOfAllowedLocations}
ResourceGroups       : ResourceGroup
```

<span data-ttu-id="0cdd5-122">A tervezet definíciójának beszerzése a megadott előfizetés és az előfizetés felügyeleti csoport hierarchiája között</span><span class="sxs-lookup"><span data-stu-id="0cdd5-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="0cdd5-123">4. példa</span><span class="sxs-lookup"><span data-stu-id="0cdd5-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="0cdd5-124">A tervezet definíciójának beszerzése a megadott névvel a megadott előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="0cdd5-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="0cdd5-125">Példa 5</span><span class="sxs-lookup"><span data-stu-id="0cdd5-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="0cdd5-126">A terv definíciójának beszerzése a megadott felügyeleti csoportban megadott névvel és verzióval</span><span class="sxs-lookup"><span data-stu-id="0cdd5-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="0cdd5-127">6. példa</span><span class="sxs-lookup"><span data-stu-id="0cdd5-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="0cdd5-128">A legutóbbi közzétett terv definíciójának beszerzése a megadott felügyeleti csoporton belüli névvel</span><span class="sxs-lookup"><span data-stu-id="0cdd5-128">Get the latest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="0cdd5-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0cdd5-129">PARAMETERS</span></span>

### <span data-ttu-id="0cdd5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cdd5-130">-DefaultProfile</span></span>
<span data-ttu-id="0cdd5-131">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0cdd5-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cdd5-132">-LatestPublished</span><span class="sxs-lookup"><span data-stu-id="0cdd5-132">-LatestPublished</span></span>
<span data-ttu-id="0cdd5-133">A legújabb közzétett Blueprint definition definition Flag.</span><span class="sxs-lookup"><span data-stu-id="0cdd5-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="0cdd5-134">Ha be van állítva, akkor a végrehajtás a tervezet definíciójának legújabb verzióját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="0cdd5-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="0cdd5-135">Az alapértelmezett érték a false.</span><span class="sxs-lookup"><span data-stu-id="0cdd5-135">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySubscriptionNameAndLatestPublished, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cdd5-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="0cdd5-136">-ManagementGroupId</span></span>
<span data-ttu-id="0cdd5-137">Annak a kezelési csoportnak az azonosítója, amelybe a terv definícióját mentette.</span><span class="sxs-lookup"><span data-stu-id="0cdd5-137">Management Group Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope, ByManagementGroupAndName, ByManagementGroupNameAndVersion, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cdd5-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0cdd5-138">-Name</span></span>
<span data-ttu-id="0cdd5-139">Terv definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="0cdd5-139">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, BySubscriptionNameAndVersion, BySubscriptionNameAndLatestPublished, ByManagementGroupAndName, ByManagementGroupNameAndVersion, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cdd5-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0cdd5-140">-SubscriptionId</span></span>
<span data-ttu-id="0cdd5-141">Az előfizetési azonosító, amelyre a terv definíciója van mentve.</span><span class="sxs-lookup"><span data-stu-id="0cdd5-141">Subscription Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName, BySubscriptionNameAndVersion, BySubscriptionNameAndLatestPublished
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cdd5-142">-Verzió</span><span class="sxs-lookup"><span data-stu-id="0cdd5-142">-Version</span></span>
<span data-ttu-id="0cdd5-143">Közzétett terv definíciós verziója.</span><span class="sxs-lookup"><span data-stu-id="0cdd5-143">Published blueprint definition version.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionNameAndVersion, ByManagementGroupNameAndVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cdd5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cdd5-144">CommonParameters</span></span>
<span data-ttu-id="0cdd5-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0cdd5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cdd5-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cdd5-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cdd5-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cdd5-147">INPUTS</span></span>

### <span data-ttu-id="0cdd5-148">System. String</span><span class="sxs-lookup"><span data-stu-id="0cdd5-148">System.String</span></span>

## <span data-ttu-id="0cdd5-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cdd5-149">OUTPUTS</span></span>

### <span data-ttu-id="0cdd5-150">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="0cdd5-150">System.Object</span></span>
## <span data-ttu-id="0cdd5-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0cdd5-151">NOTES</span></span>

## <span data-ttu-id="0cdd5-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0cdd5-152">RELATED LINKS</span></span>
