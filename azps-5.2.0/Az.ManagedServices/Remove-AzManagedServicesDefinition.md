---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
ms.openlocfilehash: 2b81a1983bb89af48115ead85c3392cc3d762734
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368212"
---
# <span data-ttu-id="68ad8-101">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="68ad8-101">Remove-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="68ad8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68ad8-102">SYNOPSIS</span></span>
<span data-ttu-id="68ad8-103">Törli a regisztrációs definíciót.</span><span class="sxs-lookup"><span data-stu-id="68ad8-103">Deletes the registration definition.</span></span>

## <span data-ttu-id="68ad8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="68ad8-104">SYNTAX</span></span>

### <span data-ttu-id="68ad8-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="68ad8-105">Default (Default)</span></span>
```
Remove-AzManagedServicesDefinition [-Scope <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68ad8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="68ad8-106">ByInputObject</span></span>
```
Remove-AzManagedServicesDefinition -InputObject <PSRegistrationDefinition>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68ad8-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="68ad8-107">DESCRIPTION</span></span>
<span data-ttu-id="68ad8-108">Törli a regisztrációs definíciót.</span><span class="sxs-lookup"><span data-stu-id="68ad8-108">Deletes the registration definition.</span></span>

## <span data-ttu-id="68ad8-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="68ad8-109">EXAMPLES</span></span>

### <span data-ttu-id="68ad8-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="68ad8-110">Example 1</span></span>
```
PS C:\> Remove-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502
PS C:\>
```

<span data-ttu-id="68ad8-111">Eltávolítja a név szerinti regisztrációdefiníciót az alapértelmezett hatókörben.</span><span class="sxs-lookup"><span data-stu-id="68ad8-111">Removes the registration definition by name at the default scope.</span></span>

### <span data-ttu-id="68ad8-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="68ad8-112">Example 2</span></span>
```
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d
PS C:\> Remove-AzManagedServicesDefinition -InputObject $definition
PS C:\>
```

<span data-ttu-id="68ad8-113">Törli a bemeneti objektumhoz megadott regisztrációs definíciót.</span><span class="sxs-lookup"><span data-stu-id="68ad8-113">Deletes the registration definition given the input object.</span></span>

## <span data-ttu-id="68ad8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68ad8-114">PARAMETERS</span></span>

### <span data-ttu-id="68ad8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68ad8-115">-DefaultProfile</span></span>
<span data-ttu-id="68ad8-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="68ad8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68ad8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68ad8-117">-InputObject</span></span>
<span data-ttu-id="68ad8-118">A regisztrációs definíciós objektum.</span><span class="sxs-lookup"><span data-stu-id="68ad8-118">The registration definition object.</span></span>

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

### <span data-ttu-id="68ad8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="68ad8-119">-Name</span></span>
<span data-ttu-id="68ad8-120">A Regisztrációdefiníció egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="68ad8-120">The unique name of the Registration Definition.</span></span>

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

### <span data-ttu-id="68ad8-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="68ad8-121">-Scope</span></span>
<span data-ttu-id="68ad8-122">Az a hatókör, ahol a regisztrációs definíció létre van hozva.</span><span class="sxs-lookup"><span data-stu-id="68ad8-122">The scope where the registration definition created.</span></span>

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

### <span data-ttu-id="68ad8-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68ad8-123">-Confirm</span></span>
<span data-ttu-id="68ad8-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="68ad8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68ad8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68ad8-125">-WhatIf</span></span>
<span data-ttu-id="68ad8-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="68ad8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68ad8-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="68ad8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68ad8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68ad8-128">CommonParameters</span></span>
<span data-ttu-id="68ad8-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68ad8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68ad8-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68ad8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68ad8-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="68ad8-131">INPUTS</span></span>

### <span data-ttu-id="68ad8-132">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="68ad8-132">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="68ad8-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68ad8-133">OUTPUTS</span></span>

### <span data-ttu-id="68ad8-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="68ad8-134">System.Void</span></span>
## <span data-ttu-id="68ad8-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="68ad8-135">NOTES</span></span>

## <span data-ttu-id="68ad8-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68ad8-136">RELATED LINKS</span></span>
