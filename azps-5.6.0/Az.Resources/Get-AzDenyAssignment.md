---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdenyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
ms.openlocfilehash: d54d6ff9ed26b76d3c36ab47cf04024dcdf11281
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920938"
---
# <span data-ttu-id="2ee3c-101">Get-AzDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="2ee3c-101">Get-AzDenyAssignment</span></span>

## <span data-ttu-id="2ee3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ee3c-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee3c-103">Az Azure RBAC a megadott hatókörű hozzárendeléseket tiltja le.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-103">Lists Azure RBAC deny assignments at the specified scope.</span></span>
<span data-ttu-id="2ee3c-104">Alapértelmezés szerint a kijelölt Azure-előfizetés összes elutasító hozzárendelését felsorolja.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-104">By default it lists all deny assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="2ee3c-105">A megfelelő paramétereket használva listában elutasíthatja egy adott felhasználó hozzárendelését, vagy elutasíthatja egy adott erőforráscsoport vagy erőforrás hozzárendelését.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-105">Use respective parameters to list deny assignments to a specific user, or to list deny assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="2ee3c-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2ee3c-106">SYNTAX</span></span>

### <span data-ttu-id="2ee3c-107">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2ee3c-107">EmptyParameterSet (Default)</span></span>
```
Get-AzDenyAssignment [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ee3c-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ee3c-108">ObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ee3c-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ee3c-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ee3c-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ee3c-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ee3c-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ee3c-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ee3c-112">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ee3c-112">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ee3c-113">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ee3c-113">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ee3c-114">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ee3c-114">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ee3c-115">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ee3c-115">SignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ee3c-116">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ee3c-116">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ee3c-117">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ee3c-117">ResourceWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ee3c-118">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ee3c-118">ScopeWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ee3c-119">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ee3c-119">SPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ee3c-120">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ee3c-120">ResourceGroupParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ee3c-121">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ee3c-121">ResourceParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ee3c-122">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ee3c-122">ScopeParameterSet</span></span>
```
Get-AzDenyAssignment -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ee3c-123">DenyAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ee3c-123">DenyAssignmentIdParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -Id <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ee3c-124">DenyAssignmentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ee3c-124">DenyAssignmentNameParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -DenyAssignmentName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ee3c-125">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2ee3c-125">DESCRIPTION</span></span>
<span data-ttu-id="2ee3c-126">A Get-AzDenyAssignment paranccsal felsorolhatja az összes elutasító feladatot, amely egy hatókörben hatékony.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-126">Use the Get-AzDenyAssignment command to list all deny assignments that are effective on a scope.</span></span>
<span data-ttu-id="2ee3c-127">Paraméterek nélkül ez a parancs az előfizetéshez megadott összes elutasítási feladatot visszaadja.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-127">Without any parameters, this command returns all the deny assignments made under the subscription.</span></span>
<span data-ttu-id="2ee3c-128">Ez a lista szűrhető a fő feladat paramétereinek szűrésével, a feladat nevének és hatókörének elutasításával.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-128">This list can  be filtered using filtering parameters for principal, deny assignment name and scope.</span></span>
<span data-ttu-id="2ee3c-129">Felhasználó megadásához használja a SignInName vagy az Azure AD ObjectId paramétereit.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="2ee3c-130">Biztonsági csoport megadásához használja az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="2ee3c-131">Azure AD-alkalmazás megadásához használja a ServicePrincipalName vagy az ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="2ee3c-132">A hozzáférés megtagadható hatóköre megadva lehet.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-132">The scope at which access is being denied may be specified.</span></span>
<span data-ttu-id="2ee3c-133">Alapértelmezés szerint a kijelölt előfizetést használja.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-133">It defaults to the selected subscription.</span></span>
<span data-ttu-id="2ee3c-134">Az elutasítás hozzárendelésének hatóköre az alábbi A paraméterkombinációk egyikével létezik megadva.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-134">The scope of the deny assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="2ee3c-135">Hatókör – Ez a teljesen minősített hatókör az /subscriptions/ tartománytól \<subscriptionId\> kezdve.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-135">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="2ee3c-136">Ezzel szűri az adott hatókörben hatékony hozzárendeléseket, azaz az adott hatókörben és fölötte elutasított összes hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-136">This will filter deny assignments that are effective at that particular scope i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="2ee3c-137">b.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-137">b.</span></span>
<span data-ttu-id="2ee3c-138">ResourceGroupName – Az előfizetés alatt bármelyik erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-138">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="2ee3c-139">Ezzel szűri a hozzárendeléseket a megadott erőforráscsoportban, azaz az adott hatókörben és fölötte található összes hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-139">This will filter assignments effective at the specified resource group i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="2ee3c-140">c.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-140">c.</span></span>
<span data-ttu-id="2ee3c-141">ResourceName, ResourceType, ResourceGroupName és (nem kötelező) ParentResource – Azonosítja az előfizetés egy adott erőforrását, és szűri az elutasító hozzárendeléseket, amelyek az adott erőforrás hatókörében hatékonyak.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter deny assignments effective at that resource scope.</span></span>
<span data-ttu-id="2ee3c-142">Ha meg szeretné állapítani, hogy egy adott felhasználónál milyen hozzáférés van megtagadva az előfizetésben, használja az ExpandPrincipalGroups kapcsolót.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-142">To determine what access is denied for a particular user in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="2ee3c-143">Ezzel felsorolja a felhasználóhoz és a felhasználóhoz rendelt csoportokhoz rendelt összes hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-143">This will list all deny assignments assigned to the user, and to the groups that the user is member of.</span></span>

## <span data-ttu-id="2ee3c-144">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2ee3c-144">EXAMPLES</span></span>

### <span data-ttu-id="2ee3c-145">1. példa</span><span class="sxs-lookup"><span data-stu-id="2ee3c-145">Example 1</span></span>

<span data-ttu-id="2ee3c-146">Az előfizetés összes elutasító hozzárendelésének felsorolása</span><span class="sxs-lookup"><span data-stu-id="2ee3c-146">List all deny assignments in the subscription</span></span>

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

### <span data-ttu-id="2ee3c-147">2. példa</span><span class="sxs-lookup"><span data-stu-id="2ee3c-147">Example 2</span></span>

<span data-ttu-id="2ee3c-148">A testRG hatókörben és a fenti hatókörben a felhasználóknak adott összes john.doe@contoso.com elutasító hozzárendelést lejátssa.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-148">Gets all deny assignments made to user john.doe@contoso.com at the scope testRG and above.</span></span>

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

### <span data-ttu-id="2ee3c-149">3. példa</span><span class="sxs-lookup"><span data-stu-id="2ee3c-149">Example 3</span></span>

<span data-ttu-id="2ee3c-150">A megadott egyszerű szolgáltatásnév összes hozzárendelésének elutasítása</span><span class="sxs-lookup"><span data-stu-id="2ee3c-150">Gets all deny assignments of the specified service principal</span></span>

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

### <span data-ttu-id="2ee3c-151">4. példa</span><span class="sxs-lookup"><span data-stu-id="2ee3c-151">Example 4</span></span>

<span data-ttu-id="2ee3c-152">A "webhely1" webhely hatókörében megtagadja a feladatokat.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-152">Gets deny assignments at the 'site1' website scope.</span></span>

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

## <span data-ttu-id="2ee3c-153">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ee3c-153">PARAMETERS</span></span>

### <span data-ttu-id="2ee3c-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ee3c-154">-DefaultProfile</span></span>
<span data-ttu-id="2ee3c-155">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2ee3c-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ee3c-156">-DenyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="2ee3c-156">-DenyAssignmentName</span></span>
<span data-ttu-id="2ee3c-157">Az elutasító feladat neve.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-157">Name of the deny assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: DenyAssignmentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ee3c-158">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="2ee3c-158">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="2ee3c-159">Ha meg van adva, akkor visszaadja a felhasználóhoz közvetlenül hozzárendelt és a felhasználó tagjainak csoportjaihoz rendelt (átviteles) hozzárendeléseket.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-159">If specified, returns deny assignments directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="2ee3c-160">Csak egyszerű felhasználó esetén támogatott.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-160">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="2ee3c-161">-Id</span><span class="sxs-lookup"><span data-stu-id="2ee3c-161">-Id</span></span>
<span data-ttu-id="2ee3c-162">Feladatazonosító elutasítása.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-162">Deny assignment id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: DenyAssignmentIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ee3c-163">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2ee3c-163">-ObjectId</span></span>
<span data-ttu-id="2ee3c-164">A felhasználó, csoport vagy szolgáltatásnév Azure AD-objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-164">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="2ee3c-165">Minden olyan hozzárendelést szűr, amely a megadott egyszerű feladathoz van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-165">Filters all deny assignments that are made to the specified principal.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ee3c-166">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="2ee3c-166">-ParentResource</span></span>
<span data-ttu-id="2ee3c-167">A szülőerőforrás a ResourceName paraméterrel megadott erőforrás hierarchiában.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-167">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="2ee3c-168">A ResourceGroupName, az ResourceType és az ResourceName paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-168">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="2ee3c-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ee3c-169">-ResourceGroupName</span></span>
<span data-ttu-id="2ee3c-170">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-170">The resource group name.</span></span>
<span data-ttu-id="2ee3c-171">A listák elutasítják a megadott erőforráscsoportban hatályos hozzárendeléseket.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-171">Lists deny assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="2ee3c-172">Az Erőforrásnév, Az Erőforrás típusa és a ParentResource paraméterekkel együtt használva a parancslisták elutasítják a hozzárendeléseket az erőforráscsoport erőforrásainál.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-172">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists deny assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="2ee3c-173">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2ee3c-173">-ResourceName</span></span>
<span data-ttu-id="2ee3c-174">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-174">The resource name.</span></span>
<span data-ttu-id="2ee3c-175">Például: storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-175">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="2ee3c-176">Az ResourceGroupName, az ResourceType és (opcionális) ParentResource paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-176">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="2ee3c-177">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="2ee3c-177">-ResourceType</span></span>
<span data-ttu-id="2ee3c-178">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-178">The resource type.</span></span>
<span data-ttu-id="2ee3c-179">Például: Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-179">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="2ee3c-180">A ResourceGroupName, az ResourceName és a ParentResource paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-180">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="2ee3c-181">-Scope</span><span class="sxs-lookup"><span data-stu-id="2ee3c-181">-Scope</span></span>
<span data-ttu-id="2ee3c-182">A szerepkör-hozzárendelés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-182">The Scope of the role assignment.</span></span>
<span data-ttu-id="2ee3c-183">Relatív URI formátumban.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-183">In the format of relative URI.</span></span>
<span data-ttu-id="2ee3c-184">Például: /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-184">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="2ee3c-185">A műveletnek a következővel kell kezdődnie: "/subscriptions/{id}".</span><span class="sxs-lookup"><span data-stu-id="2ee3c-185">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="2ee3c-186">A parancs az összes olyan hozzárendelést szűri, amely az ilyen hatókörben hatékony.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-186">The command filters all deny assignments that are effective at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, DenyAssignmentIdParameterSet, DenyAssignmentNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="2ee3c-187">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="2ee3c-187">-ServicePrincipalName</span></span>
<span data-ttu-id="2ee3c-188">A szolgáltatásnév ServicePrincipalName tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-188">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="2ee3c-189">A megadott Azure AD-alkalmazáshoz adott hozzárendelések elutasítását szűri.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-189">Filters all deny assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="2ee3c-190">-SignInName</span><span class="sxs-lookup"><span data-stu-id="2ee3c-190">-SignInName</span></span>
<span data-ttu-id="2ee3c-191">A felhasználó e-mail-címe vagy egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-191">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="2ee3c-192">Minden olyan hozzárendelést elutasít, amely adott felhasználóhoz lett hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-192">Filters all deny assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="2ee3c-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee3c-193">CommonParameters</span></span>
<span data-ttu-id="2ee3c-194">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ee3c-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee3c-195">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ee3c-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee3c-196">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ee3c-196">INPUTS</span></span>

### <span data-ttu-id="2ee3c-197">System.Guid</span><span class="sxs-lookup"><span data-stu-id="2ee3c-197">System.Guid</span></span>

### <span data-ttu-id="2ee3c-198">System.String</span><span class="sxs-lookup"><span data-stu-id="2ee3c-198">System.String</span></span>

## <span data-ttu-id="2ee3c-199">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ee3c-199">OUTPUTS</span></span>

### <span data-ttu-id="2ee3c-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDhozzárendelés</span><span class="sxs-lookup"><span data-stu-id="2ee3c-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span></span>

## <span data-ttu-id="2ee3c-201">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2ee3c-201">NOTES</span></span>
<span data-ttu-id="2ee3c-202">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, telepítés</span><span class="sxs-lookup"><span data-stu-id="2ee3c-202">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="2ee3c-203">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ee3c-203">RELATED LINKS</span></span>
