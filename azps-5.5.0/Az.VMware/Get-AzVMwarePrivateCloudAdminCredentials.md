---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 7502bbd96371aa505d8d927dfb9a491c2ca32b34
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207511"
---
# <span data-ttu-id="9a665-101">Get-AzVMwarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="9a665-101">Get-AzVMwarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="9a665-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a665-102">SYNOPSIS</span></span>
<span data-ttu-id="9a665-103">A privát felhőhöz szükséges rendszergazdai hitelesítő adatok felsorolása</span><span class="sxs-lookup"><span data-stu-id="9a665-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="9a665-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9a665-104">SYNTAX</span></span>

```
Get-AzVMwarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9a665-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9a665-105">DESCRIPTION</span></span>
<span data-ttu-id="9a665-106">A privát felhőhöz használt rendszergazdai hitelesítő adatok felsorolása</span><span class="sxs-lookup"><span data-stu-id="9a665-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="9a665-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9a665-107">EXAMPLES</span></span>

### <span data-ttu-id="9a665-108">1. példa: A privát felhő rendszergazdai hitelesítő adatainak lekérte</span><span class="sxs-lookup"><span data-stu-id="9a665-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMwarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="9a665-109">A privát felhő rendszergazdai hitelesítő adatainak lekérte</span><span class="sxs-lookup"><span data-stu-id="9a665-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="9a665-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a665-110">PARAMETERS</span></span>

### <span data-ttu-id="9a665-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a665-111">-DefaultProfile</span></span>
<span data-ttu-id="9a665-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a665-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a665-113">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="9a665-113">-PrivateCloudName</span></span>
<span data-ttu-id="9a665-114">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="9a665-114">Name of the private cloud</span></span>

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

### <span data-ttu-id="9a665-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a665-115">-ResourceGroupName</span></span>
<span data-ttu-id="9a665-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9a665-116">The name of the resource group.</span></span>
<span data-ttu-id="9a665-117">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="9a665-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9a665-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9a665-118">-SubscriptionId</span></span>
<span data-ttu-id="9a665-119">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9a665-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a665-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a665-120">-Confirm</span></span>
<span data-ttu-id="9a665-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9a665-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a665-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a665-122">-WhatIf</span></span>
<span data-ttu-id="9a665-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9a665-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a665-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9a665-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a665-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a665-125">CommonParameters</span></span>
<span data-ttu-id="9a665-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a665-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a665-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a665-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a665-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a665-128">INPUTS</span></span>

## <span data-ttu-id="9a665-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a665-129">OUTPUTS</span></span>

### <span data-ttu-id="9a665-130">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="9a665-130">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="9a665-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9a665-131">NOTES</span></span>

<span data-ttu-id="9a665-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9a665-132">ALIASES</span></span>

## <span data-ttu-id="9a665-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a665-133">RELATED LINKS</span></span>

