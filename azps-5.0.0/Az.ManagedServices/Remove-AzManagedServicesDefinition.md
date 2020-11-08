---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
ms.openlocfilehash: 2b81a1983bb89af48115ead85c3392cc3d762734
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187332"
---
# <span data-ttu-id="27d36-101">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="27d36-101">Remove-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="27d36-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27d36-102">SYNOPSIS</span></span>
<span data-ttu-id="27d36-103">Törli a regisztrációs definíciót.</span><span class="sxs-lookup"><span data-stu-id="27d36-103">Deletes the registration definition.</span></span>

## <span data-ttu-id="27d36-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27d36-104">SYNTAX</span></span>

### <span data-ttu-id="27d36-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="27d36-105">Default (Default)</span></span>
```
Remove-AzManagedServicesDefinition [-Scope <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27d36-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="27d36-106">ByInputObject</span></span>
```
Remove-AzManagedServicesDefinition -InputObject <PSRegistrationDefinition>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27d36-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="27d36-107">DESCRIPTION</span></span>
<span data-ttu-id="27d36-108">Törli a regisztrációs definíciót.</span><span class="sxs-lookup"><span data-stu-id="27d36-108">Deletes the registration definition.</span></span>

## <span data-ttu-id="27d36-109">Példák</span><span class="sxs-lookup"><span data-stu-id="27d36-109">EXAMPLES</span></span>

### <span data-ttu-id="27d36-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="27d36-110">Example 1</span></span>
```
PS C:\> Remove-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502
PS C:\>
```

<span data-ttu-id="27d36-111">A regisztráció definíciójának eltávolítása az alapértelmezett tartomány néven</span><span class="sxs-lookup"><span data-stu-id="27d36-111">Removes the registration definition by name at the default scope.</span></span>

### <span data-ttu-id="27d36-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="27d36-112">Example 2</span></span>
```
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d
PS C:\> Remove-AzManagedServicesDefinition -InputObject $definition
PS C:\>
```

<span data-ttu-id="27d36-113">A bemeneti objektumtól kapott regisztrációs definíció törlése</span><span class="sxs-lookup"><span data-stu-id="27d36-113">Deletes the registration definition given the input object.</span></span>

## <span data-ttu-id="27d36-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27d36-114">PARAMETERS</span></span>

### <span data-ttu-id="27d36-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27d36-115">-DefaultProfile</span></span>
<span data-ttu-id="27d36-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27d36-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27d36-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27d36-117">-InputObject</span></span>
<span data-ttu-id="27d36-118">A registration definition objektum.</span><span class="sxs-lookup"><span data-stu-id="27d36-118">The registration definition object.</span></span>

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

### <span data-ttu-id="27d36-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="27d36-119">-Name</span></span>
<span data-ttu-id="27d36-120">A regisztráció definíciójának egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="27d36-120">The unique name of the Registration Definition.</span></span>

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

### <span data-ttu-id="27d36-121">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="27d36-121">-Scope</span></span>
<span data-ttu-id="27d36-122">A regisztráció definícióját létrehozó hatókör.</span><span class="sxs-lookup"><span data-stu-id="27d36-122">The scope where the registration definition created.</span></span>

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

### <span data-ttu-id="27d36-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="27d36-123">-Confirm</span></span>
<span data-ttu-id="27d36-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="27d36-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27d36-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27d36-125">-WhatIf</span></span>
<span data-ttu-id="27d36-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="27d36-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27d36-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="27d36-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27d36-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27d36-128">CommonParameters</span></span>
<span data-ttu-id="27d36-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27d36-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27d36-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="27d36-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27d36-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27d36-131">INPUTS</span></span>

### <span data-ttu-id="27d36-132">Microsoft. Azure. PowerShell. parancsmagok. ManagedServices. models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="27d36-132">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="27d36-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27d36-133">OUTPUTS</span></span>

### <span data-ttu-id="27d36-134">System. Void</span><span class="sxs-lookup"><span data-stu-id="27d36-134">System.Void</span></span>
## <span data-ttu-id="27d36-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27d36-135">NOTES</span></span>

## <span data-ttu-id="27d36-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27d36-136">RELATED LINKS</span></span>
