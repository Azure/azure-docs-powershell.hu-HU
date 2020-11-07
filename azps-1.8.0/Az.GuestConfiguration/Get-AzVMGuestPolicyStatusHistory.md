---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 2e2474b784d66c3c3c34bc9ea9abc2b0959ea500
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836098"
---
# <span data-ttu-id="15c25-101">Get-AzVMGuestPolicyStatusHistory</span><span class="sxs-lookup"><span data-stu-id="15c25-101">Get-AzVMGuestPolicyStatusHistory</span></span>

## <span data-ttu-id="15c25-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15c25-102">SYNOPSIS</span></span>
<span data-ttu-id="15c25-103">A vendég konfigurációja házirend megfelelőségi előzményeit kapja egy VM-hez rendelt "Guest Configuration" típusú kezdeményezéshez.</span><span class="sxs-lookup"><span data-stu-id="15c25-103">Gets guest configuration policy compliance status history for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="15c25-104">A kezdeményezés a "kezdeményezés" típusú definíciós házirend.</span><span class="sxs-lookup"><span data-stu-id="15c25-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="15c25-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15c25-105">SYNTAX</span></span>

### <span data-ttu-id="15c25-106">InitiativeNameScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="15c25-106">InitiativeNameScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15c25-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="15c25-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15c25-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="15c25-108">DESCRIPTION</span></span>
<span data-ttu-id="15c25-109">A Get-AzVMGuestPolicyStatusHistory parancsmag a vendég konfigurációs házirendjeinek megfelelőségi előzményeit kapja egy VM-hez rendelt "Guest Configuration" típusú kezdeményezéshez.</span><span class="sxs-lookup"><span data-stu-id="15c25-109">The Get-AzVMGuestPolicyStatusHistory cmdlet gets compliance status history of guest configuration policies for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="15c25-110">A kezdeményezés a "kezdeményezés" típusú definíciós házirend.</span><span class="sxs-lookup"><span data-stu-id="15c25-110">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="15c25-111">Az Get-AzVMGuestPolicyStatus parancsmaggal az Get-AzVMGuestPolicyStatusHistory parancsmag kimenetében található ReportId használatával kaphat egyetlen megfelelőségi állapotot.</span><span class="sxs-lookup"><span data-stu-id="15c25-111">Use Get-AzVMGuestPolicyStatus cmdlet to get details of a single compliance status using ReportId that can be found in output of Get-AzVMGuestPolicyStatusHistory cmdlet.</span></span>

## <span data-ttu-id="15c25-112">Példák</span><span class="sxs-lookup"><span data-stu-id="15c25-112">EXAMPLES</span></span>

### <span data-ttu-id="15c25-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="15c25-113">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

<span data-ttu-id="15c25-114">A megfelelőségi előzményeket a kezdeményezési azonosítóval kapja meg. a ShowOnlyChange kapcsoló csak a múltbeli állapotokat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="15c25-114">Gets compliance status history by initiative Id. ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="15c25-115">Kihagyja azokat az állapotokat, amelyek nem változtak két megfelelőségi vizsgálat között.</span><span class="sxs-lookup"><span data-stu-id="15c25-115">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="15c25-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="15c25-116">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

<span data-ttu-id="15c25-117">A megfelelőségi előzményeket a kezdeményezés neve alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="15c25-117">Gets compliance status history by initiative name.</span></span>
<span data-ttu-id="15c25-118">A ShowOnlyChange-kapcsoló csak a múltbeli állapotok változásait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="15c25-118">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="15c25-119">Kihagyja azokat az állapotokat, amelyek nem változtak két megfelelőségi vizsgálat között.</span><span class="sxs-lookup"><span data-stu-id="15c25-119">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="15c25-120">3. példa</span><span class="sxs-lookup"><span data-stu-id="15c25-120">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

<span data-ttu-id="15c25-121">A VM-be rendelt összes vendégfiók-konfigurációs házirend megfelelőségi előzményeit kapja.</span><span class="sxs-lookup"><span data-stu-id="15c25-121">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>
<span data-ttu-id="15c25-122">A ShowOnlyChange-kapcsoló csak a múltbeli állapotok változásait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="15c25-122">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="15c25-123">Kihagyja azokat az állapotokat, amelyek nem változtak két megfelelőségi vizsgálat között.</span><span class="sxs-lookup"><span data-stu-id="15c25-123">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="15c25-124">4. példa</span><span class="sxs-lookup"><span data-stu-id="15c25-124">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="15c25-125">A megfelelési előzményeket kezdeményezési azonosítóval kapja meg.</span><span class="sxs-lookup"><span data-stu-id="15c25-125">Gets compliance status history by initiative Id.</span></span>

### <span data-ttu-id="15c25-126">Példa 5</span><span class="sxs-lookup"><span data-stu-id="15c25-126">Example 5</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="15c25-127">A megfelelőségi előzményeket a kezdeményezés neve alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="15c25-127">Gets compliance status history by initiative name.</span></span>

### <span data-ttu-id="15c25-128">6. példa</span><span class="sxs-lookup"><span data-stu-id="15c25-128">Example 6</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
<span data-ttu-id="15c25-129">A VM-be rendelt összes vendégfiók-konfigurációs házirend megfelelőségi előzményeit kapja.</span><span class="sxs-lookup"><span data-stu-id="15c25-129">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>

### <span data-ttu-id="15c25-130">7. példa</span><span class="sxs-lookup"><span data-stu-id="15c25-130">Example 7</span></span>
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

<span data-ttu-id="15c25-131">A vendégek konfigurációs házirendjének állapotát ReportId érheti el.</span><span class="sxs-lookup"><span data-stu-id="15c25-131">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="15c25-132">A ReportId a ReportId tulajdonság, amely a Get-AzVMGuestPolicyStatusHistory eredményei között található.</span><span class="sxs-lookup"><span data-stu-id="15c25-132">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatusHistory.</span></span> <span data-ttu-id="15c25-133">(kérjük, olvassa el a további példákat)</span><span class="sxs-lookup"><span data-stu-id="15c25-133">(please refer other examples)</span></span>

## <span data-ttu-id="15c25-134">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15c25-134">PARAMETERS</span></span>

### <span data-ttu-id="15c25-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15c25-135">-DefaultProfile</span></span>
<span data-ttu-id="15c25-136">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15c25-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15c25-137">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="15c25-137">-InitiativeId</span></span>
<span data-ttu-id="15c25-138">Definíciós azonosító egy olyan házirendhez, amelyben a definíció típusa a kezdeményezés, a kategória pedig a vendég konfigurációja</span><span class="sxs-lookup"><span data-stu-id="15c25-138">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="15c25-139">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="15c25-139">-InitiativeName</span></span>
<span data-ttu-id="15c25-140">Annak a házirendnek a neve, ahol a definíció típusa a kezdeményezés és a kategória a Guest Configuration</span><span class="sxs-lookup"><span data-stu-id="15c25-140">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="15c25-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15c25-141">-ResourceGroupName</span></span>
<span data-ttu-id="15c25-142">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="15c25-142">Resource group name.</span></span>

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

### <span data-ttu-id="15c25-143">-ShowOnlyChange</span><span class="sxs-lookup"><span data-stu-id="15c25-143">-ShowOnlyChange</span></span>
<span data-ttu-id="15c25-144">A múltbeli állapot módosításait csak a vendégek konfigurációs házirendjeihez jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="15c25-144">Shows historical status changes only for guest configuration policies.</span></span>
<span data-ttu-id="15c25-145">Kihagyja azokat az állapotokat, amelyek nem változtak két megfelelőségi állapot naplózása között.</span><span class="sxs-lookup"><span data-stu-id="15c25-145">Skips statuses that have not changed between two compliance status audit runs.</span></span>

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

### <span data-ttu-id="15c25-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="15c25-146">-VMName</span></span>
<span data-ttu-id="15c25-147">VM-név.</span><span class="sxs-lookup"><span data-stu-id="15c25-147">VM name.</span></span>

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

### <span data-ttu-id="15c25-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15c25-148">CommonParameters</span></span>
<span data-ttu-id="15c25-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15c25-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15c25-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15c25-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15c25-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15c25-151">INPUTS</span></span>

### <span data-ttu-id="15c25-152">Nincs</span><span class="sxs-lookup"><span data-stu-id="15c25-152">None</span></span>
## <span data-ttu-id="15c25-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15c25-153">OUTPUTS</span></span>

### <span data-ttu-id="15c25-154">Microsoft. Azure. Command. GuestConfiguration. models. PolicyStatus</span><span class="sxs-lookup"><span data-stu-id="15c25-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span></span>
## <span data-ttu-id="15c25-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15c25-155">NOTES</span></span>

## <span data-ttu-id="15c25-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15c25-156">RELATED LINKS</span></span>
