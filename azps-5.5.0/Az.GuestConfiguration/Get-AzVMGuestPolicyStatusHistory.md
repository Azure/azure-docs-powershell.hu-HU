---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 929bc417cf4b84800635b85e7f503972509aa7fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204038"
---
# <span data-ttu-id="00f49-101">Get-AzVMGuestPolicyStatusHistory</span><span class="sxs-lookup"><span data-stu-id="00f49-101">Get-AzVMGuestPolicyStatusHistory</span></span>

## <span data-ttu-id="00f49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00f49-102">SYNOPSIS</span></span>
<span data-ttu-id="00f49-103">A virtuális géphez hozzárendelt "Vendégkonfiguráció" típusú kezdeményezéshez a vendégkonfigurációs házirendek megfelelőségi állapotelőzményeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="00f49-103">Gets guest configuration policy compliance status history for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="00f49-104">A kezdeményezés a "Initiative" definíciótípusú házirend.</span><span class="sxs-lookup"><span data-stu-id="00f49-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="00f49-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="00f49-105">SYNTAX</span></span>

### <span data-ttu-id="00f49-106">InitiativeNameScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="00f49-106">InitiativeNameScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00f49-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="00f49-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00f49-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="00f49-108">DESCRIPTION</span></span>
<span data-ttu-id="00f49-109">A Get-AzVMGuestPolicyStatusHistory parancsmag a virtuális géphez hozzárendelt "Vendégkonfiguráció" típusú kezdeményezéshez lekérte a vendégkonfigurációs házirendek megfelelőségi állapotelőzményeit.</span><span class="sxs-lookup"><span data-stu-id="00f49-109">The Get-AzVMGuestPolicyStatusHistory cmdlet gets compliance status history of guest configuration policies for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="00f49-110">A kezdeményezés a "Initiative" definíciótípusú házirend.</span><span class="sxs-lookup"><span data-stu-id="00f49-110">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="00f49-111">Egy Get-AzVMGuestPolicyStatus parancsmaggal lekértheti egyetlen megfelelőségi állapot részleteit a ReportId segítségével, amely egy parancsmag kimenetében Get-AzVMGuestPolicyStatusHistory található.</span><span class="sxs-lookup"><span data-stu-id="00f49-111">Use Get-AzVMGuestPolicyStatus cmdlet to get details of a single compliance status using ReportId that can be found in output of Get-AzVMGuestPolicyStatusHistory cmdlet.</span></span>

## <span data-ttu-id="00f49-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="00f49-112">EXAMPLES</span></span>

### <span data-ttu-id="00f49-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="00f49-113">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

<span data-ttu-id="00f49-114">Megfelelőségi állapotelőzményeket kap kezdeményezésazonosító alapján. A ShowOnlyChange kapcsoló csak a korábbi állapotváltozásokat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="00f49-114">Gets compliance status history by initiative Id. ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="00f49-115">Kihagyja az állapotokat, amelyek nem változtak két megfelelőségi ellenőrzés között.</span><span class="sxs-lookup"><span data-stu-id="00f49-115">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="00f49-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="00f49-116">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

<span data-ttu-id="00f49-117">Megfelelőségi állapotelőzményeket kap kezdeményezésnév szerint.</span><span class="sxs-lookup"><span data-stu-id="00f49-117">Gets compliance status history by initiative name.</span></span>
<span data-ttu-id="00f49-118">A ShowOnlyChange kapcsoló csak a korábbi állapotváltozásokat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="00f49-118">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="00f49-119">Kihagyja az állapotokat, amelyek nem változtak két megfelelőségi ellenőrzés között.</span><span class="sxs-lookup"><span data-stu-id="00f49-119">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="00f49-120">3. példa</span><span class="sxs-lookup"><span data-stu-id="00f49-120">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

<span data-ttu-id="00f49-121">Megfelelőségi állapotelőzményeket kap a virtuális géphez rendelt összes vendégkonfigurációs házirendhez.</span><span class="sxs-lookup"><span data-stu-id="00f49-121">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>
<span data-ttu-id="00f49-122">A ShowOnlyChange kapcsoló csak a korábbi állapotváltozásokat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="00f49-122">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="00f49-123">Kihagyja az állapotokat, amelyek nem változtak két megfelelőségi ellenőrzés között.</span><span class="sxs-lookup"><span data-stu-id="00f49-123">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="00f49-124">4. példa</span><span class="sxs-lookup"><span data-stu-id="00f49-124">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="00f49-125">Megfelelőségi állapotelőzményeket kap kezdeményezésazonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="00f49-125">Gets compliance status history by initiative Id.</span></span>

### <span data-ttu-id="00f49-126">5. példa</span><span class="sxs-lookup"><span data-stu-id="00f49-126">Example 5</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="00f49-127">Megfelelőségi állapotelőzményeket kap kezdeményezésnév szerint.</span><span class="sxs-lookup"><span data-stu-id="00f49-127">Gets compliance status history by initiative name.</span></span>

### <span data-ttu-id="00f49-128">6. példa</span><span class="sxs-lookup"><span data-stu-id="00f49-128">Example 6</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
<span data-ttu-id="00f49-129">Megfelelőségi állapotelőzményeket kap a virtuális géphez rendelt összes vendégkonfigurációs házirendhez.</span><span class="sxs-lookup"><span data-stu-id="00f49-129">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>

### <span data-ttu-id="00f49-130">7. példa</span><span class="sxs-lookup"><span data-stu-id="00f49-130">Example 7</span></span>
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

<span data-ttu-id="00f49-131">Vendégkonfigurációs házirend állapotának lekérte a ReportId alapján.</span><span class="sxs-lookup"><span data-stu-id="00f49-131">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="00f49-132">A ReportId a ReportId tulajdonság, amely a Get-AzVMGuestPolicyStatusHistory eredményében található.</span><span class="sxs-lookup"><span data-stu-id="00f49-132">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatusHistory.</span></span> <span data-ttu-id="00f49-133">(kérjük, adjon meg további példákat)</span><span class="sxs-lookup"><span data-stu-id="00f49-133">(please refer other examples)</span></span>

## <span data-ttu-id="00f49-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00f49-134">PARAMETERS</span></span>

### <span data-ttu-id="00f49-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00f49-135">-DefaultProfile</span></span>
<span data-ttu-id="00f49-136">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00f49-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00f49-137">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="00f49-137">-InitiativeId</span></span>
<span data-ttu-id="00f49-138">Annak a házirendnek a definícióazonosítója, amelyben a definíció típusa Kezdeményezés, a kategória pedig vendégkonfiguráció</span><span class="sxs-lookup"><span data-stu-id="00f49-138">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00f49-139">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="00f49-139">-InitiativeName</span></span>
<span data-ttu-id="00f49-140">Annak a házirendnek a neve, amelyben a definíció típusa Kezdeményezés, a kategória pedig vendégkonfiguráció</span><span class="sxs-lookup"><span data-stu-id="00f49-140">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeNameScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00f49-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00f49-141">-ResourceGroupName</span></span>
<span data-ttu-id="00f49-142">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="00f49-142">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00f49-143">-ShowOnlyChange</span><span class="sxs-lookup"><span data-stu-id="00f49-143">-ShowOnlyChange</span></span>
<span data-ttu-id="00f49-144">Csak a vendégkonfigurációs házirendek előzményállapot-módosításait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="00f49-144">Shows historical status changes only for guest configuration policies.</span></span>
<span data-ttu-id="00f49-145">Kihagyja az olyan állapotokat, amelyek nem változtak két megfelelőségi állapot-ellenőrzés futtatása között.</span><span class="sxs-lookup"><span data-stu-id="00f49-145">Skips statuses that have not changed between two compliance status audit runs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00f49-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="00f49-146">-VMName</span></span>
<span data-ttu-id="00f49-147">VM neve.</span><span class="sxs-lookup"><span data-stu-id="00f49-147">VM name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00f49-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00f49-148">CommonParameters</span></span>
<span data-ttu-id="00f49-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00f49-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00f49-150">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00f49-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00f49-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00f49-151">INPUTS</span></span>

### <span data-ttu-id="00f49-152">Nincs</span><span class="sxs-lookup"><span data-stu-id="00f49-152">None</span></span>
## <span data-ttu-id="00f49-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00f49-153">OUTPUTS</span></span>

### <span data-ttu-id="00f49-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span><span class="sxs-lookup"><span data-stu-id="00f49-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span></span>
## <span data-ttu-id="00f49-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="00f49-155">NOTES</span></span>

## <span data-ttu-id="00f49-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00f49-156">RELATED LINKS</span></span>
