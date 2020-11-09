---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: 4d5b230b741deec10daa44dab7e4faa44ac96b61
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301157"
---
# <span data-ttu-id="7c2ff-101">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7c2ff-101">Get-AzPolicyAssignment</span></span>

## <span data-ttu-id="7c2ff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c2ff-102">SYNOPSIS</span></span>
<span data-ttu-id="7c2ff-103">Megkapja a házirend-hozzárendeléseket.</span><span class="sxs-lookup"><span data-stu-id="7c2ff-103">Gets policy assignments.</span></span>

## <span data-ttu-id="7c2ff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c2ff-104">SYNTAX</span></span>

### <span data-ttu-id="7c2ff-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7c2ff-105">DefaultParameterSet (Default)</span></span>
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c2ff-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c2ff-106">NameParameterSet</span></span>
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c2ff-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c2ff-107">IncludeDescendentParameterSet</span></span>
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c2ff-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c2ff-108">IdParameterSet</span></span>
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c2ff-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c2ff-109">DESCRIPTION</span></span>
<span data-ttu-id="7c2ff-110">A **Get-AzPolicyAssignment** parancsmag minden házirend-feladatot vagy adott hozzárendelést beolvas.</span><span class="sxs-lookup"><span data-stu-id="7c2ff-110">The **Get-AzPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="7c2ff-111">A név és a hatókör vagy az azonosító alapján beolvasott házirend-hozzárendelés meghatározása</span><span class="sxs-lookup"><span data-stu-id="7c2ff-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="7c2ff-112">Példák</span><span class="sxs-lookup"><span data-stu-id="7c2ff-112">EXAMPLES</span></span>

### <span data-ttu-id="7c2ff-113">1. példa: az összes házirend-hozzárendelés beolvasása</span><span class="sxs-lookup"><span data-stu-id="7c2ff-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzPolicyAssignment
```

<span data-ttu-id="7c2ff-114">Ez a parancs az összes házirend-hozzárendelést megkapja.</span><span class="sxs-lookup"><span data-stu-id="7c2ff-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="7c2ff-115">2. példa: konkrét házirend-hozzárendelés beszerzése</span><span class="sxs-lookup"><span data-stu-id="7c2ff-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="7c2ff-116">Az első parancs beolvassa a ResourceGroup11 nevű erőforráscsoportot az Get-AzResourceGroup parancsmag használatával, és a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7c2ff-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="7c2ff-117">A második parancs a PolicyAssignment07 nevű házirend-hozzárendelést kapja meg annak a hatókörnek a **ResourceId** tulajdonsága, amelyet az $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7c2ff-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="7c2ff-118">3. példa: a kezelési csoporthoz rendelt összes házirend-hozzárendelés beolvasása</span><span class="sxs-lookup"><span data-stu-id="7c2ff-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="7c2ff-119">Az első parancs a lekérdezni kívánt kezelési csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c2ff-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="7c2ff-120">A második parancs megkapja az összes olyan házirend-hozzárendelést, amely a "myManagementGroup" AZONOSÍTÓJÚ kezelési csoporthoz van rendelve.</span><span class="sxs-lookup"><span data-stu-id="7c2ff-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="7c2ff-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c2ff-121">PARAMETERS</span></span>

### <span data-ttu-id="7c2ff-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7c2ff-122">-ApiVersion</span></span>
<span data-ttu-id="7c2ff-123">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c2ff-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7c2ff-124">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="7c2ff-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c2ff-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c2ff-125">-DefaultProfile</span></span>
<span data-ttu-id="7c2ff-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7c2ff-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c2ff-127">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="7c2ff-127">-Id</span></span>
<span data-ttu-id="7c2ff-128">Annak a házirend-hozzárendelésnek a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="7c2ff-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c2ff-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="7c2ff-129">-IncludeDescendent</span></span>
<span data-ttu-id="7c2ff-130">A visszaadott házirend-hozzárendelések listáját adja meg a megadott hatókörhöz kapcsolódó összes hozzárendelésnek, köztük az előd-hatóköröktől és a leszármazott hatóköröktől származó adatokból.</span><span class="sxs-lookup"><span data-stu-id="7c2ff-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IncludeDescendentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c2ff-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7c2ff-131">-Name</span></span>
<span data-ttu-id="7c2ff-132">Annak a házirend-hozzárendelésnek a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="7c2ff-132">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c2ff-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="7c2ff-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="7c2ff-134">Annak a házirend-hozzárendelésnek az AZONOSÍTÓját adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="7c2ff-134">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c2ff-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="7c2ff-135">-Pre</span></span>
<span data-ttu-id="7c2ff-136">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="7c2ff-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7c2ff-137">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="7c2ff-137">-Scope</span></span>
<span data-ttu-id="7c2ff-138">Azt a hatókört adja meg, amelynél a program a parancsmagot tartalmazó hozzárendeléshez alkalmazza a házirendet.</span><span class="sxs-lookup"><span data-stu-id="7c2ff-138">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IncludeDescendentParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c2ff-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c2ff-139">CommonParameters</span></span>
<span data-ttu-id="7c2ff-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7c2ff-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c2ff-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7c2ff-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c2ff-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c2ff-142">INPUTS</span></span>

### <span data-ttu-id="7c2ff-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7c2ff-143">System.String</span></span>

### <span data-ttu-id="7c2ff-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7c2ff-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7c2ff-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c2ff-145">OUTPUTS</span></span>

### <span data-ttu-id="7c2ff-146">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="7c2ff-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7c2ff-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c2ff-147">NOTES</span></span>

## <span data-ttu-id="7c2ff-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c2ff-148">RELATED LINKS</span></span>

[<span data-ttu-id="7c2ff-149">Új – AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7c2ff-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="7c2ff-150">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7c2ff-150">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="7c2ff-151">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7c2ff-151">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


