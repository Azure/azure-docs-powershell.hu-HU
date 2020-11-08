---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
ms.openlocfilehash: 8aae61e163baf95cbed62ea239c7d1a6190aed1f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187340"
---
# <span data-ttu-id="586b3-101">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="586b3-101">Get-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="586b3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="586b3-102">SYNOPSIS</span></span>
<span data-ttu-id="586b3-103">Egy bizonyos regisztrációs feladatot vagy a regisztrációs feladatok listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="586b3-103">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="586b3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="586b3-104">SYNTAX</span></span>

### <span data-ttu-id="586b3-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="586b3-105">Default (Default)</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="586b3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="586b3-106">ByName</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-Name <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="586b3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="586b3-107">DESCRIPTION</span></span>
<span data-ttu-id="586b3-108">Egy bizonyos regisztrációs feladatot vagy a regisztrációs feladatok listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="586b3-108">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="586b3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="586b3-109">EXAMPLES</span></span>

### <span data-ttu-id="586b3-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="586b3-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesAssignment

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="586b3-111">Beolvassa az összes regisztrációs feladatot az alapértelmezett tartomány alá.</span><span class="sxs-lookup"><span data-stu-id="586b3-111">Gets all registration assignments under the default scope.</span></span>

### <span data-ttu-id="586b3-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="586b3-112">Example 2</span></span>
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

<span data-ttu-id="586b3-113">Az összes regisztrációs feladat beolvasása a regisztráció definíciójának részleteivel</span><span class="sxs-lookup"><span data-stu-id="586b3-113">Gets all registration assignments with the registration definition details.</span></span>

### <span data-ttu-id="586b3-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="586b3-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="586b3-115">A regisztrációt a regisztráció megadása nélkül kapja meg.</span><span class="sxs-lookup"><span data-stu-id="586b3-115">Gets a registration assignment by name without registration definition details.</span></span>

### <span data-ttu-id="586b3-116">4. példa</span><span class="sxs-lookup"><span data-stu-id="586b3-116">Example 4</span></span>
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

<span data-ttu-id="586b3-117">Beilleszti a regisztrációs feladatot név szerint a regisztráció meghatározása részleteivel.</span><span class="sxs-lookup"><span data-stu-id="586b3-117">Gets a registration assignment by name with registration definition details.</span></span>

### <span data-ttu-id="586b3-118">Példa 5</span><span class="sxs-lookup"><span data-stu-id="586b3-118">Example 5</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="586b3-119">Megkapja az összes regisztrációs feladatot a megadott hatókörben.</span><span class="sxs-lookup"><span data-stu-id="586b3-119">Gets all the registration assignments at given scope.</span></span>

## <span data-ttu-id="586b3-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="586b3-120">PARAMETERS</span></span>

### <span data-ttu-id="586b3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="586b3-121">-DefaultProfile</span></span>
<span data-ttu-id="586b3-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="586b3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="586b3-123">-ExpandRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="586b3-123">-ExpandRegistrationDefinition</span></span>
<span data-ttu-id="586b3-124">Szeretné-e szerepeltetni a regisztráció meghatározásának részleteit.</span><span class="sxs-lookup"><span data-stu-id="586b3-124">Whether to include registration definition details.</span></span>

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

### <span data-ttu-id="586b3-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="586b3-125">-Name</span></span>
<span data-ttu-id="586b3-126">A regisztrációs feladat egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="586b3-126">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="586b3-127">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="586b3-127">-Scope</span></span>
<span data-ttu-id="586b3-128">Az a tartomány, amelyben a regisztrálási feladat létrehozva van.</span><span class="sxs-lookup"><span data-stu-id="586b3-128">The scope where the registration assignment created.</span></span>

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

### <span data-ttu-id="586b3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="586b3-129">CommonParameters</span></span>
<span data-ttu-id="586b3-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="586b3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="586b3-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="586b3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="586b3-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="586b3-132">INPUTS</span></span>

### <span data-ttu-id="586b3-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="586b3-133">None</span></span>
## <span data-ttu-id="586b3-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="586b3-134">OUTPUTS</span></span>

### <span data-ttu-id="586b3-135">Microsoft. Azure. PowerShell. parancsmagok. ManagedServices. models. PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="586b3-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="586b3-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="586b3-136">NOTES</span></span>

## <span data-ttu-id="586b3-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="586b3-137">RELATED LINKS</span></span>
