---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
ms.openlocfilehash: 5282b3d0ae145088cf07040520050937f8d3a335
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187336"
---
# <span data-ttu-id="a7c63-101">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="a7c63-101">Get-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="a7c63-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a7c63-102">SYNOPSIS</span></span>
<span data-ttu-id="a7c63-103">Beolvassa a regisztráció definícióját vagy a regisztrációs definíciók listáját.</span><span class="sxs-lookup"><span data-stu-id="a7c63-103">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="a7c63-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a7c63-104">SYNTAX</span></span>

### <span data-ttu-id="a7c63-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a7c63-105">ByName (Default)</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7c63-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="a7c63-106">Default</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7c63-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a7c63-107">DESCRIPTION</span></span>
<span data-ttu-id="a7c63-108">Beolvassa a regisztráció definícióját vagy a regisztrációs definíciók listáját.</span><span class="sxs-lookup"><span data-stu-id="a7c63-108">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="a7c63-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a7c63-109">EXAMPLES</span></span>

### <span data-ttu-id="a7c63-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a7c63-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesDefinition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="a7c63-111">Az összes regisztráció definíciója az alapértelmezett tartományban lesz.</span><span class="sxs-lookup"><span data-stu-id="a7c63-111">Gets all registration definitions at default scope.</span></span>

### <span data-ttu-id="a7c63-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="a7c63-112">Example 2</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="a7c63-113">A regisztráció definícióját név szerint kapja meg alapértelmezett hatókörben.</span><span class="sxs-lookup"><span data-stu-id="a7c63-113">Gets the registration definition by name at default scope.</span></span>

### <span data-ttu-id="a7c63-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="a7c63-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="a7c63-115">Beolvassa az összes regisztráció definícióját a megadott hatókörben.</span><span class="sxs-lookup"><span data-stu-id="a7c63-115">Gets all registration definitions at the given scope.</span></span>

## <span data-ttu-id="a7c63-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a7c63-116">PARAMETERS</span></span>

### <span data-ttu-id="a7c63-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7c63-117">-DefaultProfile</span></span>
<span data-ttu-id="a7c63-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a7c63-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7c63-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a7c63-119">-Name</span></span>
<span data-ttu-id="a7c63-120">A regisztráció definíciójának egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="a7c63-120">The unique name of the Registration Definition.</span></span>

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

### <span data-ttu-id="a7c63-121">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="a7c63-121">-Scope</span></span>
<span data-ttu-id="a7c63-122">A regisztráció definícióját létrehozó hatókör.</span><span class="sxs-lookup"><span data-stu-id="a7c63-122">The scope where the registration definition created.</span></span>

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

### <span data-ttu-id="a7c63-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7c63-123">CommonParameters</span></span>
<span data-ttu-id="a7c63-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a7c63-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7c63-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a7c63-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7c63-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7c63-126">INPUTS</span></span>

### <span data-ttu-id="a7c63-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="a7c63-127">None</span></span>
## <span data-ttu-id="a7c63-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7c63-128">OUTPUTS</span></span>

### <span data-ttu-id="a7c63-129">Microsoft. Azure. PowerShell. parancsmagok. ManagedServices. models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="a7c63-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="a7c63-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a7c63-130">NOTES</span></span>

## <span data-ttu-id="a7c63-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7c63-131">RELATED LINKS</span></span>
