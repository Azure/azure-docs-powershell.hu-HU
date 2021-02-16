---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
ms.openlocfilehash: 1f165177871a2d8b425829dddaef6d1f0298cfb4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161387"
---
# <span data-ttu-id="52d13-101">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="52d13-101">New-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="52d13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52d13-102">SYNOPSIS</span></span>
<span data-ttu-id="52d13-103">Létrehoz egy új felhasználóhoz rendelt identitást, vagy frissíti a meglévő felhasználóhoz rendelt identitást.</span><span class="sxs-lookup"><span data-stu-id="52d13-103">Creates a new User Assigned Identity or updates an existing User Assigned Identity.</span></span>

## <span data-ttu-id="52d13-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="52d13-104">SYNTAX</span></span>

```
New-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52d13-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="52d13-105">DESCRIPTION</span></span>
<span data-ttu-id="52d13-106">A **New-AzUserAssignedIdentity** parancsmag létrehoz egy új felhasználóhoz rendelt identitást.</span><span class="sxs-lookup"><span data-stu-id="52d13-106">The **New-AzUserAssignedIdentity** cmdlet creates a new User Assigned Identity.</span></span> <span data-ttu-id="52d13-107">Ha egy már meglévő identitással használja, frissítette az identitást.</span><span class="sxs-lookup"><span data-stu-id="52d13-107">When used with an already existing identity, it updated the identity.</span></span>
<span data-ttu-id="52d13-108">Ha Azure Resource Manager-címkéket szeretne hozzáadni az identitáshoz, használja a Set-AzResource parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="52d13-108">To add Azure Resource Manager tags to the identity, please use the Set-AzResource cmdlet.</span></span>

## <span data-ttu-id="52d13-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="52d13-109">EXAMPLES</span></span>

### <span data-ttu-id="52d13-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="52d13-110">Example 1</span></span>
<span data-ttu-id="52d13-111">Ez a példa parancsmag létrehoz egy  új felhasználóhoz rendelt identitást a PSRG erőforráscsoport **PSRG** csoportjában, az Erőforráscsoport helyén.</span><span class="sxs-lookup"><span data-stu-id="52d13-111">This example cmdlet creates a new User Assigned Identity with name **ID1** under resource group **PSRG** in the location of the ResourceGroup.</span></span>

```powershell
PS C:\> New-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : centralus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

### <span data-ttu-id="52d13-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="52d13-112">Example 2</span></span>
<span data-ttu-id="52d13-113">Ez a példa parancsmag létrehoz egy  új felhasználóhoz rendelt identitást, amely a PSRG erőforráscsoport alatt a **PSRG** nevű erőforráscsoportban található a westus régióban.</span><span class="sxs-lookup"><span data-stu-id="52d13-113">This example cmdlet creates a new User Assigned Identity with name **ID1** under the resource group **PSRG** in the westus region.</span></span>

```powershell
PS C:\> New-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1 -Location westus

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

## <span data-ttu-id="52d13-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52d13-114">PARAMETERS</span></span>

### <span data-ttu-id="52d13-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52d13-115">-AsJob</span></span>
<span data-ttu-id="52d13-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="52d13-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52d13-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52d13-117">-DefaultProfile</span></span>
<span data-ttu-id="52d13-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="52d13-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52d13-119">-Location</span><span class="sxs-lookup"><span data-stu-id="52d13-119">-Location</span></span>
<span data-ttu-id="52d13-120">Az Azure-régió neve, ahol az identitást létre kell hoznunk.</span><span class="sxs-lookup"><span data-stu-id="52d13-120">The Azure region name where the Identity should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52d13-121">-Name</span><span class="sxs-lookup"><span data-stu-id="52d13-121">-Name</span></span>
<span data-ttu-id="52d13-122">Az identitás neve.</span><span class="sxs-lookup"><span data-stu-id="52d13-122">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52d13-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52d13-123">-ResourceGroupName</span></span>
<span data-ttu-id="52d13-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="52d13-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52d13-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="52d13-125">-Tag</span></span>
<span data-ttu-id="52d13-126">Az identitáshoz társított Azure Resource Manager-címkék.</span><span class="sxs-lookup"><span data-stu-id="52d13-126">The Azure Resource Manager tags associated with the identity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52d13-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52d13-127">-Confirm</span></span>
<span data-ttu-id="52d13-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="52d13-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52d13-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52d13-129">-WhatIf</span></span>
<span data-ttu-id="52d13-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="52d13-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52d13-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="52d13-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52d13-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d13-132">CommonParameters</span></span>
<span data-ttu-id="52d13-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52d13-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d13-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52d13-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d13-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52d13-135">INPUTS</span></span>

### <span data-ttu-id="52d13-136">System.String</span><span class="sxs-lookup"><span data-stu-id="52d13-136">System.String</span></span>

### <span data-ttu-id="52d13-137">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="52d13-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="52d13-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52d13-138">OUTPUTS</span></span>

### <span data-ttu-id="52d13-139">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="52d13-139">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="52d13-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="52d13-140">NOTES</span></span>

## <span data-ttu-id="52d13-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52d13-141">RELATED LINKS</span></span>
