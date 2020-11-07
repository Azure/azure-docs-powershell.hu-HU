---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: 160cff39918691c310de6931cd57cb415774d7e6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843438"
---
# <span data-ttu-id="8c947-101">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8c947-101">Get-AzPolicyAssignment</span></span>

## <span data-ttu-id="8c947-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8c947-102">SYNOPSIS</span></span>
<span data-ttu-id="8c947-103">Megkapja a házirend-hozzárendeléseket.</span><span class="sxs-lookup"><span data-stu-id="8c947-103">Gets policy assignments.</span></span>

## <span data-ttu-id="8c947-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8c947-104">SYNTAX</span></span>

### <span data-ttu-id="8c947-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c947-105">DefaultParameterSet (Default)</span></span>
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8c947-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c947-106">NameParameterSet</span></span>
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8c947-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c947-107">IncludeDescendentParameterSet</span></span>
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8c947-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c947-108">IdParameterSet</span></span>
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8c947-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="8c947-109">DESCRIPTION</span></span>
<span data-ttu-id="8c947-110">A **Get-AzPolicyAssignment** parancsmag minden házirend-feladatot vagy adott hozzárendelést beolvas.</span><span class="sxs-lookup"><span data-stu-id="8c947-110">The **Get-AzPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="8c947-111">A név és a hatókör vagy az azonosító alapján beolvasott házirend-hozzárendelés meghatározása</span><span class="sxs-lookup"><span data-stu-id="8c947-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="8c947-112">Példák</span><span class="sxs-lookup"><span data-stu-id="8c947-112">EXAMPLES</span></span>

### <span data-ttu-id="8c947-113">1. példa: az összes házirend-hozzárendelés beolvasása</span><span class="sxs-lookup"><span data-stu-id="8c947-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzPolicyAssignment
```

<span data-ttu-id="8c947-114">Ez a parancs az összes házirend-hozzárendelést megkapja.</span><span class="sxs-lookup"><span data-stu-id="8c947-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="8c947-115">2. példa: konkrét házirend-hozzárendelés beszerzése</span><span class="sxs-lookup"><span data-stu-id="8c947-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="8c947-116">Az első parancs beolvassa a ResourceGroup11 nevű erőforráscsoport nevű erőforráscsoportot a Get-AzResourceGroup cmdletand a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8c947-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdletand stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="8c947-117">A második parancs a PolicyAssignment07 nevű házirend-hozzárendelést kapja meg annak a hatókörnek a **ResourceId** tulajdonsága, amelyet az $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8c947-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="8c947-118">3. példa: a kezelési csoporthoz rendelt összes házirend-hozzárendelés beolvasása</span><span class="sxs-lookup"><span data-stu-id="8c947-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="8c947-119">Az első parancs a lekérdezni kívánt kezelési csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c947-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="8c947-120">A második parancs megkapja az összes olyan házirend-hozzárendelést, amely a "myManagementGroup" AZONOSÍTÓJÚ kezelési csoporthoz van rendelve.</span><span class="sxs-lookup"><span data-stu-id="8c947-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="8c947-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8c947-121">PARAMETERS</span></span>

### <span data-ttu-id="8c947-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8c947-122">-ApiVersion</span></span>
<span data-ttu-id="8c947-123">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c947-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8c947-124">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="8c947-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8c947-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c947-125">-DefaultProfile</span></span>
<span data-ttu-id="8c947-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8c947-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c947-127">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="8c947-127">-Id</span></span>
<span data-ttu-id="8c947-128">Annak a házirend-hozzárendelésnek a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="8c947-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8c947-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="8c947-129">-IncludeDescendent</span></span>
<span data-ttu-id="8c947-130">A visszaadott házirend-hozzárendelések listáját adja meg a megadott hatókörhöz kapcsolódó összes hozzárendelésnek, köztük az előd-hatóköröktől és a leszármazott hatóköröktől származó adatokból.</span><span class="sxs-lookup"><span data-stu-id="8c947-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

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

### <span data-ttu-id="8c947-131">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8c947-131">-InformationAction</span></span>
<span data-ttu-id="8c947-132">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="8c947-132">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="8c947-133">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8c947-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8c947-134">Folytassa</span><span class="sxs-lookup"><span data-stu-id="8c947-134">Continue</span></span>
- <span data-ttu-id="8c947-135">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="8c947-135">Ignore</span></span>
- <span data-ttu-id="8c947-136">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="8c947-136">Inquire</span></span>
- <span data-ttu-id="8c947-137">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8c947-137">SilentlyContinue</span></span>
- <span data-ttu-id="8c947-138">állj</span><span class="sxs-lookup"><span data-stu-id="8c947-138">Stop</span></span>
- <span data-ttu-id="8c947-139">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="8c947-139">Suspend</span></span>

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

### <span data-ttu-id="8c947-140">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8c947-140">-InformationVariable</span></span>
<span data-ttu-id="8c947-141">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="8c947-141">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8c947-142">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8c947-142">-Name</span></span>
<span data-ttu-id="8c947-143">Annak a házirend-hozzárendelésnek a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="8c947-143">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8c947-144">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="8c947-144">-PolicyDefinitionId</span></span>
<span data-ttu-id="8c947-145">Annak a házirend-hozzárendelésnek az AZONOSÍTÓját adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="8c947-145">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8c947-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="8c947-146">-Pre</span></span>
<span data-ttu-id="8c947-147">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="8c947-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8c947-148">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="8c947-148">-Scope</span></span>
<span data-ttu-id="8c947-149">Azt a hatókört adja meg, amelynél a program a parancsmagot tartalmazó hozzárendeléshez alkalmazza a házirendet.</span><span class="sxs-lookup"><span data-stu-id="8c947-149">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8c947-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c947-150">CommonParameters</span></span>
<span data-ttu-id="8c947-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8c947-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c947-152">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c947-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c947-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c947-153">INPUTS</span></span>

## <span data-ttu-id="8c947-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c947-154">OUTPUTS</span></span>

## <span data-ttu-id="8c947-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8c947-155">NOTES</span></span>

## <span data-ttu-id="8c947-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c947-156">RELATED LINKS</span></span>

[<span data-ttu-id="8c947-157">Új – AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8c947-157">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="8c947-158">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8c947-158">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="8c947-159">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8c947-159">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


