---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/powershell/module/az.managedservices/get-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
ms.openlocfilehash: 5f0398981f6c3a59c9401df4ec89208a5f8196b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925506"
---
# <span data-ttu-id="d676d-101">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="d676d-101">Get-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="d676d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d676d-102">SYNOPSIS</span></span>
<span data-ttu-id="d676d-103">Egy adott regisztrációs feladatot vagy a regisztrációs feladatok listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d676d-103">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="d676d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d676d-104">SYNTAX</span></span>

### <span data-ttu-id="d676d-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d676d-105">Default (Default)</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d676d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d676d-106">ByName</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-Name <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d676d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d676d-107">DESCRIPTION</span></span>
<span data-ttu-id="d676d-108">Egy adott regisztrációs feladatot vagy a regisztrációs feladatok listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d676d-108">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="d676d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d676d-109">EXAMPLES</span></span>

### <span data-ttu-id="d676d-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="d676d-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesAssignment

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="d676d-111">Az alapértelmezett hatókör alá tartozó összes regisztrációs hozzárendelést beveszi.</span><span class="sxs-lookup"><span data-stu-id="d676d-111">Gets all registration assignments under the default scope.</span></span>

### <span data-ttu-id="d676d-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="d676d-112">Example 2</span></span>
```
PS C:\> $assignments = Get-AzManagedServicesAssignment -ExpandRegistrationDefinition
PS C:\> $assignments[0].Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : 0c146106-c927-4098-a7ca-30bbcf44a502

PS C:\>
```

<span data-ttu-id="d676d-113">Beveszi az összes regisztrációs hozzárendelést a regisztrációdefiníció részleteivel.</span><span class="sxs-lookup"><span data-stu-id="d676d-113">Gets all registration assignments with the registration definition details.</span></span>

### <span data-ttu-id="d676d-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="d676d-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="d676d-115">Név szerint, a regisztráció definíciójának részletei nélkül kapja meg a regisztráció-hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="d676d-115">Gets a registration assignment by name without registration definition details.</span></span>

### <span data-ttu-id="d676d-116">4. példa</span><span class="sxs-lookup"><span data-stu-id="d676d-116">Example 4</span></span>
```
PS C:\> $assignment = Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80 -ExpandRegistrationDefinition
PS C:\> $assignment.Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : 0c146106-c927-4098-a7ca-30bbcf44a502

PS C:\>
```

<span data-ttu-id="d676d-117">Név szerint kap egy regisztráció-hozzárendelést a regisztráció definíciójának részleteivel.</span><span class="sxs-lookup"><span data-stu-id="d676d-117">Gets a registration assignment by name with registration definition details.</span></span>

### <span data-ttu-id="d676d-118">5. példa</span><span class="sxs-lookup"><span data-stu-id="d676d-118">Example 5</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="d676d-119">Az összes regisztrációs hozzárendelést egy adott hatókörben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d676d-119">Gets all the registration assignments at given scope.</span></span>

## <span data-ttu-id="d676d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d676d-120">PARAMETERS</span></span>

### <span data-ttu-id="d676d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d676d-121">-DefaultProfile</span></span>
<span data-ttu-id="d676d-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d676d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d676d-123">-ExpandRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="d676d-123">-ExpandRegistrationDefinition</span></span>
<span data-ttu-id="d676d-124">Szerepeljenek-e a regisztrációdefiníció részletei.</span><span class="sxs-lookup"><span data-stu-id="d676d-124">Whether to include registration definition details.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d676d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d676d-125">-Name</span></span>
<span data-ttu-id="d676d-126">A regisztrációs feladat egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="d676d-126">The unique name of the Registration Assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d676d-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="d676d-127">-Scope</span></span>
<span data-ttu-id="d676d-128">A regisztrációs feladat létrehozási hatóköre.</span><span class="sxs-lookup"><span data-stu-id="d676d-128">The scope where the registration assignment created.</span></span>

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

### <span data-ttu-id="d676d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d676d-129">CommonParameters</span></span>
<span data-ttu-id="d676d-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d676d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d676d-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d676d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d676d-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d676d-132">INPUTS</span></span>

### <span data-ttu-id="d676d-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="d676d-133">None</span></span>
## <span data-ttu-id="d676d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d676d-134">OUTPUTS</span></span>

### <span data-ttu-id="d676d-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="d676d-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="d676d-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d676d-136">NOTES</span></span>

## <span data-ttu-id="d676d-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d676d-137">RELATED LINKS</span></span>
