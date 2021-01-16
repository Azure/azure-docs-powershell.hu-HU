---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
ms.openlocfilehash: 5282b3d0ae145088cf07040520050937f8d3a335
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476853"
---
# <span data-ttu-id="e9c1e-101">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="e9c1e-101">Get-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="e9c1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9c1e-102">SYNOPSIS</span></span>
<span data-ttu-id="e9c1e-103">Egy adott regisztrációs definíciót vagy a regisztrációs definíciók listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e9c1e-103">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="e9c1e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e9c1e-104">SYNTAX</span></span>

### <span data-ttu-id="e9c1e-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e9c1e-105">ByName (Default)</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9c1e-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="e9c1e-106">Default</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9c1e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e9c1e-107">DESCRIPTION</span></span>
<span data-ttu-id="e9c1e-108">Egy adott regisztrációs definíciót vagy a regisztrációs definíciók listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e9c1e-108">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="e9c1e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e9c1e-109">EXAMPLES</span></span>

### <span data-ttu-id="e9c1e-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="e9c1e-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesDefinition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="e9c1e-111">Az összes regisztrációs definíció alapértelmezett hatókörét beveszi.</span><span class="sxs-lookup"><span data-stu-id="e9c1e-111">Gets all registration definitions at default scope.</span></span>

### <span data-ttu-id="e9c1e-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="e9c1e-112">Example 2</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="e9c1e-113">A regisztráció definícióját név szerint, alapértelmezett hatókör szerint kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e9c1e-113">Gets the registration definition by name at default scope.</span></span>

### <span data-ttu-id="e9c1e-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="e9c1e-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="e9c1e-115">A megadott hatókörű összes regisztrációs definíciót beveszi.</span><span class="sxs-lookup"><span data-stu-id="e9c1e-115">Gets all registration definitions at the given scope.</span></span>

## <span data-ttu-id="e9c1e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9c1e-116">PARAMETERS</span></span>

### <span data-ttu-id="e9c1e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9c1e-117">-DefaultProfile</span></span>
<span data-ttu-id="e9c1e-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9c1e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9c1e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e9c1e-119">-Name</span></span>
<span data-ttu-id="e9c1e-120">A Regisztrációdefiníció egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="e9c1e-120">The unique name of the Registration Definition.</span></span>

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

### <span data-ttu-id="e9c1e-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="e9c1e-121">-Scope</span></span>
<span data-ttu-id="e9c1e-122">Az a hatókör, ahol a regisztrációs definíció létre van hozva.</span><span class="sxs-lookup"><span data-stu-id="e9c1e-122">The scope where the registration definition created.</span></span>

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

### <span data-ttu-id="e9c1e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9c1e-123">CommonParameters</span></span>
<span data-ttu-id="e9c1e-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9c1e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9c1e-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9c1e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9c1e-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9c1e-126">INPUTS</span></span>

### <span data-ttu-id="e9c1e-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="e9c1e-127">None</span></span>
## <span data-ttu-id="e9c1e-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9c1e-128">OUTPUTS</span></span>

### <span data-ttu-id="e9c1e-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="e9c1e-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="e9c1e-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e9c1e-130">NOTES</span></span>

## <span data-ttu-id="e9c1e-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9c1e-131">RELATED LINKS</span></span>
