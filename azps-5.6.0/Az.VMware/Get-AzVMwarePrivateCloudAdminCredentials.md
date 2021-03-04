---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 88ecb5baff31ddcc27ce090f19a868c4d393c588
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936401"
---
# <span data-ttu-id="1a623-101">Get-AzVMWarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="1a623-101">Get-AzVMWarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="1a623-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a623-102">SYNOPSIS</span></span>
<span data-ttu-id="1a623-103">A privát felhőhöz szükséges rendszergazdai hitelesítő adatok felsorolása</span><span class="sxs-lookup"><span data-stu-id="1a623-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="1a623-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1a623-104">SYNTAX</span></span>

```
Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1a623-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1a623-105">DESCRIPTION</span></span>
<span data-ttu-id="1a623-106">A privát felhőhöz szükséges rendszergazdai hitelesítő adatok felsorolása</span><span class="sxs-lookup"><span data-stu-id="1a623-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="1a623-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1a623-107">EXAMPLES</span></span>

### <span data-ttu-id="1a623-108">1. példa: A privát felhő rendszergazdai hitelesítő adatainak lekérte</span><span class="sxs-lookup"><span data-stu-id="1a623-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="1a623-109">A privát felhő rendszergazdai hitelesítő adatainak lekérte</span><span class="sxs-lookup"><span data-stu-id="1a623-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="1a623-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a623-110">PARAMETERS</span></span>

### <span data-ttu-id="1a623-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a623-111">-DefaultProfile</span></span>
<span data-ttu-id="1a623-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1a623-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a623-113">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="1a623-113">-PrivateCloudName</span></span>
<span data-ttu-id="1a623-114">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="1a623-114">Name of the private cloud</span></span>

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

### <span data-ttu-id="1a623-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a623-115">-ResourceGroupName</span></span>
<span data-ttu-id="1a623-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1a623-116">The name of the resource group.</span></span>
<span data-ttu-id="1a623-117">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="1a623-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1a623-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1a623-118">-SubscriptionId</span></span>
<span data-ttu-id="1a623-119">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1a623-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1a623-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a623-120">-Confirm</span></span>
<span data-ttu-id="1a623-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1a623-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a623-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a623-122">-WhatIf</span></span>
<span data-ttu-id="1a623-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1a623-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a623-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1a623-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a623-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a623-125">CommonParameters</span></span>
<span data-ttu-id="1a623-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a623-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a623-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a623-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a623-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a623-128">INPUTS</span></span>

## <span data-ttu-id="1a623-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a623-129">OUTPUTS</span></span>

### <span data-ttu-id="1a623-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="1a623-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="1a623-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1a623-131">NOTES</span></span>

<span data-ttu-id="1a623-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="1a623-132">ALIASES</span></span>

## <span data-ttu-id="1a623-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1a623-133">RELATED LINKS</span></span>

