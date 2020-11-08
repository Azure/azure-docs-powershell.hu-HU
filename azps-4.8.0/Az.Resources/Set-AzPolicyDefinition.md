---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: 3aed403965bc48a26044b930fdf5cc9e9a93bbbe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181410"
---
# <span data-ttu-id="865f0-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="865f0-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="865f0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="865f0-102">SYNOPSIS</span></span>
<span data-ttu-id="865f0-103">Módosította a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="865f0-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="865f0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="865f0-104">SYNTAX</span></span>

### <span data-ttu-id="865f0-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="865f0-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="865f0-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="865f0-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="865f0-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="865f0-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="865f0-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="865f0-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="865f0-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="865f0-109">InputObjectParameterSet</span></span>
```
Set-AzPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>] [-Metadata <String>]
 [-Parameter <String>] [-Mode <String>] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="865f0-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="865f0-110">DESCRIPTION</span></span>
<span data-ttu-id="865f0-111">A **set-AzPolicyDefinition** parancsmag módosította a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="865f0-111">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="865f0-112">Példák</span><span class="sxs-lookup"><span data-stu-id="865f0-112">EXAMPLES</span></span>

### <span data-ttu-id="865f0-113">Példa 1: házirend-definíció leírásának frissítése</span><span class="sxs-lookup"><span data-stu-id="865f0-113">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="865f0-114">Az első parancs az Get-AzPolicyDefinition parancsmag használatával megkapja a VMPolicyDefinition nevű házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="865f0-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="865f0-115">A parancs az objektumot a $PolicyDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="865f0-115">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="865f0-116">A második parancs frissíti a $PolicyDefinition **ResourceId** tulajdonsága által azonosított házirend-definíció leírását.</span><span class="sxs-lookup"><span data-stu-id="865f0-116">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="865f0-117">2. példa: házirend-definíciós mód frissítése</span><span class="sxs-lookup"><span data-stu-id="865f0-117">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="865f0-118">Ez a parancs frissíti a VMPolicyDefinition nevű házirend-definíciót a Set-AzPolicyDefinition parancsmagot használva az "all" (mód) tulajdonság beállításához.</span><span class="sxs-lookup"><span data-stu-id="865f0-118">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="865f0-119">3. példa: egy házirend-definíció metaadatait frissíti</span><span class="sxs-lookup"><span data-stu-id="865f0-119">Example 3: Update the metadata of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="865f0-120">Ez a parancs frissíti a VMPolicyDefinition nevű házirend-definíció metaadatait, így jelezve, hogy a kategóriája "virtuális gép".</span><span class="sxs-lookup"><span data-stu-id="865f0-120">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="865f0-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="865f0-121">PARAMETERS</span></span>

### <span data-ttu-id="865f0-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="865f0-122">-ApiVersion</span></span>
<span data-ttu-id="865f0-123">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="865f0-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="865f0-124">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="865f0-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="865f0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="865f0-125">-DefaultProfile</span></span>
<span data-ttu-id="865f0-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="865f0-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="865f0-127">-Leírás</span><span class="sxs-lookup"><span data-stu-id="865f0-127">-Description</span></span>
<span data-ttu-id="865f0-128">A házirend-definíció új leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="865f0-128">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="865f0-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="865f0-129">-DisplayName</span></span>
<span data-ttu-id="865f0-130">A házirend-definíció új megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="865f0-130">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="865f0-131">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="865f0-131">-Id</span></span>
<span data-ttu-id="865f0-132">Annak a házirend-definíciónak a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="865f0-132">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="865f0-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="865f0-133">-InputObject</span></span>
<span data-ttu-id="865f0-134">A házirend-definíciós objektum, amely egy másik parancsmagból származó kimenetet frissít.</span><span class="sxs-lookup"><span data-stu-id="865f0-134">The policy definition object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="865f0-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="865f0-135">-ManagementGroupName</span></span>
<span data-ttu-id="865f0-136">A frissítendő házirend-definíció felügyeleti csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="865f0-136">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="865f0-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="865f0-137">-Metadata</span></span>
<span data-ttu-id="865f0-138">A házirend-definíció metaadatai.</span><span class="sxs-lookup"><span data-stu-id="865f0-138">The metadata for policy definition.</span></span> <span data-ttu-id="865f0-139">Ez lehet a metaadatokat tartalmazó fájlnév vagy a metaadatok karakterláncként való elérési útja.</span><span class="sxs-lookup"><span data-stu-id="865f0-139">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="865f0-140">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="865f0-140">-Mode</span></span>
<span data-ttu-id="865f0-141">Az új házirend-definíció üzemmódja.</span><span class="sxs-lookup"><span data-stu-id="865f0-141">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="865f0-142">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="865f0-142">-Name</span></span>
<span data-ttu-id="865f0-143">Annak a házirend-definíciónak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="865f0-143">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="865f0-144">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="865f0-144">-Parameter</span></span>
<span data-ttu-id="865f0-145">A Parameters deklaráció a házirend-definícióban.</span><span class="sxs-lookup"><span data-stu-id="865f0-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="865f0-146">Ez lehet elérési út a Parameters deklarációt tartalmazó fájlnév vagy URI-azonosítóhoz, illetve a Parameters deklaráció karakterláncként való eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="865f0-146">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="865f0-147">-Házirend</span><span class="sxs-lookup"><span data-stu-id="865f0-147">-Policy</span></span>
<span data-ttu-id="865f0-148">A házirend-definíció új házirend-szabályát adja meg.</span><span class="sxs-lookup"><span data-stu-id="865f0-148">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="865f0-149">Megadhatja a. JSON fájlok elérési útját, vagy a házirendet a JavaScript-objektum formátumban (JSON) tartalmazó karakterláncban.</span><span class="sxs-lookup"><span data-stu-id="865f0-149">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="865f0-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="865f0-150">-Pre</span></span>
<span data-ttu-id="865f0-151">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="865f0-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="865f0-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="865f0-152">-SubscriptionId</span></span>
<span data-ttu-id="865f0-153">A frissítendő házirend-definíció előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="865f0-153">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="865f0-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="865f0-154">CommonParameters</span></span>
<span data-ttu-id="865f0-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="865f0-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="865f0-156">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="865f0-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="865f0-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="865f0-157">INPUTS</span></span>

### <span data-ttu-id="865f0-158">System. String</span><span class="sxs-lookup"><span data-stu-id="865f0-158">System.String</span></span>

### <span data-ttu-id="865f0-159">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="865f0-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="865f0-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="865f0-160">OUTPUTS</span></span>

### <span data-ttu-id="865f0-161">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="865f0-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="865f0-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="865f0-162">NOTES</span></span>

## <span data-ttu-id="865f0-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="865f0-163">RELATED LINKS</span></span>

[<span data-ttu-id="865f0-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="865f0-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="865f0-165">Új – AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="865f0-165">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="865f0-166">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="865f0-166">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


