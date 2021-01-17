---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
ms.openlocfilehash: 8023dde9253ccb4a1f7ff223c4dfdddf773a4728
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467641"
---
# <span data-ttu-id="73315-101">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="73315-101">New-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="73315-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73315-102">SYNOPSIS</span></span>
<span data-ttu-id="73315-103">Regisztrációs feladatot hoz létre vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="73315-103">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="73315-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="73315-104">SYNTAX</span></span>

### <span data-ttu-id="73315-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="73315-105">Default (Default)</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>] -RegistrationDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73315-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="73315-106">ByInputObject</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>]
 -RegistrationDefinition <PSRegistrationDefinition> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73315-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="73315-107">DESCRIPTION</span></span>
<span data-ttu-id="73315-108">Regisztrációs feladatot hoz létre vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="73315-108">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="73315-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="73315-109">EXAMPLES</span></span>

### <span data-ttu-id="73315-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="73315-110">Example 1</span></span>
```
PS C:\> $definition = Get-AzManagedServicesDefinition
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded

PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\>
```

<span data-ttu-id="73315-111">Létrehoz egy regisztrációs hozzárendelést az alapértelmezett hatókörben a regisztrációs definíció azonosító használatával.</span><span class="sxs-lookup"><span data-stu-id="73315-111">Creates a registration assignment at the default scope using the registration definition identifier.</span></span>

### <span data-ttu-id="73315-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="73315-112">Example 2</span></span>
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


PS C:\>
```

<span data-ttu-id="73315-113">Egy regisztrációs hozzárendelést hoz létre bemenetként egy regisztrációs definíciós objektummal.</span><span class="sxs-lookup"><span data-stu-id="73315-113">Creates a registration assignment with a registration definition object as input.</span></span>

### <span data-ttu-id="73315-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="73315-114">Example 3</span></span>
```
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 -Name 12b05f0f-3426-48da-9e67-738e1dbf775f

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded

PS C:\>
```

<span data-ttu-id="73315-115">Frissíti a regisztrációs hozzárendelést egy regisztrációdefiníciós azonosítóval és névvel.</span><span class="sxs-lookup"><span data-stu-id="73315-115">Updates a registration assignment with a registration definition identifier and name.</span></span>


## <span data-ttu-id="73315-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73315-116">PARAMETERS</span></span>

### <span data-ttu-id="73315-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73315-117">-DefaultProfile</span></span>
<span data-ttu-id="73315-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73315-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73315-119">-Name</span><span class="sxs-lookup"><span data-stu-id="73315-119">-Name</span></span>
<span data-ttu-id="73315-120">A regisztrációs feladat egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="73315-120">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="73315-121">-RegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="73315-121">-RegistrationDefinition</span></span>
<span data-ttu-id="73315-122">A regisztrációs definíció bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="73315-122">The registration definition input object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73315-123">-RegistrationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="73315-123">-RegistrationDefinitionId</span></span>
<span data-ttu-id="73315-124">A regisztrációdefiníció teljes erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="73315-124">The fully qualified resource id of the registration definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73315-125">-Scope</span><span class="sxs-lookup"><span data-stu-id="73315-125">-Scope</span></span>
<span data-ttu-id="73315-126">A regisztrációs hozzárendelés létrehozási hatóköre.</span><span class="sxs-lookup"><span data-stu-id="73315-126">The scope where the registration assignment should be created.</span></span>

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

### <span data-ttu-id="73315-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73315-127">-AsJob</span></span>
<span data-ttu-id="73315-128">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="73315-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="73315-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73315-129">-Confirm</span></span>
<span data-ttu-id="73315-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="73315-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73315-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73315-131">-WhatIf</span></span>
<span data-ttu-id="73315-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="73315-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73315-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="73315-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73315-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73315-134">CommonParameters</span></span>
<span data-ttu-id="73315-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73315-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73315-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73315-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73315-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73315-137">INPUTS</span></span>

### <span data-ttu-id="73315-138">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="73315-138">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
### <span data-ttu-id="73315-139">System.String</span><span class="sxs-lookup"><span data-stu-id="73315-139">System.String</span></span>
## <span data-ttu-id="73315-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73315-140">OUTPUTS</span></span>

### <span data-ttu-id="73315-141">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="73315-141">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="73315-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="73315-142">NOTES</span></span>

## <span data-ttu-id="73315-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73315-143">RELATED LINKS</span></span>
