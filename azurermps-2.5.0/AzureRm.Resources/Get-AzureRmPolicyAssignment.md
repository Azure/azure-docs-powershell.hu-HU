---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
ms.openlocfilehash: cabd2c86ed687b90b45e60b8078d89ad0a413c87
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849522"
---
# <span data-ttu-id="dabdc-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dabdc-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="dabdc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dabdc-102">SYNOPSIS</span></span>
<span data-ttu-id="dabdc-103">Megkapja a házirend-hozzárendeléseket.</span><span class="sxs-lookup"><span data-stu-id="dabdc-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dabdc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dabdc-104">SYNTAX</span></span>

### <span data-ttu-id="dabdc-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dabdc-105">DefaultParameterSet (Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="dabdc-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dabdc-106">NameParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="dabdc-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="dabdc-107">IncludeDescendentParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="dabdc-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dabdc-108">IdParameterSet</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="dabdc-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="dabdc-109">DESCRIPTION</span></span>
<span data-ttu-id="dabdc-110">A **Get-AzureRmPolicyAssignment** parancsmag minden házirend-feladatot vagy adott hozzárendelést beolvas.</span><span class="sxs-lookup"><span data-stu-id="dabdc-110">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="dabdc-111">A név és a hatókör vagy az azonosító alapján beolvasott házirend-hozzárendelés meghatározása</span><span class="sxs-lookup"><span data-stu-id="dabdc-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="dabdc-112">Példák</span><span class="sxs-lookup"><span data-stu-id="dabdc-112">EXAMPLES</span></span>

### <span data-ttu-id="dabdc-113">1. példa: az összes házirend-hozzárendelés beolvasása</span><span class="sxs-lookup"><span data-stu-id="dabdc-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzureRmPolicyAssignment
```

<span data-ttu-id="dabdc-114">Ez a parancs az összes házirend-hozzárendelést megkapja.</span><span class="sxs-lookup"><span data-stu-id="dabdc-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="dabdc-115">2. példa: konkrét házirend-hozzárendelés beszerzése</span><span class="sxs-lookup"><span data-stu-id="dabdc-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="dabdc-116">Az első parancs beolvassa a ResourceGroup11 nevű erőforráscsoport nevű erőforráscsoportot a Get-AzureRMResourceGroup cmdletand a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="dabdc-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdletand stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="dabdc-117">A második parancs a PolicyAssignment07 nevű házirend-hozzárendelést kapja meg annak a hatókörnek a **ResourceId** tulajdonsága, amelyet az $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="dabdc-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="dabdc-118">3. példa: a kezelési csoporthoz rendelt összes házirend-hozzárendelés beolvasása</span><span class="sxs-lookup"><span data-stu-id="dabdc-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzureRmPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="dabdc-119">Az első parancs a lekérdezni kívánt kezelési csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dabdc-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="dabdc-120">A második parancs megkapja az összes olyan házirend-hozzárendelést, amely a "myManagementGroup" AZONOSÍTÓJÚ kezelési csoporthoz van rendelve.</span><span class="sxs-lookup"><span data-stu-id="dabdc-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="dabdc-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dabdc-121">PARAMETERS</span></span>

### <span data-ttu-id="dabdc-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="dabdc-122">-ApiVersion</span></span>
<span data-ttu-id="dabdc-123">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dabdc-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="dabdc-124">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="dabdc-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="dabdc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dabdc-125">-DefaultProfile</span></span>
<span data-ttu-id="dabdc-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dabdc-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dabdc-127">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="dabdc-127">-Id</span></span>
<span data-ttu-id="dabdc-128">Annak a házirend-hozzárendelésnek a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="dabdc-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="dabdc-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="dabdc-129">-IncludeDescendent</span></span>
<span data-ttu-id="dabdc-130">A visszaadott házirend-hozzárendelések listáját adja meg a megadott hatókörhöz kapcsolódó összes hozzárendelésnek, köztük az előd-hatóköröktől és a leszármazott hatóköröktől származó adatokból.</span><span class="sxs-lookup"><span data-stu-id="dabdc-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

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

### <span data-ttu-id="dabdc-131">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="dabdc-131">-InformationAction</span></span>
<span data-ttu-id="dabdc-132">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="dabdc-132">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="dabdc-133">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="dabdc-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dabdc-134">Folytassa</span><span class="sxs-lookup"><span data-stu-id="dabdc-134">Continue</span></span>
- <span data-ttu-id="dabdc-135">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="dabdc-135">Ignore</span></span>
- <span data-ttu-id="dabdc-136">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="dabdc-136">Inquire</span></span>
- <span data-ttu-id="dabdc-137">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dabdc-137">SilentlyContinue</span></span>
- <span data-ttu-id="dabdc-138">állj</span><span class="sxs-lookup"><span data-stu-id="dabdc-138">Stop</span></span>
- <span data-ttu-id="dabdc-139">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="dabdc-139">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabdc-140">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dabdc-140">-InformationVariable</span></span>
<span data-ttu-id="dabdc-141">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="dabdc-141">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabdc-142">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dabdc-142">-Name</span></span>
<span data-ttu-id="dabdc-143">Annak a házirend-hozzárendelésnek a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="dabdc-143">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="dabdc-144">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="dabdc-144">-PolicyDefinitionId</span></span>
<span data-ttu-id="dabdc-145">Annak a házirend-hozzárendelésnek az AZONOSÍTÓját adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="dabdc-145">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

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

### <span data-ttu-id="dabdc-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="dabdc-146">-Pre</span></span>
<span data-ttu-id="dabdc-147">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="dabdc-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="dabdc-148">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="dabdc-148">-Scope</span></span>
<span data-ttu-id="dabdc-149">Azt a hatókört adja meg, amelynél a program a parancsmagot tartalmazó hozzárendeléshez alkalmazza a házirendet.</span><span class="sxs-lookup"><span data-stu-id="dabdc-149">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="dabdc-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dabdc-150">CommonParameters</span></span>
<span data-ttu-id="dabdc-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dabdc-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dabdc-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dabdc-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dabdc-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dabdc-153">INPUTS</span></span>

## <span data-ttu-id="dabdc-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dabdc-154">OUTPUTS</span></span>

## <span data-ttu-id="dabdc-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dabdc-155">NOTES</span></span>

## <span data-ttu-id="dabdc-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dabdc-156">RELATED LINKS</span></span>

[<span data-ttu-id="dabdc-157">Új – AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dabdc-157">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="dabdc-158">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dabdc-158">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="dabdc-159">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dabdc-159">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


