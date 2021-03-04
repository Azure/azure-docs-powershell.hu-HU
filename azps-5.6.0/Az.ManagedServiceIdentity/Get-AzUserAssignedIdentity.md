---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/powershell/module/az.managedserviceidentity/get-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Get-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Get-AzUserAssignedIdentity.md
ms.openlocfilehash: f908b34b3d16efa1527e65c22364f9aadaa5b647
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930490"
---
# <span data-ttu-id="7d2a8-101">Get-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="7d2a8-101">Get-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="7d2a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d2a8-102">SYNOPSIS</span></span>
<span data-ttu-id="7d2a8-103">Felhasználóhoz rendelt identitást/identitásokat kap.</span><span class="sxs-lookup"><span data-stu-id="7d2a8-103">Gets User Assigned Identity/identities.</span></span>

## <span data-ttu-id="7d2a8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7d2a8-104">SYNTAX</span></span>

### <span data-ttu-id="7d2a8-105">SuscriptionParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7d2a8-105">SuscriptionParameterSet (Default)</span></span>
```
Get-AzUserAssignedIdentity [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d2a8-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d2a8-106">ResourceGroupParameterSet</span></span>
```
Get-AzUserAssignedIdentity -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d2a8-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7d2a8-107">DESCRIPTION</span></span>
<span data-ttu-id="7d2a8-108">A **Get-AzUserAssignedIdentity** meglévő felhasználóhoz rendelt identitásokat kap.</span><span class="sxs-lookup"><span data-stu-id="7d2a8-108">The **Get-AzUserAssignedIdentity** gets existing user assigned identities.</span></span>

## <span data-ttu-id="7d2a8-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7d2a8-109">EXAMPLES</span></span>

### <span data-ttu-id="7d2a8-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="7d2a8-110">Example 1</span></span>
<span data-ttu-id="7d2a8-111">Ez a példa parancsmag lekérte a felhasználóhoz rendelt identitást a PSRG erőforráscsoportban azonosító **1** **névvel**</span><span class="sxs-lookup"><span data-stu-id="7d2a8-111">This example cmdlet gets the User Assigned Identity with name **ID1** under the resource group **PSRG**</span></span>

```powershell
PS C:\> Get-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1

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

### <span data-ttu-id="7d2a8-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="7d2a8-112">Example 2</span></span>
<span data-ttu-id="7d2a8-113">Ez a példa parancsmag az összes felhasználó által hozzárendelt identitást a PSRG erőforráscsoport **alatt kapja meg.**</span><span class="sxs-lookup"><span data-stu-id="7d2a8-113">This example cmdlet gets all the User Assigned Identities under the resource group **PSRG**</span></span>

```powershell
PS C:\> Get-AzUserAssignedIdentity -ResourceGroupName PSRG

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities


Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2

ResourceGroupName : PSRG

Name              : ID2

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

### <span data-ttu-id="7d2a8-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="7d2a8-114">Example 3</span></span>
<span data-ttu-id="7d2a8-115">Ez a példa parancsmag begyakorlja az előfizetéshez rendelt összes felhasználóhoz rendelt identitást.</span><span class="sxs-lookup"><span data-stu-id="7d2a8-115">This example cmdlet gets all the User Assigned Identities under the subscription.</span></span>

```powershell
PS C:\> Get-AzUserAssignedIdentity

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities


Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2

ResourceGroupName : PSRG

Name              : ID2

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities


Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG2/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG2

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG2/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

## <span data-ttu-id="7d2a8-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d2a8-116">PARAMETERS</span></span>

### <span data-ttu-id="7d2a8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d2a8-117">-DefaultProfile</span></span>
<span data-ttu-id="7d2a8-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7d2a8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d2a8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7d2a8-119">-Name</span></span>
<span data-ttu-id="7d2a8-120">Az identitás neve.</span><span class="sxs-lookup"><span data-stu-id="7d2a8-120">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d2a8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d2a8-121">-ResourceGroupName</span></span>
<span data-ttu-id="7d2a8-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7d2a8-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d2a8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d2a8-123">CommonParameters</span></span>
<span data-ttu-id="7d2a8-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d2a8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d2a8-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d2a8-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d2a8-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d2a8-126">INPUTS</span></span>

### <span data-ttu-id="7d2a8-127">System.String</span><span class="sxs-lookup"><span data-stu-id="7d2a8-127">System.String</span></span>

## <span data-ttu-id="7d2a8-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d2a8-128">OUTPUTS</span></span>

### <span data-ttu-id="7d2a8-129">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.psUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="7d2a8-129">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="7d2a8-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7d2a8-130">NOTES</span></span>

## <span data-ttu-id="7d2a8-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d2a8-131">RELATED LINKS</span></span>
