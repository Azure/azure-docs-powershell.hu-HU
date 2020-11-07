---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdenyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
ms.openlocfilehash: 745df057c7c111bdca7cc30ac0864e15905ffd6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838180"
---
# <span data-ttu-id="8aa33-101">Get-AzDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="8aa33-101">Get-AzDenyAssignment</span></span>

## <span data-ttu-id="8aa33-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8aa33-102">SYNOPSIS</span></span>
<span data-ttu-id="8aa33-103">Felsorolja az Azure RBAC a feladatok elutasítását a megadott hatókörben.</span><span class="sxs-lookup"><span data-stu-id="8aa33-103">Lists Azure RBAC deny assignments at the specified scope.</span></span>
<span data-ttu-id="8aa33-104">Alapértelmezés szerint a kijelölt Azure-előfizetésben a megtagadási feladatokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="8aa33-104">By default it lists all deny assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="8aa33-105">A megfelelő paraméterekkel felsorolhatja az adott felhasználóhoz tartozó hozzárendeléseket, illetve megtagadhatja a feladatok megtagadását egy adott erőforráscsoport vagy erőforrás esetében.</span><span class="sxs-lookup"><span data-stu-id="8aa33-105">Use respective parameters to list deny assignments to a specific user, or to list deny assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="8aa33-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8aa33-106">SYNTAX</span></span>

### <span data-ttu-id="8aa33-107">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8aa33-107">EmptyParameterSet (Default)</span></span>
```
Get-AzDenyAssignment [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aa33-108">DenyAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8aa33-108">DenyAssignmentIdParameterSet</span></span>
```
Get-AzDenyAssignment -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aa33-109">DenyAssignmentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8aa33-109">DenyAssignmentNameParameterSet</span></span>
```
Get-AzDenyAssignment -DenyAssignmentName <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aa33-110">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8aa33-110">ObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aa33-111">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8aa33-111">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aa33-112">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8aa33-112">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aa33-113">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8aa33-113">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aa33-114">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8aa33-114">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aa33-115">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8aa33-115">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aa33-116">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8aa33-116">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aa33-117">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8aa33-117">SignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aa33-118">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="8aa33-118">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aa33-119">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="8aa33-119">ResourceWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aa33-120">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="8aa33-120">ScopeWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aa33-121">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="8aa33-121">SPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aa33-122">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="8aa33-122">ResourceGroupParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aa33-123">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="8aa33-123">ResourceParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aa33-124">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="8aa33-124">ScopeParameterSet</span></span>
```
Get-AzDenyAssignment -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8aa33-125">Leírás</span><span class="sxs-lookup"><span data-stu-id="8aa33-125">DESCRIPTION</span></span>
<span data-ttu-id="8aa33-126">A Get-AzDenyAssignment parancs segítségével felsorolhatja az összes olyan megtagadási feladatot, amely egy hatókörre érvényes.</span><span class="sxs-lookup"><span data-stu-id="8aa33-126">Use the Get-AzDenyAssignment command to list all deny assignments that are effective on a scope.</span></span>
<span data-ttu-id="8aa33-127">Paraméterek nélkül a parancs visszaküldi az előfizetéshez tartozó összes megtagadási feladatot.</span><span class="sxs-lookup"><span data-stu-id="8aa33-127">Without any parameters, this command returns all the deny assignments made under the subscription.</span></span>
<span data-ttu-id="8aa33-128">Ezt a listát szűrési paraméterekkel lehet szűrni a megbízó, a hozzárendelés-név és a hatókör letiltásával.</span><span class="sxs-lookup"><span data-stu-id="8aa33-128">This list can  be filtered using filtering parameters for principal, deny assignment name and scope.</span></span>
<span data-ttu-id="8aa33-129">A felhasználók megadásához használja a SignInName vagy az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="8aa33-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="8aa33-130">Ha meg szeretne adni egy biztonsági csoportot, használja az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="8aa33-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="8aa33-131">Az Azure AD-alkalmazások megadásához használja a ServicePrincipalName vagy a ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="8aa33-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="8aa33-132">A hozzáférés megtagadásának hatóköre lehet megadható.</span><span class="sxs-lookup"><span data-stu-id="8aa33-132">The scope at which access is being denied may be specified.</span></span>
<span data-ttu-id="8aa33-133">Az alapértelmezett érték a kijelölt előfizetéshez tartozik.</span><span class="sxs-lookup"><span data-stu-id="8aa33-133">It defaults to the selected subscription.</span></span>
<span data-ttu-id="8aa33-134">A megtagadási feladat hatóköre az a következő paraméter-kombinációk egyikével határozható meg.</span><span class="sxs-lookup"><span data-stu-id="8aa33-134">The scope of the deny assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="8aa33-135">Hatókör – ez a teljes mértékben minősített hatókör a/Subscriptions/subscriptionId kezdődően \< \> .</span><span class="sxs-lookup"><span data-stu-id="8aa33-135">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="8aa33-136">Ezzel a szűréssel megtagadhatja az adott hatókörben érvényben lévő feladatokat, azaz a fenti hatókörben és a fentiekben ismertetett összes elutasítási feladatot.</span><span class="sxs-lookup"><span data-stu-id="8aa33-136">This will filter deny assignments that are effective at that particular scope i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="8aa33-137">b.</span><span class="sxs-lookup"><span data-stu-id="8aa33-137">b.</span></span>
<span data-ttu-id="8aa33-138">ResourceGroupName – bármely erőforráscsoport neve az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="8aa33-138">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="8aa33-139">Ez a funkció a megadott erőforráscsoport esetén érvényes, azaz az adott hatókörben és fölötte lévő összes elutasítási feladatot szűri.</span><span class="sxs-lookup"><span data-stu-id="8aa33-139">This will filter assignments effective at the specified resource group i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="8aa33-140">c.</span><span class="sxs-lookup"><span data-stu-id="8aa33-140">c.</span></span>
<span data-ttu-id="8aa33-141">ResourceName, ResourceType, ResourceGroupName és (opcionálisan) ParentResource – egy adott erőforrást az előfizetése alatt azonosít, és a hozzárendelések megtagadását az adott erőforrás-tartományra érvényesen fogja szűrni.</span><span class="sxs-lookup"><span data-stu-id="8aa33-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter deny assignments effective at that resource scope.</span></span>
<span data-ttu-id="8aa33-142">Ha meg szeretné állapítani, hogy milyen hozzáférés van megtagadva egy adott felhasználónak az előfizetésben, használja a ExpandPrincipalGroups kapcsolót.</span><span class="sxs-lookup"><span data-stu-id="8aa33-142">To determine what access is denied for a particular user in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="8aa33-143">Ez felsorolja a felhasználóhoz rendelt minden elutasítási feladatot, valamint azokat a csoportokat, amelyeknek a felhasználó a tagja.</span><span class="sxs-lookup"><span data-stu-id="8aa33-143">This will list all deny assignments assigned to the user, and to the groups that the user is member of.</span></span>

## <span data-ttu-id="8aa33-144">Példák</span><span class="sxs-lookup"><span data-stu-id="8aa33-144">EXAMPLES</span></span>

### <span data-ttu-id="8aa33-145">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8aa33-145">Example 1</span></span>

<span data-ttu-id="8aa33-146">Az előfizetés összes megtagadási hozzárendelésének listázása</span><span class="sxs-lookup"><span data-stu-id="8aa33-146">List all deny assignments in the subscription</span></span>

```
PS C:\> Get-AzDenyAssignment
Id                      : 22704996-fbd0-4ab1-8625-722d897825d2
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  All Principals
                          ObjectType:   SystemDefined
                          ObjectId:     00000000-0000-0000-0000-000000000000
                          }
ExcludePrincipals       : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
IsSystemProtected       : True

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  PowershellTestingApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="8aa33-147">2. példa</span><span class="sxs-lookup"><span data-stu-id="8aa33-147">Example 2</span></span>

<span data-ttu-id="8aa33-148">A felhasználó megtagadja a felhasználónál john.doe@contoso.com a hatókör testRG és a fölötti feladatot.</span><span class="sxs-lookup"><span data-stu-id="8aa33-148">Gets all deny assignments made to user john.doe@contoso.com at the scope testRG and above.</span></span>

```
PS C:\> Get-AzDenyAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com

Id                      : 22704996-fbd0-4ab1-8625-722d897825d2
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  john.doe
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  john.doe
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  PowershellTestingApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="8aa33-149">3. példa</span><span class="sxs-lookup"><span data-stu-id="8aa33-149">Example 3</span></span>

<span data-ttu-id="8aa33-150">A megadott szolgáltatási megbízó minden elutasítási feladatát kapja</span><span class="sxs-lookup"><span data-stu-id="8aa33-150">Gets all deny assignments of the specified service principal</span></span>

```
PS C:\> Get-AzDenyAssignment -ServicePrincipalName 'http://testapp1.com'

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 94e3d9da-3700-4113-aab4-15f6c173d794
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/testRG/providers/Microsoft.Web/sites/site1
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="8aa33-151">4. példa</span><span class="sxs-lookup"><span data-stu-id="8aa33-151">Example 4</span></span>

<span data-ttu-id="8aa33-152">Megtagadja a feladatok elutasítását a "hely1" webhely hatókörében.</span><span class="sxs-lookup"><span data-stu-id="8aa33-152">Gets deny assignments at the 'site1' website scope.</span></span>

```
PS C:\> Get-AzDenyAssignment -Scope '/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/testRG/providers/Microsoft.Web/sites/site1'

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 94e3d9da-3700-4113-aab4-15f6c173d794
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/testRG/providers/Microsoft.Web/sites/site1
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

```

## <span data-ttu-id="8aa33-153">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8aa33-153">PARAMETERS</span></span>

### <span data-ttu-id="8aa33-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aa33-154">-DefaultProfile</span></span>
<span data-ttu-id="8aa33-155">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8aa33-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aa33-156">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="8aa33-156">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="8aa33-157">Ha meg van adva, akkor a felhasználó és a felhasználó tagjai (tranzitívan) által közvetlenül hozzárendelt visszautasítási hozzárendeléseket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8aa33-157">If specified, returns deny assignments directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="8aa33-158">Csak a felhasználói résztvevők számára támogatott.</span><span class="sxs-lookup"><span data-stu-id="8aa33-158">Supported only for a user principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ObjectIdParameterSet, SignInNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aa33-159">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8aa33-159">-ObjectId</span></span>
<span data-ttu-id="8aa33-160">Az Azure AD ObjectId a felhasználó, a csoport vagy a szolgáltatás megbízójának</span><span class="sxs-lookup"><span data-stu-id="8aa33-160">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="8aa33-161">Szűri az összes megtagadási feladatot a megadott megbízónál.</span><span class="sxs-lookup"><span data-stu-id="8aa33-161">Filters all deny assignments that are made to the specified principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aa33-162">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="8aa33-162">-ParentResource</span></span>
<span data-ttu-id="8aa33-163">A szülő erőforrás az erőforrás hierarchiájában a ResourceName paraméterrel megadva.</span><span class="sxs-lookup"><span data-stu-id="8aa33-163">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="8aa33-164">A ResourceGroupName, az ResourceType és a ResourceName paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="8aa33-164">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aa33-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aa33-165">-ResourceGroupName</span></span>
<span data-ttu-id="8aa33-166">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="8aa33-166">The resource group name.</span></span>
<span data-ttu-id="8aa33-167">A megadott erőforráscsoport által ténylegesen érvényben lévő hozzárendelések megtagadását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8aa33-167">Lists deny assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="8aa33-168">Ha a ResourceName, az ResourceType és a ParentResource paraméterekkel együtt használja, a parancs az erőforrás csoport erőforrásain érvényes erőforrás-hozzárendelések megtagadását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8aa33-168">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists deny assignments effective at resources within the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aa33-169">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8aa33-169">-ResourceName</span></span>
<span data-ttu-id="8aa33-170">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="8aa33-170">The resource name.</span></span>
<span data-ttu-id="8aa33-171">Például storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="8aa33-171">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="8aa33-172">A ResourceGroupName, ResourceType és (opcionálisan) ParentResource paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="8aa33-172">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aa33-173">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8aa33-173">-ResourceType</span></span>
<span data-ttu-id="8aa33-174">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="8aa33-174">The resource type.</span></span>
<span data-ttu-id="8aa33-175">Például Microsoft. hálózat/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="8aa33-175">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="8aa33-176">A ResourceGroupName, ResourceName és (opcionálisan) ParentResource paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="8aa33-176">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aa33-177">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="8aa33-177">-Scope</span></span>
<span data-ttu-id="8aa33-178">A szerepkör-hozzárendelés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="8aa33-178">The Scope of the role assignment.</span></span>
<span data-ttu-id="8aa33-179">A relatív URI formátuma.</span><span class="sxs-lookup"><span data-stu-id="8aa33-179">In the format of relative URI.</span></span>
<span data-ttu-id="8aa33-180">Például/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="8aa33-180">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="8aa33-181">A "/Subscriptions/{id}" szöveggel kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="8aa33-181">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="8aa33-182">A parancs szűri az összes olyan feladatot, amely az adott hatókörben érvényes.</span><span class="sxs-lookup"><span data-stu-id="8aa33-182">The command filters all deny assignments that are effective at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet, ScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aa33-183">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8aa33-183">-ServicePrincipalName</span></span>
<span data-ttu-id="8aa33-184">A ServicePrincipalName.</span><span class="sxs-lookup"><span data-stu-id="8aa33-184">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="8aa33-185">Szűri a megadott Azure AD-alkalmazáshoz tartozó összes megtagadási feladatot.</span><span class="sxs-lookup"><span data-stu-id="8aa33-185">Filters all deny assignments that are made to the specified Azure AD application.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aa33-186">-SignInName</span><span class="sxs-lookup"><span data-stu-id="8aa33-186">-SignInName</span></span>
<span data-ttu-id="8aa33-187">Az e-mail-cím vagy a felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="8aa33-187">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="8aa33-188">Szűri az összes, az adott felhasználóra vonatkozó megtagadási feladatot.</span><span class="sxs-lookup"><span data-stu-id="8aa33-188">Filters all deny assignments that are made to the specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aa33-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aa33-189">CommonParameters</span></span>
<span data-ttu-id="8aa33-190">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8aa33-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aa33-191">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8aa33-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aa33-192">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8aa33-192">INPUTS</span></span>

### <span data-ttu-id="8aa33-193">System. GUID</span><span class="sxs-lookup"><span data-stu-id="8aa33-193">System.Guid</span></span>

### <span data-ttu-id="8aa33-194">System. String</span><span class="sxs-lookup"><span data-stu-id="8aa33-194">System.String</span></span>

## <span data-ttu-id="8aa33-195">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8aa33-195">OUTPUTS</span></span>

### <span data-ttu-id="8aa33-196">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="8aa33-196">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span></span>

## <span data-ttu-id="8aa33-197">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8aa33-197">NOTES</span></span>
<span data-ttu-id="8aa33-198">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="8aa33-198">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>