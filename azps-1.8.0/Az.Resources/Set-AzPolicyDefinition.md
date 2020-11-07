---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: f96ea5b7f36806378dff31cc81d211074638342c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669315"
---
# <span data-ttu-id="041d9-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="041d9-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="041d9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="041d9-102">SYNOPSIS</span></span>
<span data-ttu-id="041d9-103">Módosította a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="041d9-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="041d9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="041d9-104">SYNTAX</span></span>

### <span data-ttu-id="041d9-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="041d9-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="041d9-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="041d9-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="041d9-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="041d9-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="041d9-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="041d9-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="041d9-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="041d9-109">DESCRIPTION</span></span>
<span data-ttu-id="041d9-110">A **set-AzPolicyDefinition** parancsmag módosította a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="041d9-110">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="041d9-111">Példák</span><span class="sxs-lookup"><span data-stu-id="041d9-111">EXAMPLES</span></span>

### <span data-ttu-id="041d9-112">Példa 1: házirend-definíció leírásának frissítése</span><span class="sxs-lookup"><span data-stu-id="041d9-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="041d9-113">Az első parancs az Get-AzPolicyDefinition parancsmag használatával megkapja a VMPolicyDefinition nevű házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="041d9-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="041d9-114">A parancs az objektumot a $PolicyDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="041d9-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="041d9-115">A második parancs frissíti a $PolicyDefinition **ResourceId** tulajdonsága által azonosított házirend-definíció leírását.</span><span class="sxs-lookup"><span data-stu-id="041d9-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="041d9-116">2. példa: házirend-definíciós mód frissítése</span><span class="sxs-lookup"><span data-stu-id="041d9-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="041d9-117">Ez a parancs frissíti a VMPolicyDefinition nevű házirend-definíciót a Set-AzPolicyDefinition parancsmagot használva az "all" (mód) tulajdonság beállításához.</span><span class="sxs-lookup"><span data-stu-id="041d9-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

## <span data-ttu-id="041d9-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="041d9-118">PARAMETERS</span></span>

### <span data-ttu-id="041d9-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="041d9-119">-ApiVersion</span></span>
<span data-ttu-id="041d9-120">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="041d9-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="041d9-121">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="041d9-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="041d9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="041d9-122">-DefaultProfile</span></span>
<span data-ttu-id="041d9-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="041d9-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="041d9-124">-Leírás</span><span class="sxs-lookup"><span data-stu-id="041d9-124">-Description</span></span>
<span data-ttu-id="041d9-125">A házirend-definíció új leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="041d9-125">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="041d9-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="041d9-126">-DisplayName</span></span>
<span data-ttu-id="041d9-127">A házirend-definíció új megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="041d9-127">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="041d9-128">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="041d9-128">-Id</span></span>
<span data-ttu-id="041d9-129">Annak a házirend-definíciónak a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="041d9-129">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="041d9-130">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="041d9-130">-ManagementGroupName</span></span>
<span data-ttu-id="041d9-131">A frissítendő házirend-definíció felügyeleti csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="041d9-131">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="041d9-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="041d9-132">-Metadata</span></span>
<span data-ttu-id="041d9-133">A házirend-definíció metaadatai.</span><span class="sxs-lookup"><span data-stu-id="041d9-133">The metadata for policy definition.</span></span> <span data-ttu-id="041d9-134">Ez lehet a metaadatokat tartalmazó fájlnév vagy a metaadatok karakterláncként való elérési útja.</span><span class="sxs-lookup"><span data-stu-id="041d9-134">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="041d9-135">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="041d9-135">-Mode</span></span>
<span data-ttu-id="041d9-136">Az új házirend-definíció üzemmódja.</span><span class="sxs-lookup"><span data-stu-id="041d9-136">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="041d9-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="041d9-137">-Name</span></span>
<span data-ttu-id="041d9-138">Annak a házirend-definíciónak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="041d9-138">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="041d9-139">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="041d9-139">-Parameter</span></span>
<span data-ttu-id="041d9-140">A Parameters deklaráció a házirend-definícióban.</span><span class="sxs-lookup"><span data-stu-id="041d9-140">The parameters declaration for policy definition.</span></span> <span data-ttu-id="041d9-141">Ez lehet elérési út a Parameters deklarációt tartalmazó fájlnév vagy URI-azonosítóhoz, illetve a Parameters deklaráció karakterláncként való eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="041d9-141">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="041d9-142">-Házirend</span><span class="sxs-lookup"><span data-stu-id="041d9-142">-Policy</span></span>
<span data-ttu-id="041d9-143">A házirend-definíció új házirend-szabályát adja meg.</span><span class="sxs-lookup"><span data-stu-id="041d9-143">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="041d9-144">Megadhatja a. JSON fájlok elérési útját, vagy a házirendet a JavaScript-objektum formátumban (JSON) tartalmazó karakterláncban.</span><span class="sxs-lookup"><span data-stu-id="041d9-144">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="041d9-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="041d9-145">-Pre</span></span>
<span data-ttu-id="041d9-146">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="041d9-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="041d9-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="041d9-147">-SubscriptionId</span></span>
<span data-ttu-id="041d9-148">A frissítendő házirend-definíció előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="041d9-148">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="041d9-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="041d9-149">CommonParameters</span></span>
<span data-ttu-id="041d9-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="041d9-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="041d9-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="041d9-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="041d9-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="041d9-152">INPUTS</span></span>

### <span data-ttu-id="041d9-153">System. String</span><span class="sxs-lookup"><span data-stu-id="041d9-153">System.String</span></span>

### <span data-ttu-id="041d9-154">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="041d9-154">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="041d9-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="041d9-155">OUTPUTS</span></span>

### <span data-ttu-id="041d9-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="041d9-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="041d9-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="041d9-157">NOTES</span></span>

## <span data-ttu-id="041d9-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="041d9-158">RELATED LINKS</span></span>

[<span data-ttu-id="041d9-159">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="041d9-159">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="041d9-160">Új – AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="041d9-160">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="041d9-161">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="041d9-161">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


