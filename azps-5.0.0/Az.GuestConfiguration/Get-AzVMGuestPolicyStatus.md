---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 49148f1c62b71436e48b2b92a4591a7cdb36cccf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185402"
---
# <span data-ttu-id="6ce3c-101">Get-AzVMGuestPolicyStatus</span><span class="sxs-lookup"><span data-stu-id="6ce3c-101">Get-AzVMGuestPolicyStatus</span></span>

## <span data-ttu-id="6ce3c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6ce3c-102">SYNOPSIS</span></span>
<span data-ttu-id="6ce3c-103">Egy VM-hez rendelt "vendég konfigurációja" típusú kezdeményezéshez (részletesen) kapja a vendégek konfigurációs házirend-állapotát.</span><span class="sxs-lookup"><span data-stu-id="6ce3c-103">Gets guest configuration policy statuses (detailed) for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="6ce3c-104">A kezdeményezés a "kezdeményezés" típusú definíciós házirend.</span><span class="sxs-lookup"><span data-stu-id="6ce3c-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="6ce3c-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6ce3c-105">SYNTAX</span></span>

### <span data-ttu-id="6ce3c-106">VmScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6ce3c-106">VmScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ce3c-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="6ce3c-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ce3c-108">InitiativeNameScope</span><span class="sxs-lookup"><span data-stu-id="6ce3c-108">InitiativeNameScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ce3c-109">ReportIdScope</span><span class="sxs-lookup"><span data-stu-id="6ce3c-109">ReportIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ce3c-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="6ce3c-110">DESCRIPTION</span></span>
<span data-ttu-id="6ce3c-111">A Get-AzVMGuestPolicyStatus parancsmagban egy VM-hez rendelt "vendég konfigurációja" típusú kezdeményezéshez kapja meg a Guest Configuration Policy állapotát.</span><span class="sxs-lookup"><span data-stu-id="6ce3c-111">The Get-AzVMGuestPolicyStatus cmdlet gets guest configuration policy statuses for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="6ce3c-112">A kezdeményezés a "kezdeményezés" típusú definíciós házirend.</span><span class="sxs-lookup"><span data-stu-id="6ce3c-112">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="6ce3c-113">Ez a parancsmag a VM megfelelőségi állapotát és annak okait kapja meg, hogy miért nem kompatibilis a kezdeményezésben szereplő egyes házirendekkel.</span><span class="sxs-lookup"><span data-stu-id="6ce3c-113">This cmdlet gets compliance statuses of the VM and reasons why it is non-compliant for the individual policies in the initiative.</span></span>

## <span data-ttu-id="6ce3c-114">Példák</span><span class="sxs-lookup"><span data-stu-id="6ce3c-114">EXAMPLES</span></span>

### <span data-ttu-id="6ce3c-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6ce3c-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

<span data-ttu-id="6ce3c-116">Megtudhatja, hogy miként szerezheti be a legújabb konfiguráció házirend-állapotát egy VM-hez.</span><span class="sxs-lookup"><span data-stu-id="6ce3c-116">Get all latest guest configuration policy statuses for a VM.</span></span>
<span data-ttu-id="6ce3c-117">Az állapot magában foglalja a VM megfelelőségi állapotát a "vendég konfigurációja" típus minden kezdeményezéséhez, a megfelelőségi vizsgálat időpontját, a megfelelőségi vizsgálat időpontját, a megfelelőségi vizsgálat során ellenőrzött erőforrás-információkat.</span><span class="sxs-lookup"><span data-stu-id="6ce3c-117">The status includes compliance status of the VM for each policy in all initiatives of type "Guest Configuration", compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="6ce3c-118">Az eredmény a legújabb állapotokat tartalmazza, és nem tartalmazza az előző korábbi állapotokat.</span><span class="sxs-lookup"><span data-stu-id="6ce3c-118">The results include latest statuses, does not include previous historical statuses.</span></span>

### <span data-ttu-id="6ce3c-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="6ce3c-119">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="6ce3c-120">A legújabb konfiguráció-házirendek állapotának beszerzése kezdeményezési azonosítóval Az állapot magában foglalja a VM megfelelőségi állapotát a kezdeményezés minden házirendjéhez, megfelelőségi okok, a megfelelőségi ellenőrzés időpontja, a megfelelőségi vizsgálat során ellenőrzött erőforrás-adatok.</span><span class="sxs-lookup"><span data-stu-id="6ce3c-120">Get the latest guest configuration policy statuses by initiative Id. The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="6ce3c-121">Az eredmény nem tartalmazza az előző állapotokat, de a kezdeményezés minden házirendjéhez csak a legújabb állapotot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6ce3c-121">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="6ce3c-122">3. példa</span><span class="sxs-lookup"><span data-stu-id="6ce3c-122">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="6ce3c-123">A legújabb konfiguráció házirend-állapotának beszerzése a kezdeményezés neve szerint</span><span class="sxs-lookup"><span data-stu-id="6ce3c-123">Get the latest guest configuration policy statuses by initiative name.</span></span>
<span data-ttu-id="6ce3c-124">Az állapot magában foglalja a VM megfelelőségi állapotát a kezdeményezés minden házirendjéhez, megfelelőségi okok, a megfelelőségi ellenőrzés időpontja, a megfelelőségi vizsgálat során ellenőrzött erőforrás-adatok.</span><span class="sxs-lookup"><span data-stu-id="6ce3c-124">The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="6ce3c-125">Az eredmény nem tartalmazza az előző állapotokat, de a kezdeményezés minden házirendjéhez csak a legújabb állapotot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6ce3c-125">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="6ce3c-126">4. példa</span><span class="sxs-lookup"><span data-stu-id="6ce3c-126">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

<span data-ttu-id="6ce3c-127">A vendégek konfigurációs házirendjének állapotát ReportId érheti el.</span><span class="sxs-lookup"><span data-stu-id="6ce3c-127">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="6ce3c-128">A ReportId a ReportId tulajdonság, amely a initiativeId vagy Get-AzVMGuestPolicyStatus a kezdeményezés neve szerint (kérjük, további példákat is tartalmaz)</span><span class="sxs-lookup"><span data-stu-id="6ce3c-128">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatus by initiativeId or Initiative name (please refer other examples)</span></span>

## <span data-ttu-id="6ce3c-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6ce3c-129">PARAMETERS</span></span>

### <span data-ttu-id="6ce3c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ce3c-130">-DefaultProfile</span></span>
<span data-ttu-id="6ce3c-131">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ce3c-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ce3c-132">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="6ce3c-132">-InitiativeId</span></span>
<span data-ttu-id="6ce3c-133">Definíciós azonosító egy olyan házirendhez, amelyben a definíció típusa a kezdeményezés, a kategória pedig a vendég konfigurációja</span><span class="sxs-lookup"><span data-stu-id="6ce3c-133">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ce3c-134">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="6ce3c-134">-InitiativeName</span></span>
<span data-ttu-id="6ce3c-135">Annak a házirendnek a neve, ahol a definíció típusa a kezdeményezés és a kategória a Guest Configuration</span><span class="sxs-lookup"><span data-stu-id="6ce3c-135">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="6ce3c-136">-ReportId</span><span class="sxs-lookup"><span data-stu-id="6ce3c-136">-ReportId</span></span>
<span data-ttu-id="6ce3c-137">A vendég konfigurációja házirend-állapot azonosítója</span><span class="sxs-lookup"><span data-stu-id="6ce3c-137">Id of a Guest Configuration policy status.</span></span>
<span data-ttu-id="6ce3c-138">Egy olyan házirend, ahol a definíció típusa a kezdeményezés és a kategória, a program a tartományhoz társítja a jogosultságokat.</span><span class="sxs-lookup"><span data-stu-id="6ce3c-138">A policy where definition type is Initiative and category is Guest Configuration must be assigned to a scope to get statuses.</span></span>

```yaml
Type: System.String
Parameter Sets: ReportIdScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ce3c-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ce3c-139">-ResourceGroupName</span></span>
<span data-ttu-id="6ce3c-140">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="6ce3c-140">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ce3c-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="6ce3c-141">-VMName</span></span>
<span data-ttu-id="6ce3c-142">VM-név.</span><span class="sxs-lookup"><span data-stu-id="6ce3c-142">VM name.</span></span>

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ce3c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ce3c-143">CommonParameters</span></span>
<span data-ttu-id="6ce3c-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6ce3c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ce3c-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ce3c-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ce3c-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ce3c-146">INPUTS</span></span>

### <span data-ttu-id="6ce3c-147">Nincs</span><span class="sxs-lookup"><span data-stu-id="6ce3c-147">None</span></span>
## <span data-ttu-id="6ce3c-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ce3c-148">OUTPUTS</span></span>

### <span data-ttu-id="6ce3c-149">Microsoft. Azure. Command. GuestConfiguration. models. PolicyStatusDetailed</span><span class="sxs-lookup"><span data-stu-id="6ce3c-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span></span>
## <span data-ttu-id="6ce3c-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6ce3c-150">NOTES</span></span>

## <span data-ttu-id="6ce3c-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ce3c-151">RELATED LINKS</span></span>