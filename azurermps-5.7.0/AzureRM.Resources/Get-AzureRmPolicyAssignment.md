---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 0604c7bd8f4f016f908eb7e9c93ff6b9d95db979
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679262"
---
# <span data-ttu-id="67621-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="67621-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="67621-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="67621-102">SYNOPSIS</span></span>
<span data-ttu-id="67621-103">Megkapja a házirend-hozzárendeléseket.</span><span class="sxs-lookup"><span data-stu-id="67621-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67621-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="67621-104">SYNTAX</span></span>

### <span data-ttu-id="67621-105">GetAllPolicyAssignments (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="67621-105">GetAllPolicyAssignments (Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="67621-106">GetPolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="67621-106">GetPolicyAssignmentName</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] -Scope <String> [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="67621-107">GetPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="67621-107">GetPolicyAssignmentId</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="67621-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="67621-108">DESCRIPTION</span></span>
<span data-ttu-id="67621-109">A **Get-AzureRmPolicyAssignment** parancsmag minden házirend-feladatot vagy adott hozzárendelést beolvas.</span><span class="sxs-lookup"><span data-stu-id="67621-109">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="67621-110">A név és a hatókör vagy az azonosító alapján beolvasott házirend-hozzárendelés meghatározása</span><span class="sxs-lookup"><span data-stu-id="67621-110">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="67621-111">Példák</span><span class="sxs-lookup"><span data-stu-id="67621-111">EXAMPLES</span></span>

### <span data-ttu-id="67621-112">1. példa: az összes házirend-hozzárendelés beolvasása</span><span class="sxs-lookup"><span data-stu-id="67621-112">Example 1: Get all policy assignments</span></span>
```
PS C:\>Get-AzureRmPolicyAssignment
```

<span data-ttu-id="67621-113">Ez a parancs az összes házirend-hozzárendelést megkapja.</span><span class="sxs-lookup"><span data-stu-id="67621-113">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="67621-114">2. példa: konkrét házirend-hozzárendelés beszerzése</span><span class="sxs-lookup"><span data-stu-id="67621-114">Example 2: Get a specific policy assignment</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="67621-115">Az első parancs az Get-AzureRMResourceGroup parancsmag segítségével a ResourceGroup11 nevű erőforráscsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="67621-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="67621-116">A parancs az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="67621-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="67621-117">A második parancs beolvassa a PolicyAssignment07 nevű házirend-hozzárendelést annak a hatókörnek a **ResourceId** tulajdonsága, amelyre az $ResourceGroup azonosítja.</span><span class="sxs-lookup"><span data-stu-id="67621-117">The second command get the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

## <span data-ttu-id="67621-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="67621-118">PARAMETERS</span></span>

### <span data-ttu-id="67621-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="67621-119">-ApiVersion</span></span>
<span data-ttu-id="67621-120">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="67621-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="67621-121">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="67621-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67621-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67621-122">-DefaultProfile</span></span>
<span data-ttu-id="67621-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="67621-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67621-124">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="67621-124">-Id</span></span>
<span data-ttu-id="67621-125">Annak a házirend-hozzárendelésnek a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="67621-125">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67621-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="67621-126">-InformationAction</span></span>
<span data-ttu-id="67621-127">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="67621-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="67621-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="67621-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="67621-129">Folytassa</span><span class="sxs-lookup"><span data-stu-id="67621-129">Continue</span></span>
- <span data-ttu-id="67621-130">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="67621-130">Ignore</span></span>
- <span data-ttu-id="67621-131">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="67621-131">Inquire</span></span>
- <span data-ttu-id="67621-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="67621-132">SilentlyContinue</span></span>
- <span data-ttu-id="67621-133">állj</span><span class="sxs-lookup"><span data-stu-id="67621-133">Stop</span></span>
- <span data-ttu-id="67621-134">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="67621-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67621-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="67621-135">-InformationVariable</span></span>
<span data-ttu-id="67621-136">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="67621-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67621-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="67621-137">-Name</span></span>
<span data-ttu-id="67621-138">Annak a házirend-hozzárendelésnek a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="67621-138">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67621-139">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="67621-139">-PolicyDefinitionId</span></span>
<span data-ttu-id="67621-140">Annak a házirend-hozzárendelésnek az AZONOSÍTÓját adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="67621-140">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName, GetPolicyAssignmentId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67621-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="67621-141">-Pre</span></span>
<span data-ttu-id="67621-142">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="67621-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67621-143">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="67621-143">-Scope</span></span>
<span data-ttu-id="67621-144">Azt a hatókört adja meg, amelynél a program a parancsmagot tartalmazó hozzárendeléshez alkalmazza a házirendet.</span><span class="sxs-lookup"><span data-stu-id="67621-144">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67621-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67621-145">CommonParameters</span></span>
<span data-ttu-id="67621-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="67621-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67621-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67621-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67621-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="67621-148">INPUTS</span></span>

### <span data-ttu-id="67621-149">Nincs</span><span class="sxs-lookup"><span data-stu-id="67621-149">None</span></span>
<span data-ttu-id="67621-150">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="67621-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="67621-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67621-151">OUTPUTS</span></span>

### <span data-ttu-id="67621-152">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="67621-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="67621-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="67621-153">NOTES</span></span>

## <span data-ttu-id="67621-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67621-154">RELATED LINKS</span></span>

[<span data-ttu-id="67621-155">Új – AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="67621-155">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="67621-156">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="67621-156">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="67621-157">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="67621-157">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


