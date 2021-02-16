---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 49148f1c62b71436e48b2b92a4591a7cdb36cccf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154891"
---
# <span data-ttu-id="30e20-101">Get-AzVMGuestPolicyStatus</span><span class="sxs-lookup"><span data-stu-id="30e20-101">Get-AzVMGuestPolicyStatus</span></span>

## <span data-ttu-id="30e20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30e20-102">SYNOPSIS</span></span>
<span data-ttu-id="30e20-103">A virtuális géphez hozzárendelt "Vendégkonfiguráció" típusú kezdeményezés vendégkonfigurációs házirend-állapotát (részletes) kapja meg.</span><span class="sxs-lookup"><span data-stu-id="30e20-103">Gets guest configuration policy statuses (detailed) for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="30e20-104">A kezdeményezés a "Initiative" definíciótípusú házirend.</span><span class="sxs-lookup"><span data-stu-id="30e20-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="30e20-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="30e20-105">SYNTAX</span></span>

### <span data-ttu-id="30e20-106">VmScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="30e20-106">VmScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30e20-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="30e20-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30e20-108">InitiativeNameScope</span><span class="sxs-lookup"><span data-stu-id="30e20-108">InitiativeNameScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30e20-109">ReportIdScope</span><span class="sxs-lookup"><span data-stu-id="30e20-109">ReportIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30e20-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="30e20-110">DESCRIPTION</span></span>
<span data-ttu-id="30e20-111">A Get-AzVMGuestPolicyStatus parancsmag vendégkonfigurációs házirend-állapotokat kap egy virtuális géphez hozzárendelt "Vendégkonfiguráció" típusú kezdeményezéshez.</span><span class="sxs-lookup"><span data-stu-id="30e20-111">The Get-AzVMGuestPolicyStatus cmdlet gets guest configuration policy statuses for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="30e20-112">A kezdeményezés a "Initiative" definíciótípusú házirend.</span><span class="sxs-lookup"><span data-stu-id="30e20-112">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="30e20-113">Ez a parancsmag megfelelőségi állapotokat kap a VM-ről, és annak okait, hogy miért nem felel meg a kezdeményezésben található egyes házirendek követelményeinek.</span><span class="sxs-lookup"><span data-stu-id="30e20-113">This cmdlet gets compliance statuses of the VM and reasons why it is non-compliant for the individual policies in the initiative.</span></span>

## <span data-ttu-id="30e20-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="30e20-114">EXAMPLES</span></span>

### <span data-ttu-id="30e20-115">1. példa</span><span class="sxs-lookup"><span data-stu-id="30e20-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

<span data-ttu-id="30e20-116">Szerezze be a vm összes legújabb vendégkonfigurációs házirend-állapotát.</span><span class="sxs-lookup"><span data-stu-id="30e20-116">Get all latest guest configuration policy statuses for a VM.</span></span>
<span data-ttu-id="30e20-117">Az állapot tartalmazza a virtuális gép megfelelőségi állapotát minden olyan kezdeményezésben, amely a "Vendégkonfiguráció" típusú kezdeményezésekre vonatkozik, megfelelőségi okokból, a megfelelőségi ellenőrzés ideje, valamint a megfelelőség szempontjából ellenőrzött erőforrás-információk.</span><span class="sxs-lookup"><span data-stu-id="30e20-117">The status includes compliance status of the VM for each policy in all initiatives of type "Guest Configuration", compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="30e20-118">Az eredmények közé tartoznak a legutóbbi állapotok, a korábbi előzményállapotok nem.</span><span class="sxs-lookup"><span data-stu-id="30e20-118">The results include latest statuses, does not include previous historical statuses.</span></span>

### <span data-ttu-id="30e20-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="30e20-119">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="30e20-120">A legújabb vendégkonfigurációs házirend-állapotok lekérte kezdeményezésazonosító alapján. Az állapot tartalmazza a virtuális gép megfelelőségi állapotát a kezdeményezésben az egyes házirendek esetén, megfelelőségi okokból, a megfelelőségi ellenőrzés ideje, a megfelelőség szempontjából ellenőrzött erőforrás-információk.</span><span class="sxs-lookup"><span data-stu-id="30e20-120">Get the latest guest configuration policy statuses by initiative Id. The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="30e20-121">Az eredmények között nem szerepel a korábban létrehozott állapot, csak a kezdeményezésben található egyes házirendek legutóbbi állapota.</span><span class="sxs-lookup"><span data-stu-id="30e20-121">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="30e20-122">3. példa</span><span class="sxs-lookup"><span data-stu-id="30e20-122">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="30e20-123">A legújabb vendégkonfigurációs házirend-állapotok lekérte a kezdeményezés neve alapján.</span><span class="sxs-lookup"><span data-stu-id="30e20-123">Get the latest guest configuration policy statuses by initiative name.</span></span>
<span data-ttu-id="30e20-124">Az állapot tartalmazza a virtuális gép megfelelőségi állapotát a kezdeményezésben az egyes házirendek esetén, megfelelőségi okokból, a megfelelőségi ellenőrzés ideje, a megfelelőség szempontjából ellenőrzött erőforrás-információk.</span><span class="sxs-lookup"><span data-stu-id="30e20-124">The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="30e20-125">Az eredmények között nem szerepel a korábban létrehozott állapot, csak a kezdeményezésben található egyes házirendek legutóbbi állapota.</span><span class="sxs-lookup"><span data-stu-id="30e20-125">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="30e20-126">4. példa</span><span class="sxs-lookup"><span data-stu-id="30e20-126">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

<span data-ttu-id="30e20-127">Vendégkonfigurációs házirend állapotának lekérte a ReportId alapján.</span><span class="sxs-lookup"><span data-stu-id="30e20-127">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="30e20-128">A ReportId a ReportId tulajdonság, amely a Get-AzVMGuestPolicyStatus initiativeId vagy Initiative név alapján (további példákat is tartalmaz)</span><span class="sxs-lookup"><span data-stu-id="30e20-128">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatus by initiativeId or Initiative name (please refer other examples)</span></span>

## <span data-ttu-id="30e20-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30e20-129">PARAMETERS</span></span>

### <span data-ttu-id="30e20-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30e20-130">-DefaultProfile</span></span>
<span data-ttu-id="30e20-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30e20-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30e20-132">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="30e20-132">-InitiativeId</span></span>
<span data-ttu-id="30e20-133">Annak a házirendnek a definícióazonosítója, amelyben a definíció típusa Kezdeményezés, a kategória pedig vendégkonfiguráció</span><span class="sxs-lookup"><span data-stu-id="30e20-133">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="30e20-134">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="30e20-134">-InitiativeName</span></span>
<span data-ttu-id="30e20-135">Annak a házirendnek a neve, amelyben a definíció típusa Kezdeményezés, a kategória pedig vendégkonfiguráció</span><span class="sxs-lookup"><span data-stu-id="30e20-135">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="30e20-136">-ReportId</span><span class="sxs-lookup"><span data-stu-id="30e20-136">-ReportId</span></span>
<span data-ttu-id="30e20-137">Vendégkonfigurációs házirend-állapot azonosítója.</span><span class="sxs-lookup"><span data-stu-id="30e20-137">Id of a Guest Configuration policy status.</span></span>
<span data-ttu-id="30e20-138">Egy olyan házirendet, amelyben a definíció típusa Kezdeményezés, a kategória pedig vendégkonfiguráció, egy hatókörhöz kell rendelni az állapotok lekért állapotának ellenőrzéshez.</span><span class="sxs-lookup"><span data-stu-id="30e20-138">A policy where definition type is Initiative and category is Guest Configuration must be assigned to a scope to get statuses.</span></span>

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

### <span data-ttu-id="30e20-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30e20-139">-ResourceGroupName</span></span>
<span data-ttu-id="30e20-140">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="30e20-140">Resource group name.</span></span>

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

### <span data-ttu-id="30e20-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="30e20-141">-VMName</span></span>
<span data-ttu-id="30e20-142">VM neve.</span><span class="sxs-lookup"><span data-stu-id="30e20-142">VM name.</span></span>

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

### <span data-ttu-id="30e20-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30e20-143">CommonParameters</span></span>
<span data-ttu-id="30e20-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30e20-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30e20-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30e20-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30e20-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30e20-146">INPUTS</span></span>

### <span data-ttu-id="30e20-147">Nincs</span><span class="sxs-lookup"><span data-stu-id="30e20-147">None</span></span>
## <span data-ttu-id="30e20-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30e20-148">OUTPUTS</span></span>

### <span data-ttu-id="30e20-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span><span class="sxs-lookup"><span data-stu-id="30e20-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span></span>
## <span data-ttu-id="30e20-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="30e20-150">NOTES</span></span>

## <span data-ttu-id="30e20-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30e20-151">RELATED LINKS</span></span>
