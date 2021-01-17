---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: 4d5b230b741deec10daa44dab7e4faa44ac96b61
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340194"
---
# <span data-ttu-id="c8254-101">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c8254-101">Get-AzPolicyAssignment</span></span>

## <span data-ttu-id="c8254-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8254-102">SYNOPSIS</span></span>
<span data-ttu-id="c8254-103">Házirend-hozzárendeléseket kap.</span><span class="sxs-lookup"><span data-stu-id="c8254-103">Gets policy assignments.</span></span>

## <span data-ttu-id="c8254-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c8254-104">SYNTAX</span></span>

### <span data-ttu-id="c8254-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c8254-105">DefaultParameterSet (Default)</span></span>
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8254-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8254-106">NameParameterSet</span></span>
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8254-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8254-107">IncludeDescendentParameterSet</span></span>
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8254-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8254-108">IdParameterSet</span></span>
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8254-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c8254-109">DESCRIPTION</span></span>
<span data-ttu-id="c8254-110">A **Get-AzPolicyAssignment** parancsmag megkapja az összes házirend-hozzárendelést vagy bizonyos feladatot.</span><span class="sxs-lookup"><span data-stu-id="c8254-110">The **Get-AzPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="c8254-111">Azonosítsa a házirend-hozzárendeléseket név és hatókör, illetve azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="c8254-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="c8254-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c8254-112">EXAMPLES</span></span>

### <span data-ttu-id="c8254-113">1. példa: Az összes házirend-hozzárendelés lekérte</span><span class="sxs-lookup"><span data-stu-id="c8254-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzPolicyAssignment
```

<span data-ttu-id="c8254-114">Ez a parancs az összes házirend-hozzárendelést megkapja.</span><span class="sxs-lookup"><span data-stu-id="c8254-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="c8254-115">2. példa: Adott házirend-hozzárendelés kiosztása</span><span class="sxs-lookup"><span data-stu-id="c8254-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="c8254-116">Az első parancs egy ResourceGroup11 nevű erőforráscsoportot kap a Get-AzResourceGroup parancsmag használatával, és tárolja azt a $ResourceGroup változóban.</span><span class="sxs-lookup"><span data-stu-id="c8254-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c8254-117">A második parancs a PolicyAssignment07 nevű házirend-hozzárendelést kapja meg annak a hatókörnek a hatóköre alapján, $ResourceGroup **ResourceId** tulajdonsága azonosítja.</span><span class="sxs-lookup"><span data-stu-id="c8254-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="c8254-118">3. példa: A felügyeleti csoportokhoz rendelt összes házirend-hozzárendelés lekérte</span><span class="sxs-lookup"><span data-stu-id="c8254-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="c8254-119">Az első parancs megadja a lekérdezéshez használható felügyeleti csoport azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="c8254-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="c8254-120">A második parancs a felügyeleti csoporthoz hozzárendelt összes házirend-hozzárendelést a myManagementGroup azonosítóval kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c8254-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="c8254-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8254-121">PARAMETERS</span></span>

### <span data-ttu-id="c8254-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c8254-122">-ApiVersion</span></span>
<span data-ttu-id="c8254-123">Az erőforrás-szolgáltató API-jának használnia kell verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8254-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c8254-124">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="c8254-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c8254-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8254-125">-DefaultProfile</span></span>
<span data-ttu-id="c8254-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c8254-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8254-127">-Id</span><span class="sxs-lookup"><span data-stu-id="c8254-127">-Id</span></span>
<span data-ttu-id="c8254-128">A parancsmag által kapott házirend-hozzárendelés teljes erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8254-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c8254-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="c8254-129">-IncludeDescendent</span></span>
<span data-ttu-id="c8254-130">A visszaadott házirend-hozzárendelések listája az adott hatókörre vonatkozó összes hozzárendelést tartalmazza, beleértve az elődök és a csökkenő hatókörökből származó hozzárendeléseket is.</span><span class="sxs-lookup"><span data-stu-id="c8254-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

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

### <span data-ttu-id="c8254-131">-Name</span><span class="sxs-lookup"><span data-stu-id="c8254-131">-Name</span></span>
<span data-ttu-id="c8254-132">A parancsmag által kapott házirend-hozzárendelés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8254-132">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c8254-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="c8254-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="c8254-134">A parancsmag által kapott házirend-hozzárendelések házirenddefiníciójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c8254-134">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c8254-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="c8254-135">-Pre</span></span>
<span data-ttu-id="c8254-136">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="c8254-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c8254-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="c8254-137">-Scope</span></span>
<span data-ttu-id="c8254-138">Meghatározza, hogy milyen hatókörben alkalmazza a házirendet a parancsmag által kapott feladatra.</span><span class="sxs-lookup"><span data-stu-id="c8254-138">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c8254-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8254-139">CommonParameters</span></span>
<span data-ttu-id="c8254-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8254-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8254-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8254-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8254-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8254-142">INPUTS</span></span>

### <span data-ttu-id="c8254-143">System.String</span><span class="sxs-lookup"><span data-stu-id="c8254-143">System.String</span></span>

### <span data-ttu-id="c8254-144">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c8254-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c8254-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8254-145">OUTPUTS</span></span>

### <span data-ttu-id="c8254-146">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="c8254-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c8254-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c8254-147">NOTES</span></span>

## <span data-ttu-id="c8254-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8254-148">RELATED LINKS</span></span>

[<span data-ttu-id="c8254-149">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c8254-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="c8254-150">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c8254-150">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="c8254-151">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c8254-151">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


