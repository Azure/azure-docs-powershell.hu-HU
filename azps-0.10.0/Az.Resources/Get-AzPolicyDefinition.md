---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicyDefinition.md
ms.openlocfilehash: 66901872a6a7c3e871ce95287b45966aee974b52
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843434"
---
# <span data-ttu-id="dd785-101">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dd785-101">Get-AzPolicyDefinition</span></span>

## <span data-ttu-id="dd785-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd785-102">SYNOPSIS</span></span>
<span data-ttu-id="dd785-103">Házirend-definíciókat kap.</span><span class="sxs-lookup"><span data-stu-id="dd785-103">Gets policy definitions.</span></span>

## <span data-ttu-id="dd785-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd785-104">SYNTAX</span></span>

### <span data-ttu-id="dd785-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dd785-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="dd785-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd785-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="dd785-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd785-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="dd785-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd785-108">IdParameterSet</span></span>
```
Get-AzPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="dd785-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd785-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="dd785-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd785-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="dd785-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd785-111">DESCRIPTION</span></span>
<span data-ttu-id="dd785-112">A **Get-AzPolicyDefinition** parancsmag egy név vagy azonosító szerint azonosított házirend-definíciók vagy konkrét házirend-definíció gyűjteményét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="dd785-112">The **Get-AzPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="dd785-113">Példák</span><span class="sxs-lookup"><span data-stu-id="dd785-113">EXAMPLES</span></span>

### <span data-ttu-id="dd785-114">Példa 1: az összes házirend-definíció beolvasása</span><span class="sxs-lookup"><span data-stu-id="dd785-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzPolicyDefinition
```

<span data-ttu-id="dd785-115">Ez a parancs az összes házirend-definíciót megkapja.</span><span class="sxs-lookup"><span data-stu-id="dd785-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="dd785-116">2. példa: házirend-definíció beolvasása az aktuális előfizetésből név szerint</span><span class="sxs-lookup"><span data-stu-id="dd785-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="dd785-117">Ez a parancs az aktuális alapértelmezett előfizetésből a VMPolicyDefinition nevű házirend-definíciót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="dd785-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="dd785-118">3. példa: házirend-definíció beolvasása a kezelés csoportból név szerint</span><span class="sxs-lookup"><span data-stu-id="dd785-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="dd785-119">Ez a parancs a VMPolicyDefinition nevű házirend-definíciót a Dept42 nevű felügyeleti csoporttól kapja.</span><span class="sxs-lookup"><span data-stu-id="dd785-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="dd785-120">Példa 4: a beépített házirend-definíciók beszerzése az előfizetésből</span><span class="sxs-lookup"><span data-stu-id="dd785-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="dd785-121">Ez a parancs a beépített házirend-definíciókat az előfizetés 3bf44b72-c631-427a-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="dd785-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

## <span data-ttu-id="dd785-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd785-122">PARAMETERS</span></span>

### <span data-ttu-id="dd785-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="dd785-123">-ApiVersion</span></span>
<span data-ttu-id="dd785-124">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd785-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="dd785-125">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="dd785-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="dd785-126">-Beépített</span><span class="sxs-lookup"><span data-stu-id="dd785-126">-Builtin</span></span>
<span data-ttu-id="dd785-127">Az eredmények listáját csak a beépített házirend-definíciókkal korlátozhatja.</span><span class="sxs-lookup"><span data-stu-id="dd785-127">Limits list of results to only built-in policy definitions.</span></span>

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

### <span data-ttu-id="dd785-128">-Custom</span><span class="sxs-lookup"><span data-stu-id="dd785-128">-Custom</span></span>
<span data-ttu-id="dd785-129">Az eredmények listáját csak az egyéni házirend-definíciók szerint korlátozhatja.</span><span class="sxs-lookup"><span data-stu-id="dd785-129">Limits list of results to only custom policy definitions.</span></span>

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

### <span data-ttu-id="dd785-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd785-130">-DefaultProfile</span></span>
<span data-ttu-id="dd785-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dd785-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd785-132">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="dd785-132">-Id</span></span>
<span data-ttu-id="dd785-133">Annak a házirend-definíciónak a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="dd785-133">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="dd785-134">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="dd785-134">-InformationAction</span></span>
<span data-ttu-id="dd785-135">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="dd785-135">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="dd785-136">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="dd785-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dd785-137">Folytassa</span><span class="sxs-lookup"><span data-stu-id="dd785-137">Continue</span></span>
- <span data-ttu-id="dd785-138">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="dd785-138">Ignore</span></span>
- <span data-ttu-id="dd785-139">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="dd785-139">Inquire</span></span>
- <span data-ttu-id="dd785-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dd785-140">SilentlyContinue</span></span>
- <span data-ttu-id="dd785-141">állj</span><span class="sxs-lookup"><span data-stu-id="dd785-141">Stop</span></span>
- <span data-ttu-id="dd785-142">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="dd785-142">Suspend</span></span>

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

### <span data-ttu-id="dd785-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dd785-143">-InformationVariable</span></span>
<span data-ttu-id="dd785-144">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="dd785-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="dd785-145">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="dd785-145">-ManagementGroupName</span></span>
<span data-ttu-id="dd785-146">A beolvasott házirend-definíció (ok) kezelési csoportjának a neve.</span><span class="sxs-lookup"><span data-stu-id="dd785-146">The name of the management group of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="dd785-147">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dd785-147">-Name</span></span>
<span data-ttu-id="dd785-148">Annak a házirend-definíciónak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="dd785-148">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="dd785-149">-Pre</span><span class="sxs-lookup"><span data-stu-id="dd785-149">-Pre</span></span>
<span data-ttu-id="dd785-150">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="dd785-150">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="dd785-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dd785-151">-SubscriptionId</span></span>
<span data-ttu-id="dd785-152">A házirend-definíció (ok) előfizetési azonosítója a beszerzéshez.</span><span class="sxs-lookup"><span data-stu-id="dd785-152">The subscription ID of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="dd785-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd785-153">CommonParameters</span></span>
<span data-ttu-id="dd785-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd785-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd785-155">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd785-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd785-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd785-156">INPUTS</span></span>

## <span data-ttu-id="dd785-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd785-157">OUTPUTS</span></span>

## <span data-ttu-id="dd785-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd785-158">NOTES</span></span>

## <span data-ttu-id="dd785-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd785-159">RELATED LINKS</span></span>

[<span data-ttu-id="dd785-160">Új – AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dd785-160">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="dd785-161">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dd785-161">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="dd785-162">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dd785-162">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


