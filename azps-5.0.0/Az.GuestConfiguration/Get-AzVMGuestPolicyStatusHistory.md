---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 929bc417cf4b84800635b85e7f503972509aa7fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185398"
---
# <span data-ttu-id="42776-101">Get-AzVMGuestPolicyStatusHistory</span><span class="sxs-lookup"><span data-stu-id="42776-101">Get-AzVMGuestPolicyStatusHistory</span></span>

## <span data-ttu-id="42776-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="42776-102">SYNOPSIS</span></span>
<span data-ttu-id="42776-103">A vendég konfigurációja házirend megfelelőségi előzményeit kapja egy VM-hez rendelt "Guest Configuration" típusú kezdeményezéshez.</span><span class="sxs-lookup"><span data-stu-id="42776-103">Gets guest configuration policy compliance status history for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="42776-104">A kezdeményezés a "kezdeményezés" típusú definíciós házirend.</span><span class="sxs-lookup"><span data-stu-id="42776-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="42776-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="42776-105">SYNTAX</span></span>

### <span data-ttu-id="42776-106">InitiativeNameScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="42776-106">InitiativeNameScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42776-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="42776-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42776-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="42776-108">DESCRIPTION</span></span>
<span data-ttu-id="42776-109">A Get-AzVMGuestPolicyStatusHistory parancsmag a vendég konfigurációs házirendjeinek megfelelőségi előzményeit kapja egy VM-hez rendelt "Guest Configuration" típusú kezdeményezéshez.</span><span class="sxs-lookup"><span data-stu-id="42776-109">The Get-AzVMGuestPolicyStatusHistory cmdlet gets compliance status history of guest configuration policies for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="42776-110">A kezdeményezés a "kezdeményezés" típusú definíciós házirend.</span><span class="sxs-lookup"><span data-stu-id="42776-110">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="42776-111">Az Get-AzVMGuestPolicyStatus parancsmaggal az Get-AzVMGuestPolicyStatusHistory parancsmag kimenetében található ReportId használatával kaphat egyetlen megfelelőségi állapotot.</span><span class="sxs-lookup"><span data-stu-id="42776-111">Use Get-AzVMGuestPolicyStatus cmdlet to get details of a single compliance status using ReportId that can be found in output of Get-AzVMGuestPolicyStatusHistory cmdlet.</span></span>

## <span data-ttu-id="42776-112">Példák</span><span class="sxs-lookup"><span data-stu-id="42776-112">EXAMPLES</span></span>

### <span data-ttu-id="42776-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="42776-113">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

<span data-ttu-id="42776-114">A megfelelőségi előzményeket a kezdeményezési azonosítóval kapja meg. a ShowOnlyChange kapcsoló csak a múltbeli állapotokat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="42776-114">Gets compliance status history by initiative Id. ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="42776-115">Kihagyja azokat az állapotokat, amelyek nem változtak két megfelelőségi vizsgálat között.</span><span class="sxs-lookup"><span data-stu-id="42776-115">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="42776-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="42776-116">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

<span data-ttu-id="42776-117">A megfelelőségi előzményeket a kezdeményezés neve alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="42776-117">Gets compliance status history by initiative name.</span></span>
<span data-ttu-id="42776-118">A ShowOnlyChange-kapcsoló csak a múltbeli állapotok változásait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="42776-118">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="42776-119">Kihagyja azokat az állapotokat, amelyek nem változtak két megfelelőségi vizsgálat között.</span><span class="sxs-lookup"><span data-stu-id="42776-119">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="42776-120">3. példa</span><span class="sxs-lookup"><span data-stu-id="42776-120">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

<span data-ttu-id="42776-121">A VM-be rendelt összes vendégfiók-konfigurációs házirend megfelelőségi előzményeit kapja.</span><span class="sxs-lookup"><span data-stu-id="42776-121">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>
<span data-ttu-id="42776-122">A ShowOnlyChange-kapcsoló csak a múltbeli állapotok változásait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="42776-122">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="42776-123">Kihagyja azokat az állapotokat, amelyek nem változtak két megfelelőségi vizsgálat között.</span><span class="sxs-lookup"><span data-stu-id="42776-123">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="42776-124">4. példa</span><span class="sxs-lookup"><span data-stu-id="42776-124">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="42776-125">A megfelelési előzményeket kezdeményezési azonosítóval kapja meg.</span><span class="sxs-lookup"><span data-stu-id="42776-125">Gets compliance status history by initiative Id.</span></span>

### <span data-ttu-id="42776-126">Példa 5</span><span class="sxs-lookup"><span data-stu-id="42776-126">Example 5</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="42776-127">A megfelelőségi előzményeket a kezdeményezés neve alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="42776-127">Gets compliance status history by initiative name.</span></span>

### <span data-ttu-id="42776-128">6. példa</span><span class="sxs-lookup"><span data-stu-id="42776-128">Example 6</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
<span data-ttu-id="42776-129">A VM-be rendelt összes vendégfiók-konfigurációs házirend megfelelőségi előzményeit kapja.</span><span class="sxs-lookup"><span data-stu-id="42776-129">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>

### <span data-ttu-id="42776-130">7. példa</span><span class="sxs-lookup"><span data-stu-id="42776-130">Example 7</span></span>
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

<span data-ttu-id="42776-131">A vendégek konfigurációs házirendjének állapotát ReportId érheti el.</span><span class="sxs-lookup"><span data-stu-id="42776-131">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="42776-132">A ReportId a ReportId tulajdonság, amely a Get-AzVMGuestPolicyStatusHistory eredményei között található.</span><span class="sxs-lookup"><span data-stu-id="42776-132">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatusHistory.</span></span> <span data-ttu-id="42776-133">(kérjük, olvassa el a további példákat)</span><span class="sxs-lookup"><span data-stu-id="42776-133">(please refer other examples)</span></span>

## <span data-ttu-id="42776-134">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="42776-134">PARAMETERS</span></span>

### <span data-ttu-id="42776-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42776-135">-DefaultProfile</span></span>
<span data-ttu-id="42776-136">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="42776-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42776-137">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="42776-137">-InitiativeId</span></span>
<span data-ttu-id="42776-138">Definíciós azonosító egy olyan házirendhez, amelyben a definíció típusa a kezdeményezés, a kategória pedig a vendég konfigurációja</span><span class="sxs-lookup"><span data-stu-id="42776-138">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="42776-139">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="42776-139">-InitiativeName</span></span>
<span data-ttu-id="42776-140">Annak a házirendnek a neve, ahol a definíció típusa a kezdeményezés és a kategória a Guest Configuration</span><span class="sxs-lookup"><span data-stu-id="42776-140">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="42776-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42776-141">-ResourceGroupName</span></span>
<span data-ttu-id="42776-142">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="42776-142">Resource group name.</span></span>

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

### <span data-ttu-id="42776-143">-ShowOnlyChange</span><span class="sxs-lookup"><span data-stu-id="42776-143">-ShowOnlyChange</span></span>
<span data-ttu-id="42776-144">A múltbeli állapot módosításait csak a vendégek konfigurációs házirendjeihez jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="42776-144">Shows historical status changes only for guest configuration policies.</span></span>
<span data-ttu-id="42776-145">Kihagyja azokat az állapotokat, amelyek nem változtak két megfelelőségi állapot naplózása között.</span><span class="sxs-lookup"><span data-stu-id="42776-145">Skips statuses that have not changed between two compliance status audit runs.</span></span>

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

### <span data-ttu-id="42776-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="42776-146">-VMName</span></span>
<span data-ttu-id="42776-147">VM-név.</span><span class="sxs-lookup"><span data-stu-id="42776-147">VM name.</span></span>

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

### <span data-ttu-id="42776-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42776-148">CommonParameters</span></span>
<span data-ttu-id="42776-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="42776-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42776-150">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42776-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42776-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="42776-151">INPUTS</span></span>

### <span data-ttu-id="42776-152">Nincs</span><span class="sxs-lookup"><span data-stu-id="42776-152">None</span></span>
## <span data-ttu-id="42776-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="42776-153">OUTPUTS</span></span>

### <span data-ttu-id="42776-154">Microsoft. Azure. Command. GuestConfiguration. models. PolicyStatus</span><span class="sxs-lookup"><span data-stu-id="42776-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span></span>
## <span data-ttu-id="42776-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="42776-155">NOTES</span></span>

## <span data-ttu-id="42776-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="42776-156">RELATED LINKS</span></span>