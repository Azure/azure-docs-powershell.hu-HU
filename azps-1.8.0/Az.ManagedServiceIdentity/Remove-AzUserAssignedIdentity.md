---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/remove-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
ms.openlocfilehash: cf87bb3048139077080263feb71a0f5c9012d719
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835245"
---
# <span data-ttu-id="49223-101">Remove-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="49223-101">Remove-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="49223-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="49223-102">SYNOPSIS</span></span>
<span data-ttu-id="49223-103">Felhasználó által kiosztott identitás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="49223-103">Removes a User Assigned Identity.</span></span>

## <span data-ttu-id="49223-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="49223-104">SYNTAX</span></span>

### <span data-ttu-id="49223-105">ResourceGroupAndNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="49223-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49223-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49223-106">InputObjectParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49223-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49223-107">ResourceIdParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49223-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="49223-108">DESCRIPTION</span></span>
<span data-ttu-id="49223-109">A **Remove-AzUserAssignedIdentity** törli a megadott felhasználó által kiosztott identitást.</span><span class="sxs-lookup"><span data-stu-id="49223-109">The **Remove-AzUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="49223-110">Példák</span><span class="sxs-lookup"><span data-stu-id="49223-110">EXAMPLES</span></span>

### <span data-ttu-id="49223-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="49223-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzurRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="49223-112">Ez a példa parancsmag törli az identitás **ID1** az erőforráscsoport **PSRG** csoportban.</span><span class="sxs-lookup"><span data-stu-id="49223-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="49223-113">Igaz</span><span class="sxs-lookup"><span data-stu-id="49223-113">True</span></span>

## <span data-ttu-id="49223-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="49223-114">PARAMETERS</span></span>

### <span data-ttu-id="49223-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49223-115">-AsJob</span></span>
<span data-ttu-id="49223-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="49223-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49223-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49223-117">-DefaultProfile</span></span>
<span data-ttu-id="49223-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="49223-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49223-119">-Force</span><span class="sxs-lookup"><span data-stu-id="49223-119">-Force</span></span>
<span data-ttu-id="49223-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="49223-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="49223-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49223-121">-InputObject</span></span>
<span data-ttu-id="49223-122">Az identitás objektum.</span><span class="sxs-lookup"><span data-stu-id="49223-122">The Identity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity
Parameter Sets: InputObjectParameterSet
Aliases: Identity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49223-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="49223-123">-Name</span></span>
<span data-ttu-id="49223-124">Az identitás neve.</span><span class="sxs-lookup"><span data-stu-id="49223-124">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49223-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49223-125">-ResourceGroupName</span></span>
<span data-ttu-id="49223-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="49223-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49223-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49223-127">-ResourceId</span></span>
<span data-ttu-id="49223-128">Az identitás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="49223-128">The Identity's resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49223-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="49223-129">-Confirm</span></span>
<span data-ttu-id="49223-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="49223-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49223-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49223-131">-WhatIf</span></span>
<span data-ttu-id="49223-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="49223-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49223-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49223-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49223-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49223-134">CommonParameters</span></span>
<span data-ttu-id="49223-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="49223-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49223-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49223-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49223-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="49223-137">INPUTS</span></span>

### <span data-ttu-id="49223-138">Microsoft. Azure. Command. ManagedServiceIdentity. models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="49223-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

### <span data-ttu-id="49223-139">System. String</span><span class="sxs-lookup"><span data-stu-id="49223-139">System.String</span></span>

## <span data-ttu-id="49223-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49223-140">OUTPUTS</span></span>

### <span data-ttu-id="49223-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="49223-141">System.Boolean</span></span>

## <span data-ttu-id="49223-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="49223-142">NOTES</span></span>

## <span data-ttu-id="49223-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49223-143">RELATED LINKS</span></span>
