---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
ms.openlocfilehash: 5f2328ba75a0142a61238665eef41e32bf1fbba6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845486"
---
# <span data-ttu-id="5334e-101">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="5334e-101">Remove-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="5334e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5334e-102">SYNOPSIS</span></span>
<span data-ttu-id="5334e-103">Törli a regisztrációs feladatot.</span><span class="sxs-lookup"><span data-stu-id="5334e-103">Deletes a registration assignment.</span></span>

## <span data-ttu-id="5334e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5334e-104">SYNTAX</span></span>

### <span data-ttu-id="5334e-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5334e-105">Default (Default)</span></span>
```
Remove-AzManagedServicesAssignment [[-Scope] <String>] -Id <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5334e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5334e-106">ByResourceId</span></span>
```
Remove-AzManagedServicesAssignment -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5334e-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5334e-107">ByInputObject</span></span>
```
Remove-AzManagedServicesAssignment -InputObject <PSRegistrationAssignment> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5334e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5334e-108">DESCRIPTION</span></span>
<span data-ttu-id="5334e-109">Törli a regisztrációs feladatot.</span><span class="sxs-lookup"><span data-stu-id="5334e-109">Deletes a registration assignment.</span></span>

## <span data-ttu-id="5334e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5334e-110">EXAMPLES</span></span>

### <span data-ttu-id="5334e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5334e-111">Example 1</span></span>
```powershell
PS C:\Remove-AzManagedServicesAssignment -Id b037e73c-815e-4472-868f-59e51b49b949

Name                                 RegistrationDefinitionId
----                                 ------------------------
b037e73c-815e-4472-868f-59e51b49b949 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/be2f72e6-93e0-4d3f-ac50-9a756ed4ffa7
```

<span data-ttu-id="5334e-112">Törli a regisztrációs feladatot az alapértelmezett hatókörben.</span><span class="sxs-lookup"><span data-stu-id="5334e-112">Deletes the registration assignment under the default scope.</span></span>

### <span data-ttu-id="5334e-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="5334e-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzManagedServicesAssignment -ResourceId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationAssignments/88ba878b-9a3c-40c3-80da-015cbe488a2f

Name                                 RegistrationDefinitionId
----                                 ------------------------
88ba878b-9a3c-40c3-80da-015cbe488a2f /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/40be0299-6573-4391-be2f-b41dd4aaf4f9
```

<span data-ttu-id="5334e-114">A teljes mértékben minősített erőforrás-azonosítóval rendelkező regisztrációs feladat törlése</span><span class="sxs-lookup"><span data-stu-id="5334e-114">Deletes the registration assignment given the fully qualified resource id.</span></span>

### <span data-ttu-id="5334e-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="5334e-115">Example 3</span></span>
```powershell
PS C:\> $assignment = New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/33974646-9bce-461d-89eb-331f20fca33c
PS C:\> Remove-AzManagedServicesAssignment -InputObject $assignment
```

<span data-ttu-id="5334e-116">A regisztrációs hozzárendelés törlése a megadott bemeneti objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="5334e-116">Deletes the registration assignment using the input object provided.</span></span>

## <span data-ttu-id="5334e-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5334e-117">PARAMETERS</span></span>

### <span data-ttu-id="5334e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5334e-118">-AsJob</span></span>
<span data-ttu-id="5334e-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5334e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5334e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5334e-120">-DefaultProfile</span></span>
<span data-ttu-id="5334e-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5334e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5334e-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="5334e-122">-Id</span></span>
<span data-ttu-id="5334e-123">A regisztrációs hozzárendelés globálisan egyedi azonosítója (például b0c052e5-c437-4771-a476-8b1201158a57)</span><span class="sxs-lookup"><span data-stu-id="5334e-123">The registration assignment GUID (for example, b0c052e5-c437-4771-a476-8b1201158a57)</span></span>
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

### <span data-ttu-id="5334e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5334e-124">-InputObject</span></span>
<span data-ttu-id="5334e-125">A regisztráció hozzárendelési objektum.</span><span class="sxs-lookup"><span data-stu-id="5334e-125">The registration assignment object.</span></span>

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

### <span data-ttu-id="5334e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5334e-126">-ResourceId</span></span>
<span data-ttu-id="5334e-127">A regisztrációs hozzárendelés teljes erőforrás-azonosítója (például/subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationAssignments/b0c052e5-c437-4771-a476-8b1201158a57).</span><span class="sxs-lookup"><span data-stu-id="5334e-127">The fully qualified resource id of the registration assignment (for example, /subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationAssignments/b0c052e5-c437-4771-a476-8b1201158a57).</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5334e-128">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="5334e-128">-Scope</span></span>
<span data-ttu-id="5334e-129">Az a hatókör, ahol a regisztrációs feladatot létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="5334e-129">The scope where the registration assignment should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5334e-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5334e-130">-Confirm</span></span>
<span data-ttu-id="5334e-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5334e-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5334e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5334e-132">-WhatIf</span></span>
<span data-ttu-id="5334e-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5334e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5334e-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5334e-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5334e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5334e-135">CommonParameters</span></span>
<span data-ttu-id="5334e-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5334e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5334e-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5334e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5334e-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5334e-138">INPUTS</span></span>

### <span data-ttu-id="5334e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5334e-139">System.String</span></span>

### <span data-ttu-id="5334e-140">Microsoft. Azure. PowerShell. parancsmagok. ManagedServices. models. PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="5334e-140">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>

## <span data-ttu-id="5334e-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5334e-141">OUTPUTS</span></span>

### <span data-ttu-id="5334e-142">Microsoft. Azure. PowerShell. parancsmagok. ManagedServices. models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="5334e-142">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="5334e-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5334e-143">NOTES</span></span>

## <span data-ttu-id="5334e-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5334e-144">RELATED LINKS</span></span>
