---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
ms.openlocfilehash: 9d63c208daffe6e06da759ff929de120cab58c1c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665931"
---
# <span data-ttu-id="5984d-101">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="5984d-101">Remove-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="5984d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5984d-102">SYNOPSIS</span></span>
<span data-ttu-id="5984d-103">Törli a regisztrációs definíciót.</span><span class="sxs-lookup"><span data-stu-id="5984d-103">Deletes the registration definition.</span></span>

## <span data-ttu-id="5984d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5984d-104">SYNTAX</span></span>

### <span data-ttu-id="5984d-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5984d-105">Default (Default)</span></span>
```
Remove-AzManagedServicesDefinition -Id <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5984d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5984d-106">ByResourceId</span></span>
```
Remove-AzManagedServicesDefinition -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5984d-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5984d-107">ByInputObject</span></span>
```
Remove-AzManagedServicesDefinition -InputObject <PSRegistrationDefinition> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5984d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5984d-108">DESCRIPTION</span></span>
<span data-ttu-id="5984d-109">Törli a regisztrációs definíciót.</span><span class="sxs-lookup"><span data-stu-id="5984d-109">Deletes the registration definition.</span></span>

## <span data-ttu-id="5984d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5984d-110">EXAMPLES</span></span>

### <span data-ttu-id="5984d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5984d-111">Example 1</span></span>
```powershell
PS C:\> Remove-RegistrationDefinition -Id 0513b566-cab0-4fef-9b53-a285cd33389f
```

<span data-ttu-id="5984d-112">Eltávolítja a regisztrációs definíciót az IT-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="5984d-112">Removes the registration definition given it identifier.</span></span>

### <span data-ttu-id="5984d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="5984d-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzManagedServicesDefinition -ResourceId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/11b7c937-c5c1-4dd1-9a77-204591f93fcd

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
11b7c937-c5c1-4dd1-9a77-204591f93fcd bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="5984d-114">A teljes mértékben minősített erőforrás-azonosító alapján eltávolítja a regisztrációs definíciót.</span><span class="sxs-lookup"><span data-stu-id="5984d-114">Removes the registration definition given the fully qualified resource id.</span></span> 

### <span data-ttu-id="5984d-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="5984d-115">Example 3</span></span>
```powershell
PS C:\> $def = New-AzManagedServicesDefinition -RegistrationDefinitionName 572e1807-b80b-4401-9128-1968f432a5ad -ManagedByTenantId "bab3375b-6197-4a15-a44b-16c41faa91d7" -PrincipalId "d6f6c88a-5b7a-455e-ba40-ce146d4d3671" -RoleDefinitionId "acdd72a7-3385-48ef-bd42-f606fba81ae7"
PS C:\> Remove-AzManagedServicesDefinition -InputObject $def

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
eee59839-119f-453f-adec-4a72a8687125 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="5984d-116">Törli az objektum által megadott regisztrációs definíciót.</span><span class="sxs-lookup"><span data-stu-id="5984d-116">Deletes the registration definition given the object.</span></span>

## <span data-ttu-id="5984d-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5984d-117">PARAMETERS</span></span>

### <span data-ttu-id="5984d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5984d-118">-AsJob</span></span>
<span data-ttu-id="5984d-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5984d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5984d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5984d-120">-DefaultProfile</span></span>
<span data-ttu-id="5984d-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5984d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5984d-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="5984d-122">-Id</span></span>
<span data-ttu-id="5984d-123">A registration definition azonosító.</span><span class="sxs-lookup"><span data-stu-id="5984d-123">The registration definition identifier.</span></span>

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

### <span data-ttu-id="5984d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5984d-124">-InputObject</span></span>
<span data-ttu-id="5984d-125">A registration definition objektum.</span><span class="sxs-lookup"><span data-stu-id="5984d-125">The registration definition object.</span></span>

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

### <span data-ttu-id="5984d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5984d-126">-ResourceId</span></span>
<span data-ttu-id="5984d-127">A regisztrációs definíció ResourceId</span><span class="sxs-lookup"><span data-stu-id="5984d-127">ResourceId of the registration definition</span></span>

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

### <span data-ttu-id="5984d-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5984d-128">-Confirm</span></span>
<span data-ttu-id="5984d-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5984d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5984d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5984d-130">-WhatIf</span></span>
<span data-ttu-id="5984d-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5984d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5984d-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5984d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5984d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5984d-133">CommonParameters</span></span>
<span data-ttu-id="5984d-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5984d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5984d-135">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5984d-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5984d-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5984d-136">INPUTS</span></span>

### <span data-ttu-id="5984d-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="5984d-137">None</span></span>

## <span data-ttu-id="5984d-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5984d-138">OUTPUTS</span></span>

### <span data-ttu-id="5984d-139">Microsoft. Azure. PowerShell. parancsmagok. ManagedServices. models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="5984d-139">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="5984d-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5984d-140">NOTES</span></span>

## <span data-ttu-id="5984d-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5984d-141">RELATED LINKS</span></span>
