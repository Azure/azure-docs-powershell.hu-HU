---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
ms.openlocfilehash: a3a39db5f110f247ab58f2b4c6afcdb4536f4f50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147546"
---
# <span data-ttu-id="c9fbf-101">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="c9fbf-101">Remove-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="c9fbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9fbf-102">SYNOPSIS</span></span>
<span data-ttu-id="c9fbf-103">Egy regisztrációs feladat törlése.</span><span class="sxs-lookup"><span data-stu-id="c9fbf-103">Deletes a registration assignment.</span></span>

## <span data-ttu-id="c9fbf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c9fbf-104">SYNTAX</span></span>

### <span data-ttu-id="c9fbf-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c9fbf-105">Default (Default)</span></span>
```
Remove-AzManagedServicesAssignment [-Scope <String>] -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9fbf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c9fbf-106">ByInputObject</span></span>
```
Remove-AzManagedServicesAssignment -InputObject <PSRegistrationAssignment> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9fbf-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c9fbf-107">DESCRIPTION</span></span>
<span data-ttu-id="c9fbf-108">Egy regisztrációs feladat törlése.</span><span class="sxs-lookup"><span data-stu-id="c9fbf-108">Deletes a registration assignment.</span></span>

## <span data-ttu-id="c9fbf-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c9fbf-109">EXAMPLES</span></span>

### <span data-ttu-id="c9fbf-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="c9fbf-110">Example 1</span></span>
```
PS C:\> Remove-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80
PS C:\>
```

<span data-ttu-id="c9fbf-111">Törli a regisztrációs hozzárendelést név szerint az alapértelmezett hatókörben.</span><span class="sxs-lookup"><span data-stu-id="c9fbf-111">Deletes the registration assignment by name at the default scope.</span></span>

### <span data-ttu-id="c9fbf-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="c9fbf-112">Example 2</span></span>
```
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 -Name 12b05f0f-3426-48da-9e67-738e1dbf775f

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\> $assignment = Get-AzManagedServicesAssignment -Name 12b05f0f-3426-48da-9e67-738e1dbf775f
PS C:\> Remove-AzManagedServicesAssignment -InputObject $assignment
PS C:\>
```

<span data-ttu-id="c9fbf-113">A megadott bemeneti objektum használatával törli a regisztrációs hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="c9fbf-113">Deletes the registration assignment using the input object provided.</span></span>

### <span data-ttu-id="c9fbf-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="c9fbf-114">Example 3</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded


PS C:\> New-AzManagedServicesAssignment -RegistrationDefinition $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b279ec53-b42f-4952-bd62-cd49982e9572 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/b279ec53-b42f-4952-bd62-cd49982e9572 Succeeded


PS C:\> Remove-AzManagedServicesAssignment -Name b279ec53-b42f-4952-bd62-cd49982e9572 -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8
PS C:\>
```

<span data-ttu-id="c9fbf-115">Törli a regisztrációs hozzárendelést név szerint a megadott hatókörben.</span><span class="sxs-lookup"><span data-stu-id="c9fbf-115">Deletes the registration assignment by name at the given scope.</span></span>

## <span data-ttu-id="c9fbf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9fbf-116">PARAMETERS</span></span>

### <span data-ttu-id="c9fbf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9fbf-117">-DefaultProfile</span></span>
<span data-ttu-id="c9fbf-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9fbf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9fbf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9fbf-119">-InputObject</span></span>
<span data-ttu-id="c9fbf-120">A regisztrációs hozzárendelés-objektum.</span><span class="sxs-lookup"><span data-stu-id="c9fbf-120">The registration assignment object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9fbf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c9fbf-121">-Name</span></span>
<span data-ttu-id="c9fbf-122">A regisztrációs feladat egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="c9fbf-122">The unique name of the Registration Assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9fbf-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="c9fbf-123">-Scope</span></span>
<span data-ttu-id="c9fbf-124">A regisztráció-hozzárendelés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="c9fbf-124">The scope of the registration assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9fbf-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9fbf-125">-AsJob</span></span>
<span data-ttu-id="c9fbf-126">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c9fbf-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c9fbf-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9fbf-127">-Confirm</span></span>
<span data-ttu-id="c9fbf-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c9fbf-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9fbf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9fbf-129">-WhatIf</span></span>
<span data-ttu-id="c9fbf-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c9fbf-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9fbf-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c9fbf-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9fbf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9fbf-132">CommonParameters</span></span>
<span data-ttu-id="c9fbf-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9fbf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9fbf-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9fbf-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9fbf-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9fbf-135">INPUTS</span></span>

### <span data-ttu-id="c9fbf-136">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="c9fbf-136">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="c9fbf-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9fbf-137">OUTPUTS</span></span>

### <span data-ttu-id="c9fbf-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="c9fbf-138">System.Void</span></span>
## <span data-ttu-id="c9fbf-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c9fbf-139">NOTES</span></span>

## <span data-ttu-id="c9fbf-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9fbf-140">RELATED LINKS</span></span>
