---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: 9f6f23babc1dfaf947a7eb8cea88011ff184cce7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011737"
---
# <span data-ttu-id="6617b-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6617b-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="6617b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6617b-102">SYNOPSIS</span></span>
<span data-ttu-id="6617b-103">Módosította a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="6617b-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="6617b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6617b-104">SYNTAX</span></span>

### <span data-ttu-id="6617b-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6617b-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6617b-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6617b-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6617b-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6617b-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6617b-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6617b-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6617b-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="6617b-109">DESCRIPTION</span></span>
<span data-ttu-id="6617b-110">A **set-AzPolicyDefinition** parancsmag módosította a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="6617b-110">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="6617b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6617b-111">EXAMPLES</span></span>

### <span data-ttu-id="6617b-112">Példa 1: házirend-definíció leírásának frissítése</span><span class="sxs-lookup"><span data-stu-id="6617b-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="6617b-113">Az első parancs az Get-AzPolicyDefinition parancsmag használatával megkapja a VMPolicyDefinition nevű házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="6617b-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="6617b-114">A parancs az objektumot a $PolicyDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="6617b-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="6617b-115">A második parancs frissíti a $PolicyDefinition **ResourceId** tulajdonsága által azonosított házirend-definíció leírását.</span><span class="sxs-lookup"><span data-stu-id="6617b-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="6617b-116">2. példa: házirend-definíciós mód frissítése</span><span class="sxs-lookup"><span data-stu-id="6617b-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="6617b-117">Ez a parancs frissíti a VMPolicyDefinition nevű házirend-definíciót a Set-AzPolicyDefinition parancsmagot használva az "all" (mód) tulajdonság beállításához.</span><span class="sxs-lookup"><span data-stu-id="6617b-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="6617b-118">3. példa: egy házirend-definíció metaadatait frissíti</span><span class="sxs-lookup"><span data-stu-id="6617b-118">Example 3: Update the metadata of a policy definition</span></span>
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

<span data-ttu-id="6617b-119">Ez a parancs frissíti a VMPolicyDefinition nevű házirend-definíció metaadatait, így jelezve, hogy a kategóriája "virtuális gép".</span><span class="sxs-lookup"><span data-stu-id="6617b-119">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="6617b-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6617b-120">PARAMETERS</span></span>

### <span data-ttu-id="6617b-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6617b-121">-ApiVersion</span></span>
<span data-ttu-id="6617b-122">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6617b-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6617b-123">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="6617b-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6617b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6617b-124">-DefaultProfile</span></span>
<span data-ttu-id="6617b-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6617b-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6617b-126">-Leírás</span><span class="sxs-lookup"><span data-stu-id="6617b-126">-Description</span></span>
<span data-ttu-id="6617b-127">A házirend-definíció új leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="6617b-127">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="6617b-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6617b-128">-DisplayName</span></span>
<span data-ttu-id="6617b-129">A házirend-definíció új megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6617b-129">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="6617b-130">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="6617b-130">-Id</span></span>
<span data-ttu-id="6617b-131">Annak a házirend-definíciónak a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="6617b-131">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6617b-132">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="6617b-132">-ManagementGroupName</span></span>
<span data-ttu-id="6617b-133">A frissítendő házirend-definíció felügyeleti csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="6617b-133">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="6617b-134">-Metadata</span><span class="sxs-lookup"><span data-stu-id="6617b-134">-Metadata</span></span>
<span data-ttu-id="6617b-135">A házirend-definíció metaadatai.</span><span class="sxs-lookup"><span data-stu-id="6617b-135">The metadata for policy definition.</span></span> <span data-ttu-id="6617b-136">Ez lehet a metaadatokat tartalmazó fájlnév vagy a metaadatok karakterláncként való elérési útja.</span><span class="sxs-lookup"><span data-stu-id="6617b-136">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="6617b-137">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="6617b-137">-Mode</span></span>
<span data-ttu-id="6617b-138">Az új házirend-definíció üzemmódja.</span><span class="sxs-lookup"><span data-stu-id="6617b-138">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="6617b-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6617b-139">-Name</span></span>
<span data-ttu-id="6617b-140">Annak a házirend-definíciónak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="6617b-140">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6617b-141">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="6617b-141">-Parameter</span></span>
<span data-ttu-id="6617b-142">A Parameters deklaráció a házirend-definícióban.</span><span class="sxs-lookup"><span data-stu-id="6617b-142">The parameters declaration for policy definition.</span></span> <span data-ttu-id="6617b-143">Ez lehet elérési út a Parameters deklarációt tartalmazó fájlnév vagy URI-azonosítóhoz, illetve a Parameters deklaráció karakterláncként való eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="6617b-143">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="6617b-144">-Házirend</span><span class="sxs-lookup"><span data-stu-id="6617b-144">-Policy</span></span>
<span data-ttu-id="6617b-145">A házirend-definíció új házirend-szabályát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6617b-145">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="6617b-146">Megadhatja a. JSON fájlok elérési útját, vagy a házirendet a JavaScript-objektum formátumban (JSON) tartalmazó karakterláncban.</span><span class="sxs-lookup"><span data-stu-id="6617b-146">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="6617b-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="6617b-147">-Pre</span></span>
<span data-ttu-id="6617b-148">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="6617b-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6617b-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6617b-149">-SubscriptionId</span></span>
<span data-ttu-id="6617b-150">A frissítendő házirend-definíció előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6617b-150">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="6617b-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6617b-151">CommonParameters</span></span>
<span data-ttu-id="6617b-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6617b-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6617b-153">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6617b-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6617b-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6617b-154">INPUTS</span></span>

### <span data-ttu-id="6617b-155">System. String</span><span class="sxs-lookup"><span data-stu-id="6617b-155">System.String</span></span>

### <span data-ttu-id="6617b-156">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6617b-156">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6617b-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6617b-157">OUTPUTS</span></span>

### <span data-ttu-id="6617b-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="6617b-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6617b-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6617b-159">NOTES</span></span>

## <span data-ttu-id="6617b-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6617b-160">RELATED LINKS</span></span>

[<span data-ttu-id="6617b-161">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6617b-161">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="6617b-162">Új – AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6617b-162">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="6617b-163">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6617b-163">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


