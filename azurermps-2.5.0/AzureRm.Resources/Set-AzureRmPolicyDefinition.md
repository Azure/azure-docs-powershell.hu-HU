---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicydefinition
schema: 2.0.0
ms.openlocfilehash: aa6687efb331cbb702ea36c53cc02cd77cefd45d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848638"
---
# <span data-ttu-id="f3638-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f3638-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="f3638-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3638-102">SYNOPSIS</span></span>
<span data-ttu-id="f3638-103">Módosította a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="f3638-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3638-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3638-104">SYNTAX</span></span>

### <span data-ttu-id="f3638-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f3638-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f3638-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3638-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f3638-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3638-107">SubscriptionIdParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f3638-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3638-108">IdParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f3638-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3638-109">DESCRIPTION</span></span>
<span data-ttu-id="f3638-110">A **set-AzureRmPolicyDefinition** parancsmag módosította a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="f3638-110">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="f3638-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f3638-111">EXAMPLES</span></span>

### <span data-ttu-id="f3638-112">Példa 1: házirend-definíció leírásának frissítése</span><span class="sxs-lookup"><span data-stu-id="f3638-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="f3638-113">Az első parancs az Get-AzureRmPolicyDefinition parancsmag használatával megkapja a VMPolicyDefinition nevű házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="f3638-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="f3638-114">A parancs az objektumot a $PolicyDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f3638-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="f3638-115">A második parancs frissíti a $PolicyDefinition **ResourceId** tulajdonsága által azonosított házirend-definíció leírását.</span><span class="sxs-lookup"><span data-stu-id="f3638-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="f3638-116">2. példa: házirend-definíciós mód frissítése</span><span class="sxs-lookup"><span data-stu-id="f3638-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="f3638-117">Ez a parancs frissíti a VMPolicyDefinition nevű házirend-definíciót a Set-AzureRmPolicyDefinition parancsmagot használva az "all" (mód) tulajdonság beállításához.</span><span class="sxs-lookup"><span data-stu-id="f3638-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzureRmPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

## <span data-ttu-id="f3638-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3638-118">PARAMETERS</span></span>

### <span data-ttu-id="f3638-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f3638-119">-ApiVersion</span></span>
<span data-ttu-id="f3638-120">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3638-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f3638-121">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="f3638-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f3638-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3638-122">-DefaultProfile</span></span>
<span data-ttu-id="f3638-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f3638-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3638-124">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f3638-124">-Description</span></span>
<span data-ttu-id="f3638-125">A házirend-definíció új leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3638-125">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="f3638-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f3638-126">-DisplayName</span></span>
<span data-ttu-id="f3638-127">A házirend-definíció új megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3638-127">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="f3638-128">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="f3638-128">-Id</span></span>
<span data-ttu-id="f3638-129">Annak a házirend-definíciónak a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="f3638-129">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f3638-130">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f3638-130">-InformationAction</span></span>
<span data-ttu-id="f3638-131">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="f3638-131">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="f3638-132">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f3638-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f3638-133">Folytassa</span><span class="sxs-lookup"><span data-stu-id="f3638-133">Continue</span></span>
- <span data-ttu-id="f3638-134">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="f3638-134">Ignore</span></span>
- <span data-ttu-id="f3638-135">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="f3638-135">Inquire</span></span>
- <span data-ttu-id="f3638-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f3638-136">SilentlyContinue</span></span>
- <span data-ttu-id="f3638-137">állj</span><span class="sxs-lookup"><span data-stu-id="f3638-137">Stop</span></span>
- <span data-ttu-id="f3638-138">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="f3638-138">Suspend</span></span>

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

### <span data-ttu-id="f3638-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f3638-139">-InformationVariable</span></span>
<span data-ttu-id="f3638-140">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="f3638-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f3638-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="f3638-141">-ManagementGroupName</span></span>
<span data-ttu-id="f3638-142">A frissítendő házirend-definíció felügyeleti csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="f3638-142">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="f3638-143">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f3638-143">-Metadata</span></span>
<span data-ttu-id="f3638-144">A házirend-definíció metaadatai.</span><span class="sxs-lookup"><span data-stu-id="f3638-144">The metadata for policy definition.</span></span> <span data-ttu-id="f3638-145">Ez lehet a metaadatokat tartalmazó fájlnév vagy a metaadatok karakterláncként való elérési útja.</span><span class="sxs-lookup"><span data-stu-id="f3638-145">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="f3638-146">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="f3638-146">-Mode</span></span>
<span data-ttu-id="f3638-147">Az új házirend-definíció üzemmódja.</span><span class="sxs-lookup"><span data-stu-id="f3638-147">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="f3638-148">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f3638-148">-Name</span></span>
<span data-ttu-id="f3638-149">Annak a házirend-definíciónak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="f3638-149">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f3638-150">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="f3638-150">-Parameter</span></span>
<span data-ttu-id="f3638-151">A Parameters deklaráció a házirend-definícióban.</span><span class="sxs-lookup"><span data-stu-id="f3638-151">The parameters declaration for policy definition.</span></span> <span data-ttu-id="f3638-152">Ez lehet elérési út a Parameters deklarációt tartalmazó fájlnév vagy URI-azonosítóhoz, illetve a Parameters deklaráció karakterláncként való eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="f3638-152">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="f3638-153">-Házirend</span><span class="sxs-lookup"><span data-stu-id="f3638-153">-Policy</span></span>
<span data-ttu-id="f3638-154">A házirend-definíció új házirend-szabályát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3638-154">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="f3638-155">Megadhatja a. JSON fájlok elérési útját, vagy a házirendet a JavaScript-objektum formátumban (JSON) tartalmazó karakterláncban.</span><span class="sxs-lookup"><span data-stu-id="f3638-155">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="f3638-156">-Pre</span><span class="sxs-lookup"><span data-stu-id="f3638-156">-Pre</span></span>
<span data-ttu-id="f3638-157">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="f3638-157">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f3638-158">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f3638-158">-SubscriptionId</span></span>
<span data-ttu-id="f3638-159">A frissítendő házirend-definíció előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f3638-159">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="f3638-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3638-160">CommonParameters</span></span>
<span data-ttu-id="f3638-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3638-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3638-162">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3638-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3638-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3638-163">INPUTS</span></span>

## <span data-ttu-id="f3638-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3638-164">OUTPUTS</span></span>

## <span data-ttu-id="f3638-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3638-165">NOTES</span></span>

## <span data-ttu-id="f3638-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3638-166">RELATED LINKS</span></span>

[<span data-ttu-id="f3638-167">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f3638-167">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="f3638-168">Új – AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f3638-168">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="f3638-169">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f3638-169">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


