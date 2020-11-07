---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicydefinition
schema: 2.0.0
ms.openlocfilehash: 5bd650583a933ba8d7ea56762c918d386b630c6c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849521"
---
# <span data-ttu-id="d9d58-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d9d58-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="d9d58-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d9d58-102">SYNOPSIS</span></span>
<span data-ttu-id="d9d58-103">Házirend-definíciókat kap.</span><span class="sxs-lookup"><span data-stu-id="d9d58-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9d58-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d9d58-104">SYNTAX</span></span>

### <span data-ttu-id="d9d58-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d9d58-105">NameParameterSet (Default)</span></span>
```
Get-AzureRmPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d9d58-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9d58-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d9d58-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9d58-107">SubscriptionIdParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d9d58-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9d58-108">IdParameterSet</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d9d58-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9d58-109">BuiltinFilterParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d9d58-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9d58-110">CustomFilterParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d9d58-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="d9d58-111">DESCRIPTION</span></span>
<span data-ttu-id="d9d58-112">A **Get-AzureRmPolicyDefinition** parancsmag egy név vagy azonosító szerint azonosított házirend-definíciók vagy konkrét házirend-definíció gyűjteményét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d9d58-112">The **Get-AzureRmPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="d9d58-113">Példák</span><span class="sxs-lookup"><span data-stu-id="d9d58-113">EXAMPLES</span></span>

### <span data-ttu-id="d9d58-114">Példa 1: az összes házirend-definíció beolvasása</span><span class="sxs-lookup"><span data-stu-id="d9d58-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition
```

<span data-ttu-id="d9d58-115">Ez a parancs az összes házirend-definíciót megkapja.</span><span class="sxs-lookup"><span data-stu-id="d9d58-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="d9d58-116">2. példa: házirend-definíció beolvasása az aktuális előfizetésből név szerint</span><span class="sxs-lookup"><span data-stu-id="d9d58-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="d9d58-117">Ez a parancs az aktuális alapértelmezett előfizetésből a VMPolicyDefinition nevű házirend-definíciót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d9d58-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="d9d58-118">3. példa: házirend-definíció beolvasása a kezelés csoportból név szerint</span><span class="sxs-lookup"><span data-stu-id="d9d58-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="d9d58-119">Ez a parancs a VMPolicyDefinition nevű házirend-definíciót a Dept42 nevű felügyeleti csoporttól kapja.</span><span class="sxs-lookup"><span data-stu-id="d9d58-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="d9d58-120">Példa 4: a beépített házirend-definíciók beszerzése az előfizetésből</span><span class="sxs-lookup"><span data-stu-id="d9d58-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="d9d58-121">Ez a parancs a beépített házirend-definíciókat az előfizetés 3bf44b72-c631-427a-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="d9d58-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

## <span data-ttu-id="d9d58-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d9d58-122">PARAMETERS</span></span>

### <span data-ttu-id="d9d58-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d9d58-123">-ApiVersion</span></span>
<span data-ttu-id="d9d58-124">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9d58-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d9d58-125">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="d9d58-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d9d58-126">-Beépített</span><span class="sxs-lookup"><span data-stu-id="d9d58-126">-Builtin</span></span>
<span data-ttu-id="d9d58-127">Az eredmények listáját csak a beépített házirend-definíciókkal korlátozhatja.</span><span class="sxs-lookup"><span data-stu-id="d9d58-127">Limits list of results to only built-in policy definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BuiltinFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9d58-128">-Custom</span><span class="sxs-lookup"><span data-stu-id="d9d58-128">-Custom</span></span>
<span data-ttu-id="d9d58-129">Az eredmények listáját csak az egyéni házirend-definíciók szerint korlátozhatja.</span><span class="sxs-lookup"><span data-stu-id="d9d58-129">Limits list of results to only custom policy definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CustomFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9d58-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9d58-130">-DefaultProfile</span></span>
<span data-ttu-id="d9d58-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d9d58-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9d58-132">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="d9d58-132">-Id</span></span>
<span data-ttu-id="d9d58-133">Annak a házirend-definíciónak a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="d9d58-133">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d9d58-134">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d9d58-134">-InformationAction</span></span>
<span data-ttu-id="d9d58-135">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="d9d58-135">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="d9d58-136">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d9d58-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d9d58-137">Folytassa</span><span class="sxs-lookup"><span data-stu-id="d9d58-137">Continue</span></span>
- <span data-ttu-id="d9d58-138">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="d9d58-138">Ignore</span></span>
- <span data-ttu-id="d9d58-139">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="d9d58-139">Inquire</span></span>
- <span data-ttu-id="d9d58-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d9d58-140">SilentlyContinue</span></span>
- <span data-ttu-id="d9d58-141">állj</span><span class="sxs-lookup"><span data-stu-id="d9d58-141">Stop</span></span>
- <span data-ttu-id="d9d58-142">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="d9d58-142">Suspend</span></span>

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

### <span data-ttu-id="d9d58-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d9d58-143">-InformationVariable</span></span>
<span data-ttu-id="d9d58-144">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="d9d58-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d9d58-145">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="d9d58-145">-ManagementGroupName</span></span>
<span data-ttu-id="d9d58-146">A beolvasott házirend-definíció (ok) kezelési csoportjának a neve.</span><span class="sxs-lookup"><span data-stu-id="d9d58-146">The name of the management group of the policy definition(s) to get.</span></span>

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

```yaml
Type: System.String
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9d58-147">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d9d58-147">-Name</span></span>
<span data-ttu-id="d9d58-148">Annak a házirend-definíciónak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="d9d58-148">Specifies the name of the policy definition that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9d58-149">-Pre</span><span class="sxs-lookup"><span data-stu-id="d9d58-149">-Pre</span></span>
<span data-ttu-id="d9d58-150">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="d9d58-150">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d9d58-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d9d58-151">-SubscriptionId</span></span>
<span data-ttu-id="d9d58-152">A házirend-definíció (ok) előfizetési azonosítója a beszerzéshez.</span><span class="sxs-lookup"><span data-stu-id="d9d58-152">The subscription ID of the policy definition(s) to get.</span></span>

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

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9d58-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9d58-153">CommonParameters</span></span>
<span data-ttu-id="d9d58-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d9d58-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9d58-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9d58-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9d58-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9d58-156">INPUTS</span></span>

## <span data-ttu-id="d9d58-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9d58-157">OUTPUTS</span></span>

## <span data-ttu-id="d9d58-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d9d58-158">NOTES</span></span>

## <span data-ttu-id="d9d58-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9d58-159">RELATED LINKS</span></span>

[<span data-ttu-id="d9d58-160">Új – AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d9d58-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="d9d58-161">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d9d58-161">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="d9d58-162">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d9d58-162">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


