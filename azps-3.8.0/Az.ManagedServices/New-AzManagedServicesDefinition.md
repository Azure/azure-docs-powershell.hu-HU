---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: 6c9c4b562acbf80dba9b1b414345d5eb8e3ecc60
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014197"
---
# <span data-ttu-id="3479e-101">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="3479e-101">New-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="3479e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3479e-102">SYNOPSIS</span></span>
<span data-ttu-id="3479e-103">Regisztrációs definíciót hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="3479e-103">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="3479e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3479e-104">SYNTAX</span></span>

### <span data-ttu-id="3479e-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3479e-105">Default (Default)</span></span>
```
New-AzManagedServicesDefinition -Name <String> -ManagedByTenantId <String>
 -PrincipalId <String> -RoleDefinitionId <String> [-Description <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3479e-106">ByPlan</span><span class="sxs-lookup"><span data-stu-id="3479e-106">ByPlan</span></span>
```
New-AzManagedServicesDefinition -Name <String> -ManagedByTenantId <String>
 -PrincipalId <String> -RoleDefinitionId <String> [-Description <String>] -PlanName <String>
 -PlanPublisher <String> -PlanProduct <String> -PlanVersion <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3479e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3479e-107">DESCRIPTION</span></span>
<span data-ttu-id="3479e-108">Regisztrációs definíciót hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="3479e-108">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="3479e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3479e-109">EXAMPLES</span></span>

### <span data-ttu-id="3479e-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3479e-110">Example 1</span></span>
```powershell
PS C:\> PS C:\> New-AzManagedServicesDefinition -Name name -ManagedByTenantId bab3375b-6197-4a15-a44b-16c41faa91d7 -PrincipalId d6f6c88a-5b7a-455e-ba40-ce146d4d3671 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -Description mydef

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
fdad02a1-a715-4352-844f-2923233590da bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="3479e-111">A kötelező paramétereket tartalmazó regisztrációs definíciót hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="3479e-111">Creates or updates a registration definition given the required parameters.</span></span>

### <span data-ttu-id="3479e-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="3479e-112">Example 2</span></span>
```powershell
PS C> New-AzManagedServicesDefinition -Name asd -ManagedByTenantId "bab3375b-6197-4a15-a44b-16c41faa91d7" -PrincipalId "d6f6c88a-5b7a-455e-ba40-ce146d4d3671" -RoleDefinitionId "acdd72a7-3385-48ef-bd42-f606fba81ae7" -PlanName plan -PlanPublisher publisher -PlanProduct product -PlanVersion 0.1

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
8cde7c19-1750-468e-973e-b711549edc35 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="3479e-113">Regisztrációs definíciót hoz létre vagy frissít a terv részleteivel.</span><span class="sxs-lookup"><span data-stu-id="3479e-113">Creates or updates a registration definition with the plan details.</span></span>

## <span data-ttu-id="3479e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3479e-114">PARAMETERS</span></span>

### <span data-ttu-id="3479e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3479e-115">-AsJob</span></span>
<span data-ttu-id="3479e-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3479e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3479e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3479e-117">-DefaultProfile</span></span>
<span data-ttu-id="3479e-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3479e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3479e-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="3479e-119">-Description</span></span>
<span data-ttu-id="3479e-120">A regisztráció definíciójának leírása.</span><span class="sxs-lookup"><span data-stu-id="3479e-120">The description of the Registration Definition.</span></span>

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

### <span data-ttu-id="3479e-121">-ManagedByTenantId</span><span class="sxs-lookup"><span data-stu-id="3479e-121">-ManagedByTenantId</span></span>
<span data-ttu-id="3479e-122">A ManagedBy bérlői azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3479e-122">The ManagedBy Tenant Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3479e-123">-PlanName</span><span class="sxs-lookup"><span data-stu-id="3479e-123">-PlanName</span></span>
<span data-ttu-id="3479e-124">A terv neve.</span><span class="sxs-lookup"><span data-stu-id="3479e-124">The name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3479e-125">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="3479e-125">-PlanProduct</span></span>
<span data-ttu-id="3479e-126">A szorzat neve.</span><span class="sxs-lookup"><span data-stu-id="3479e-126">The name of the Product.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3479e-127">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="3479e-127">-PlanPublisher</span></span>
<span data-ttu-id="3479e-128">A közzétevő neve.</span><span class="sxs-lookup"><span data-stu-id="3479e-128">The name of the Publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3479e-129">-PlanVersion</span><span class="sxs-lookup"><span data-stu-id="3479e-129">-PlanVersion</span></span>
<span data-ttu-id="3479e-130">A terv verziószáma.</span><span class="sxs-lookup"><span data-stu-id="3479e-130">The version number of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3479e-131">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="3479e-131">-PrincipalId</span></span>
<span data-ttu-id="3479e-132">Az ManagedBy-azonosító.</span><span class="sxs-lookup"><span data-stu-id="3479e-132">The ManagedBy Principal Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3479e-133">-RegistrationDefinitionName</span><span class="sxs-lookup"><span data-stu-id="3479e-133">-RegistrationDefinitionName</span></span>
<span data-ttu-id="3479e-134">A regisztráció definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="3479e-134">The name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3479e-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="3479e-135">-RoleDefinitionId</span></span>
<span data-ttu-id="3479e-136">A felügyelt szolgáltató szerepkör-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3479e-136">The Managed Service Provider's Role Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3479e-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3479e-137">-Confirm</span></span>
<span data-ttu-id="3479e-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3479e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3479e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3479e-139">-WhatIf</span></span>
<span data-ttu-id="3479e-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3479e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3479e-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3479e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3479e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3479e-142">CommonParameters</span></span>
<span data-ttu-id="3479e-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3479e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3479e-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3479e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3479e-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3479e-145">INPUTS</span></span>

### <span data-ttu-id="3479e-146">Nincs</span><span class="sxs-lookup"><span data-stu-id="3479e-146">None</span></span>

## <span data-ttu-id="3479e-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3479e-147">OUTPUTS</span></span>

### <span data-ttu-id="3479e-148">Microsoft. Azure. PowerShell. parancsmagok. ManagedServices. models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="3479e-148">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="3479e-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3479e-149">NOTES</span></span>

## <span data-ttu-id="3479e-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3479e-150">RELATED LINKS</span></span>
