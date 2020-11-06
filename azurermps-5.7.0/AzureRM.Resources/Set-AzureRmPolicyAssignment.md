---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
ms.openlocfilehash: 97be8f9eef611a87dae045df680d2823dc2f7acb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502459"
---
# <span data-ttu-id="bfdf9-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="bfdf9-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="bfdf9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bfdf9-102">SYNOPSIS</span></span>
<span data-ttu-id="bfdf9-103">Házirend-hozzárendelés módosítása</span><span class="sxs-lookup"><span data-stu-id="bfdf9-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfdf9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bfdf9-104">SYNTAX</span></span>

### <span data-ttu-id="bfdf9-105">SetByPolicyAssignmentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bfdf9-105">SetByPolicyAssignmentName (Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="bfdf9-106">SetByPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="bfdf9-106">SetByPolicyAssignmentId</span></span>
```
Set-AzureRmPolicyAssignment -Id <String> [-DisplayName <String>] [-Description <String>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bfdf9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bfdf9-107">DESCRIPTION</span></span>
<span data-ttu-id="bfdf9-108">A **set-AzureRmPolicyAssignment** parancsmag módosította egy házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="bfdf9-108">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="bfdf9-109">Adjon meg egy hozzárendelést azonosító alapján vagy név és hatókör szerint.</span><span class="sxs-lookup"><span data-stu-id="bfdf9-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="bfdf9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bfdf9-110">EXAMPLES</span></span>

### <span data-ttu-id="bfdf9-111">Példa 1: a megjelenítendő név frissítése</span><span class="sxs-lookup"><span data-stu-id="bfdf9-111">Example 1: Update the display name</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment" -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName "Do not allow VM creation"
```

<span data-ttu-id="bfdf9-112">Az első parancs az Get-AzureRMResourceGroup parancsmag segítségével a ResourceGroup11 nevű erőforráscsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="bfdf9-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="bfdf9-113">A parancs az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="bfdf9-113">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="bfdf9-114">A második parancs az Get-AzureRmPolicyAssignment parancsmag használatával kapja meg a PolicyAssignment nevű házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="bfdf9-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="bfdf9-115">A parancs az objektumot a $PolicyAssignment változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="bfdf9-115">The command stores that object in the $PolicyAssignment variable.</span></span>

<span data-ttu-id="bfdf9-116">A végleges parancs frissíti az $PolicyAssignment **ResourceId** tulajdonsága által azonosított házirend-hozzárendelés megjelenítendő nevét.</span><span class="sxs-lookup"><span data-stu-id="bfdf9-116">The final command updates the display name on the policy assignment identified by the **ResourceId** property of $PolicyAssignment.</span></span>

## <span data-ttu-id="bfdf9-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bfdf9-117">PARAMETERS</span></span>

### <span data-ttu-id="bfdf9-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bfdf9-118">-ApiVersion</span></span>
<span data-ttu-id="bfdf9-119">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bfdf9-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="bfdf9-120">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="bfdf9-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="bfdf9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfdf9-121">-DefaultProfile</span></span>
<span data-ttu-id="bfdf9-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bfdf9-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bfdf9-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="bfdf9-123">-Description</span></span>
<span data-ttu-id="bfdf9-124">A házirend-hozzárendelés leírása</span><span class="sxs-lookup"><span data-stu-id="bfdf9-124">The description for policy assignment</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfdf9-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bfdf9-125">-DisplayName</span></span>
<span data-ttu-id="bfdf9-126">A házirend-hozzárendelés új megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bfdf9-126">Specifies a new display name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfdf9-127">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="bfdf9-127">-Id</span></span>
<span data-ttu-id="bfdf9-128">Annak a házirend-hozzárendelésnek a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="bfdf9-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfdf9-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bfdf9-129">-InformationAction</span></span>
<span data-ttu-id="bfdf9-130">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="bfdf9-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bfdf9-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="bfdf9-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bfdf9-132">Folytassa</span><span class="sxs-lookup"><span data-stu-id="bfdf9-132">Continue</span></span>
- <span data-ttu-id="bfdf9-133">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="bfdf9-133">Ignore</span></span>
- <span data-ttu-id="bfdf9-134">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="bfdf9-134">Inquire</span></span>
- <span data-ttu-id="bfdf9-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bfdf9-135">SilentlyContinue</span></span>
- <span data-ttu-id="bfdf9-136">állj</span><span class="sxs-lookup"><span data-stu-id="bfdf9-136">Stop</span></span>
- <span data-ttu-id="bfdf9-137">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="bfdf9-137">Suspend</span></span>

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

### <span data-ttu-id="bfdf9-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bfdf9-138">-InformationVariable</span></span>
<span data-ttu-id="bfdf9-139">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="bfdf9-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bfdf9-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bfdf9-140">-Name</span></span>
<span data-ttu-id="bfdf9-141">Annak a házirend-hozzárendelésnek a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="bfdf9-141">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfdf9-142">-NotScope</span><span class="sxs-lookup"><span data-stu-id="bfdf9-142">-NotScope</span></span>
<span data-ttu-id="bfdf9-143">A házirend-hozzárendelés nem hatókörök.</span><span class="sxs-lookup"><span data-stu-id="bfdf9-143">The policy assignment not scopes.</span></span>

```yaml
Type: String[]
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfdf9-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="bfdf9-144">-Pre</span></span>
<span data-ttu-id="bfdf9-145">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="bfdf9-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="bfdf9-146">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="bfdf9-146">-Scope</span></span>
<span data-ttu-id="bfdf9-147">Azt a hatókört adja meg, amelyen a házirendet alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="bfdf9-147">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfdf9-148">-SKU</span><span class="sxs-lookup"><span data-stu-id="bfdf9-148">-Sku</span></span>
<span data-ttu-id="bfdf9-149">A SKU tulajdonságokat reprezentáló kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="bfdf9-149">A hash table which represents sku properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfdf9-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfdf9-150">CommonParameters</span></span>
<span data-ttu-id="bfdf9-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bfdf9-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfdf9-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfdf9-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfdf9-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfdf9-153">INPUTS</span></span>

### <span data-ttu-id="bfdf9-154">Nincs</span><span class="sxs-lookup"><span data-stu-id="bfdf9-154">None</span></span>
<span data-ttu-id="bfdf9-155">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="bfdf9-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bfdf9-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfdf9-156">OUTPUTS</span></span>

### <span data-ttu-id="bfdf9-157">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="bfdf9-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="bfdf9-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bfdf9-158">NOTES</span></span>

## <span data-ttu-id="bfdf9-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bfdf9-159">RELATED LINKS</span></span>

[<span data-ttu-id="bfdf9-160">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="bfdf9-160">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="bfdf9-161">Új – AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="bfdf9-161">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="bfdf9-162">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="bfdf9-162">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


