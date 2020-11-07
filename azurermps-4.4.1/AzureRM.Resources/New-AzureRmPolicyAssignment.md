---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: fa43b462cf06b9e2cd58df5d6796c098e942fafc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679341"
---
# <span data-ttu-id="b9445-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b9445-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="b9445-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9445-102">SYNOPSIS</span></span>
<span data-ttu-id="b9445-103">Házirend-hozzárendelést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b9445-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9445-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9445-104">SYNTAX</span></span>

### <span data-ttu-id="b9445-105">Házirend-hozzárendelés paraméterek nélkül (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9445-105">Policy assignment without parameters (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b9445-106">Házirend-hozzárendelés paraméteres objektumon keresztüli paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="b9445-106">Policy assignment with parameters via policy parameter object</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b9445-107">Házirend-hozzárendelés paraméteres karakterlánc-karakterláncon keresztül</span><span class="sxs-lookup"><span data-stu-id="b9445-107">Policy assignment with parameters via policy parameter string</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b9445-108">Házirend-hozzárendelés paraméterekkel a Policy set paraméteres objektumon keresztül</span><span class="sxs-lookup"><span data-stu-id="b9445-108">Policy assignment with parameters via policy set parameter object</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b9445-109">Házirend-hozzárendelés paraméter-karakterláncon keresztüli paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="b9445-109">Policy assignment with parameters via policy set parameter string</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b9445-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9445-110">DESCRIPTION</span></span>
<span data-ttu-id="b9445-111">A **New-AzureRmPolicyAssignment** parancsmag létrehoz egy házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="b9445-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="b9445-112">Adjon meg egy házirendet és egy hatókört.</span><span class="sxs-lookup"><span data-stu-id="b9445-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="b9445-113">Példák</span><span class="sxs-lookup"><span data-stu-id="b9445-113">EXAMPLES</span></span>

### <span data-ttu-id="b9445-114">1. példa: házirend-hozzárendelés az erőforrás csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="b9445-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name "VirtualMachinePolicy"
PS C:\> New-AzureRmPolicyAssignment -Name "VirtualMachinePolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="b9445-115">Az első parancs az Get-AzureRMResourceGroup parancsmag segítségével a ResourceGroup11 nevű erőforráscsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="b9445-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="b9445-116">A parancs az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b9445-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="b9445-117">A második parancs az Get-AzureRmPolicyDefinition parancsmag segítségével a VirtualMachinePolicy nevű házirend-definíciót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b9445-117">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="b9445-118">A parancs az objektumot a $Policy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b9445-118">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="b9445-119">A végleges parancs az erőforráscsoport szintjén rendeli hozzá a házirendet a $Policyhoz.</span><span class="sxs-lookup"><span data-stu-id="b9445-119">The final command assigns the policy in $Policy at the level of a resource group.</span></span>
<span data-ttu-id="b9445-120">A $ResourceGroup **ResourceId** tulajdonság azonosítja az erőforráscsoport értékét.</span><span class="sxs-lookup"><span data-stu-id="b9445-120">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

## <span data-ttu-id="b9445-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9445-121">PARAMETERS</span></span>

### <span data-ttu-id="b9445-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b9445-122">-ApiVersion</span></span>
<span data-ttu-id="b9445-123">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9445-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b9445-124">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="b9445-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b9445-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b9445-125">-DisplayName</span></span>
<span data-ttu-id="b9445-126">A házirend-hozzárendelés megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9445-126">Specifies a display name for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9445-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b9445-127">-InformationAction</span></span>
<span data-ttu-id="b9445-128">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="b9445-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b9445-129">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b9445-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b9445-130">Folytassa</span><span class="sxs-lookup"><span data-stu-id="b9445-130">Continue</span></span>
- <span data-ttu-id="b9445-131">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="b9445-131">Ignore</span></span>
- <span data-ttu-id="b9445-132">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="b9445-132">Inquire</span></span>
- <span data-ttu-id="b9445-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b9445-133">SilentlyContinue</span></span>
- <span data-ttu-id="b9445-134">állj</span><span class="sxs-lookup"><span data-stu-id="b9445-134">Stop</span></span>
- <span data-ttu-id="b9445-135">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="b9445-135">Suspend</span></span>

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

### <span data-ttu-id="b9445-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b9445-136">-InformationVariable</span></span>
<span data-ttu-id="b9445-137">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="b9445-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b9445-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b9445-138">-Name</span></span>
<span data-ttu-id="b9445-139">A házirend-hozzárendelés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9445-139">Specifies a name for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9445-140">-NotScope</span><span class="sxs-lookup"><span data-stu-id="b9445-140">-NotScope</span></span>
<span data-ttu-id="b9445-141">A házirend-hozzárendeléshez nem tartozó hatókörök</span><span class="sxs-lookup"><span data-stu-id="b9445-141">The not scopes for policy assignment.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9445-142">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b9445-142">-PolicyDefinition</span></span>
<span data-ttu-id="b9445-143">A házirendet adja meg **PSObject** -objektumként, amely a házirend-szabályt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b9445-143">Specifies a policy, as a **PSObject** object that contains the policy rule.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment without parameters, Policy assignment with parameters via policy set parameter object, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9445-144">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="b9445-144">-PolicyParameter</span></span>
<span data-ttu-id="b9445-145">A házirend paraméterének fájlelérési útja vagy a házirend paraméterének karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="b9445-145">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: System.String
Parameter Sets: Policy assignment with parameters via policy parameter string, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9445-146">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="b9445-146">-PolicyParameterObject</span></span>
<span data-ttu-id="b9445-147">A Policy paraméter objektuma.</span><span class="sxs-lookup"><span data-stu-id="b9445-147">The policy parameter object.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy set parameter object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9445-148">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="b9445-148">-PolicySetDefinition</span></span>
<span data-ttu-id="b9445-149">A Policy set definition objektum.</span><span class="sxs-lookup"><span data-stu-id="b9445-149">The policy set definition object.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment without parameters, Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy parameter string
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment with parameters via policy set parameter object, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9445-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="b9445-150">-Pre</span></span>
<span data-ttu-id="b9445-151">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="b9445-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b9445-152">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="b9445-152">-Scope</span></span>
<span data-ttu-id="b9445-153">A házirend hozzárendelésének hatókörét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9445-153">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="b9445-154">Ha például egy erőforrás-csoporthoz szeretne házirendet rendelni, adja meg az alábbiakat:</span><span class="sxs-lookup"><span data-stu-id="b9445-154">For instance, to assign a policy to a resource group, specify the following:</span></span>

<span data-ttu-id="b9445-155">`/subscriptions/`előfizetés-azonosító `/resourcegroups/` Erőforrás-csoport neve</span><span class="sxs-lookup"><span data-stu-id="b9445-155">`/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9445-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9445-156">-DefaultProfile</span></span>
<span data-ttu-id="b9445-157">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9445-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9445-158">-Leírás</span><span class="sxs-lookup"><span data-stu-id="b9445-158">-Description</span></span>
<span data-ttu-id="b9445-159">A házirend-hozzárendelés leírása.</span><span class="sxs-lookup"><span data-stu-id="b9445-159">The description for policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9445-160">-SKU</span><span class="sxs-lookup"><span data-stu-id="b9445-160">-Sku</span></span>
<span data-ttu-id="b9445-161">A SKU tulajdonságokat reprezentáló kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="b9445-161">A hash table which represents sku properties.</span></span> <span data-ttu-id="b9445-162">Alapértékek az ingyenes SKU-hoz: név = a0, Tier = ingyenes</span><span class="sxs-lookup"><span data-stu-id="b9445-162">Defaults to Free Sku: Name = A0, Tier = Free</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9445-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9445-163">CommonParameters</span></span>
<span data-ttu-id="b9445-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9445-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9445-165">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9445-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9445-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9445-166">INPUTS</span></span>

## <span data-ttu-id="b9445-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9445-167">OUTPUTS</span></span>

### <span data-ttu-id="b9445-168">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b9445-168">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b9445-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9445-169">NOTES</span></span>

## <span data-ttu-id="b9445-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9445-170">RELATED LINKS</span></span>

[<span data-ttu-id="b9445-171">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b9445-171">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="b9445-172">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b9445-172">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="b9445-173">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b9445-173">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="b9445-174">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b9445-174">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


