---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: ab383b1fb46759c2369d94d4bb57284ba59cf671
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331421"
---
# <span data-ttu-id="1fceb-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="1fceb-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="1fceb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fceb-102">SYNOPSIS</span></span>
<span data-ttu-id="1fceb-103">Lekért egy vagy több tervrajzdefiníciót.</span><span class="sxs-lookup"><span data-stu-id="1fceb-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="1fceb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1fceb-104">SYNTAX</span></span>

### <span data-ttu-id="1fceb-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1fceb-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fceb-106">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="1fceb-106">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fceb-107">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="1fceb-107">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1fceb-108">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="1fceb-108">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1fceb-109">ByManagementGroupNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="1fceb-109">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fceb-110">BySubscriptionNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="1fceb-110">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fceb-111">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="1fceb-111">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fceb-112">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="1fceb-112">ManagementGroupScope</span></span>
```
Get-AzBlueprint -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fceb-113">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1fceb-113">DESCRIPTION</span></span>
<span data-ttu-id="1fceb-114">Lekért egy vagy több tervrajzdefiníciót.</span><span class="sxs-lookup"><span data-stu-id="1fceb-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="1fceb-115">A tervdefiníciók a felügyeleti csoport vagy az előfizetés hatókörében léteznek.</span><span class="sxs-lookup"><span data-stu-id="1fceb-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="1fceb-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1fceb-116">EXAMPLES</span></span>

### <span data-ttu-id="1fceb-117">1. példa</span><span class="sxs-lookup"><span data-stu-id="1fceb-117">Example 1</span></span>
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

<span data-ttu-id="1fceb-118">A tervdefiníciókat az aktuális előfizetésen belül, valamint az előfizetés felügyeleti csoporthierarchiájában is le kell szereznie.</span><span class="sxs-lookup"><span data-stu-id="1fceb-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="1fceb-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="1fceb-119">Example 2</span></span>
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

<span data-ttu-id="1fceb-120">A tervdefiníciók lekérte a megadott felügyeleti csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="1fceb-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="1fceb-121">3. példa</span><span class="sxs-lookup"><span data-stu-id="1fceb-121">Example 3</span></span>
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

<span data-ttu-id="1fceb-122">A tervdefiníciókat a megadott előfizetésen belül, valamint az előfizetés felügyeleti csoporthierarchiájában is le kell szereznie.</span><span class="sxs-lookup"><span data-stu-id="1fceb-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="1fceb-123">4. példa</span><span class="sxs-lookup"><span data-stu-id="1fceb-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="1fceb-124">Szerezze be a tervdefiníciót a megadott néven a megadott előfizetésen belül.</span><span class="sxs-lookup"><span data-stu-id="1fceb-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="1fceb-125">5. példa</span><span class="sxs-lookup"><span data-stu-id="1fceb-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="1fceb-126">Szerezze be a tervdefiníciót a megadott néven és verzióval a megadott felügyeleti csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="1fceb-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="1fceb-127">6. példa</span><span class="sxs-lookup"><span data-stu-id="1fceb-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="1fceb-128">Szerezze be a legutóbbi közzétett tervrajzdefiníciót a megadott néven a megadott felügyeleti csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="1fceb-128">Get the latest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="1fceb-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fceb-129">PARAMETERS</span></span>

### <span data-ttu-id="1fceb-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fceb-130">-DefaultProfile</span></span>
<span data-ttu-id="1fceb-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1fceb-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fceb-132">-LatestPublished</span><span class="sxs-lookup"><span data-stu-id="1fceb-132">-LatestPublished</span></span>
<span data-ttu-id="1fceb-133">A legutóbbi közzétett tervdefiníciós jelölő.</span><span class="sxs-lookup"><span data-stu-id="1fceb-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="1fceb-134">Ha be van állítva, a végrehajtás a tervrajzdefiníció legújabb közzétett verzióját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="1fceb-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="1fceb-135">Alapértelmezés szerint hamis.</span><span class="sxs-lookup"><span data-stu-id="1fceb-135">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByManagementGroupNameAndLatestPublished, BySubscriptionNameAndLatestPublished
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fceb-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="1fceb-136">-ManagementGroupId</span></span>
<span data-ttu-id="1fceb-137">Management Group Id where the blueprint definition is saved.</span><span class="sxs-lookup"><span data-stu-id="1fceb-137">Management Group Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, ByManagementGroupAndName, ByManagementGroupNameAndLatestPublished, ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fceb-138">-Name</span><span class="sxs-lookup"><span data-stu-id="1fceb-138">-Name</span></span>
<span data-ttu-id="1fceb-139">A tervrajz definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="1fceb-139">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, ByManagementGroupAndName, ByManagementGroupNameAndLatestPublished, BySubscriptionNameAndLatestPublished, BySubscriptionNameAndVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fceb-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1fceb-140">-SubscriptionId</span></span>
<span data-ttu-id="1fceb-141">Előfizetés azonosítója, ahová a tervrajz definíciója mentve van.</span><span class="sxs-lookup"><span data-stu-id="1fceb-141">Subscription Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName, BySubscriptionNameAndLatestPublished, BySubscriptionNameAndVersion
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fceb-142">-Version</span><span class="sxs-lookup"><span data-stu-id="1fceb-142">-Version</span></span>
<span data-ttu-id="1fceb-143">Közzétett tervdefiníciós verzió.</span><span class="sxs-lookup"><span data-stu-id="1fceb-143">Published blueprint definition version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, BySubscriptionNameAndVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fceb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fceb-144">CommonParameters</span></span>
<span data-ttu-id="1fceb-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fceb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fceb-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1fceb-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fceb-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1fceb-147">INPUTS</span></span>

### <span data-ttu-id="1fceb-148">System.String</span><span class="sxs-lookup"><span data-stu-id="1fceb-148">System.String</span></span>

## <span data-ttu-id="1fceb-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1fceb-149">OUTPUTS</span></span>

### <span data-ttu-id="1fceb-150">System.Object</span><span class="sxs-lookup"><span data-stu-id="1fceb-150">System.Object</span></span>
## <span data-ttu-id="1fceb-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1fceb-151">NOTES</span></span>

## <span data-ttu-id="1fceb-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1fceb-152">RELATED LINKS</span></span>
