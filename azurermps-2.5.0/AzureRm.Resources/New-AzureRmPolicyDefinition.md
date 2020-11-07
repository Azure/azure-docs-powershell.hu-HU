---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicydefinition
schema: 2.0.0
ms.openlocfilehash: 844c4d6af4d5ea0b11f0ae3e662bd2ba91957c1d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850261"
---
# <span data-ttu-id="8268c-101">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8268c-101">New-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="8268c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8268c-102">SYNOPSIS</span></span>
<span data-ttu-id="8268c-103">Házirend-definíciót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8268c-103">Creates a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8268c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8268c-104">SYNTAX</span></span>

### <span data-ttu-id="8268c-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8268c-105">NameParameterSet (Default)</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8268c-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8268c-106">ManagementGroupNameParameterSet</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8268c-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8268c-107">SubscriptionIdParameterSet</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8268c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8268c-108">DESCRIPTION</span></span>
<span data-ttu-id="8268c-109">A **New-AzureRmPolicyDefinition** parancsmag olyan házirend-definíciót hoz létre, amely egy JavaScript-objektum formátumú (JSON) formátumú házirend-szabályt tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="8268c-109">The **New-AzureRmPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="8268c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8268c-110">EXAMPLES</span></span>

### <span data-ttu-id="8268c-111">Példa 1: házirend-definíció létrehozása házirendfájl használatával</span><span class="sxs-lookup"><span data-stu-id="8268c-111">Example 1: Create a policy definition by using a policy file</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": ["eastus", "westus", "centralus"]
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzureRmPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json
```

<span data-ttu-id="8268c-112">Ez a parancs létrehoz egy LocationDefinition nevű házirend-definíciót, amely a C:\LocationPolicy.jsban megadott házirend-szabályt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8268c-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="8268c-113">A fenti LocationPolicy.jspéldául a fájlhoz tartozó tartalmakat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8268c-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="8268c-114">2. példa: paraméteres házirend-definíció létrehozása szövegközi paraméterek használatával</span><span class="sxs-lookup"><span data-stu-id="8268c-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": "[parameters('listOfAllowedLocations')]"
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzureRmPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json -Parameter '{ "listOfAllowedLocations": { "type": "array" } }'
```

<span data-ttu-id="8268c-115">Ez a parancs létrehoz egy LocationDefinition nevű házirend-definíciót, amely a C:\LocationPolicy.jsban megadott házirend-szabályt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8268c-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="8268c-116">A házirend-szabály paraméter-definíciója szövegközi módon van megadva.</span><span class="sxs-lookup"><span data-stu-id="8268c-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="8268c-117">3. példa: házirend-definíció létrehozása egy felügyeleti csoportban</span><span class="sxs-lookup"><span data-stu-id="8268c-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="8268c-118">Ez a parancs létrehoz egy VMPolicyDefinition nevű házirend-definíciót a felügyeleti csoport Dept42.</span><span class="sxs-lookup"><span data-stu-id="8268c-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="8268c-119">A parancs érvényes JSON formátumú karakterláncként adja meg a házirendet.</span><span class="sxs-lookup"><span data-stu-id="8268c-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="8268c-120">Példa 4: házirend-definíció létrehozása a metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="8268c-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"Category":"Virtual Machine"}' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="8268c-121">Ez a parancs létrehoz egy VMPolicyDefinition nevű házirend-definíciót, amelyben a kategóriája "virtuális gép".</span><span class="sxs-lookup"><span data-stu-id="8268c-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="8268c-122">A parancs érvényes JSON formátumú karakterláncként adja meg a házirendet.</span><span class="sxs-lookup"><span data-stu-id="8268c-122">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="8268c-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8268c-123">PARAMETERS</span></span>

### <span data-ttu-id="8268c-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8268c-124">-ApiVersion</span></span>
<span data-ttu-id="8268c-125">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8268c-125">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8268c-126">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="8268c-126">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8268c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8268c-127">-DefaultProfile</span></span>
<span data-ttu-id="8268c-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8268c-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8268c-129">-Leírás</span><span class="sxs-lookup"><span data-stu-id="8268c-129">-Description</span></span>
<span data-ttu-id="8268c-130">A házirend definíciójának leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="8268c-130">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="8268c-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8268c-131">-DisplayName</span></span>
<span data-ttu-id="8268c-132">A házirend-definíció megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8268c-132">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="8268c-133">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8268c-133">-InformationAction</span></span>
<span data-ttu-id="8268c-134">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="8268c-134">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="8268c-135">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8268c-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8268c-136">Folytassa</span><span class="sxs-lookup"><span data-stu-id="8268c-136">Continue</span></span>
- <span data-ttu-id="8268c-137">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="8268c-137">Ignore</span></span>
- <span data-ttu-id="8268c-138">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="8268c-138">Inquire</span></span>
- <span data-ttu-id="8268c-139">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8268c-139">SilentlyContinue</span></span>
- <span data-ttu-id="8268c-140">állj</span><span class="sxs-lookup"><span data-stu-id="8268c-140">Stop</span></span>
- <span data-ttu-id="8268c-141">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="8268c-141">Suspend</span></span>

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

### <span data-ttu-id="8268c-142">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8268c-142">-InformationVariable</span></span>
<span data-ttu-id="8268c-143">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="8268c-143">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8268c-144">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="8268c-144">-ManagementGroupName</span></span>
<span data-ttu-id="8268c-145">Az új házirend-definíció felügyeleti csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="8268c-145">The name of the management group of the new policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8268c-146">-Metadata</span><span class="sxs-lookup"><span data-stu-id="8268c-146">-Metadata</span></span>
<span data-ttu-id="8268c-147">A házirend-definíció metaadatai.</span><span class="sxs-lookup"><span data-stu-id="8268c-147">The metadata for policy definition.</span></span> <span data-ttu-id="8268c-148">Ez lehet a metaadatot tartalmazó fájlnév vagy a metaadat karakterláncként való elérési útja.</span><span class="sxs-lookup"><span data-stu-id="8268c-148">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="8268c-149">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="8268c-149">-Mode</span></span>
<span data-ttu-id="8268c-150">A házirend-definíció módja</span><span class="sxs-lookup"><span data-stu-id="8268c-150">The mode of the policy definition</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyDefinitionMode]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8268c-151">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8268c-151">-Name</span></span>
<span data-ttu-id="8268c-152">A házirend-definíció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8268c-152">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="8268c-153">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="8268c-153">-Parameter</span></span>
<span data-ttu-id="8268c-154">A Parameters deklaráció a házirend-definícióban.</span><span class="sxs-lookup"><span data-stu-id="8268c-154">The parameters declaration for policy definition.</span></span> <span data-ttu-id="8268c-155">Ez lehet a Parameters deklarációt vagy a Parameters deklarációt karakterláncként tartalmazó fájlnév elérési útja.</span><span class="sxs-lookup"><span data-stu-id="8268c-155">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="8268c-156">-Házirend</span><span class="sxs-lookup"><span data-stu-id="8268c-156">-Policy</span></span>
<span data-ttu-id="8268c-157">A házirend-definíció szabályait adja meg.</span><span class="sxs-lookup"><span data-stu-id="8268c-157">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="8268c-158">Megadhatja a. JSON fájlok elérési útját vagy a JSON formátumú házirendet tartalmazó karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="8268c-158">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="8268c-159">-Pre</span><span class="sxs-lookup"><span data-stu-id="8268c-159">-Pre</span></span>
<span data-ttu-id="8268c-160">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="8268c-160">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8268c-161">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8268c-161">-SubscriptionId</span></span>
<span data-ttu-id="8268c-162">Az új házirend-definíció előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8268c-162">The subscription ID of the new policy definition.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8268c-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8268c-163">CommonParameters</span></span>
<span data-ttu-id="8268c-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8268c-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8268c-165">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8268c-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8268c-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8268c-166">INPUTS</span></span>

## <span data-ttu-id="8268c-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8268c-167">OUTPUTS</span></span>

## <span data-ttu-id="8268c-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8268c-168">NOTES</span></span>

## <span data-ttu-id="8268c-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8268c-169">RELATED LINKS</span></span>

[<span data-ttu-id="8268c-170">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8268c-170">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="8268c-171">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8268c-171">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="8268c-172">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8268c-172">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


