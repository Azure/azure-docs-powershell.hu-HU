---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigraterunasaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
ms.openlocfilehash: d028e66fc5f1f4b2c3ab520bd76615e8e9e79099
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934025"
---
# <span data-ttu-id="4d66e-101">Get-AzMigrateRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="4d66e-101">Get-AzMigrateRunAsAccount</span></span>

## <span data-ttu-id="4d66e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d66e-102">SYNOPSIS</span></span>
<span data-ttu-id="4d66e-103">A fiókként való futtatás módja.</span><span class="sxs-lookup"><span data-stu-id="4d66e-103">Method to get run as account.</span></span>

## <span data-ttu-id="4d66e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4d66e-104">SYNTAX</span></span>

### <span data-ttu-id="4d66e-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4d66e-105">List (Default)</span></span>
```
Get-AzMigrateRunAsAccount -ResourceGroupName <String> -SiteName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4d66e-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="4d66e-106">Get</span></span>
```
Get-AzMigrateRunAsAccount -AccountName <String> -ResourceGroupName <String> -SiteName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4d66e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4d66e-107">DESCRIPTION</span></span>
<span data-ttu-id="4d66e-108">A fiókként való futtatás módja.</span><span class="sxs-lookup"><span data-stu-id="4d66e-108">Method to get run as account.</span></span>

## <span data-ttu-id="4d66e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4d66e-109">EXAMPLES</span></span>

### <span data-ttu-id="4d66e-110">1. példa: Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4d66e-110">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="4d66e-111">List all run as accounts in a site.</span><span class="sxs-lookup"><span data-stu-id="4d66e-111">List all run as accounts in a site.</span></span>

### <span data-ttu-id="4d66e-112">2. példa: Get</span><span class="sxs-lookup"><span data-stu-id="4d66e-112">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite -AccountName b090bef3-b733-5e34-bc8f-eb6f2701432a

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="4d66e-113">A Futtatás fiókként név alapján.</span><span class="sxs-lookup"><span data-stu-id="4d66e-113">Get Run as account by name.</span></span>

## <span data-ttu-id="4d66e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d66e-114">PARAMETERS</span></span>

### <span data-ttu-id="4d66e-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4d66e-115">-AccountName</span></span>
<span data-ttu-id="4d66e-116">Futtassa fióknév ARM néven.</span><span class="sxs-lookup"><span data-stu-id="4d66e-116">Run as account ARM name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d66e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d66e-117">-DefaultProfile</span></span>
<span data-ttu-id="4d66e-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d66e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d66e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d66e-119">-ResourceGroupName</span></span>
<span data-ttu-id="4d66e-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4d66e-120">The name of the resource group.</span></span>
<span data-ttu-id="4d66e-121">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="4d66e-121">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4d66e-122">-SiteName</span><span class="sxs-lookup"><span data-stu-id="4d66e-122">-SiteName</span></span>
<span data-ttu-id="4d66e-123">Webhely neve.</span><span class="sxs-lookup"><span data-stu-id="4d66e-123">Site name.</span></span>

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

### <span data-ttu-id="4d66e-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4d66e-124">-SubscriptionId</span></span>
<span data-ttu-id="4d66e-125">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4d66e-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4d66e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d66e-126">CommonParameters</span></span>
<span data-ttu-id="4d66e-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d66e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d66e-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d66e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d66e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d66e-129">INPUTS</span></span>

## <span data-ttu-id="4d66e-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d66e-130">OUTPUTS</span></span>

### <span data-ttu-id="4d66e-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="4d66e-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span></span>

## <span data-ttu-id="4d66e-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4d66e-132">NOTES</span></span>

<span data-ttu-id="4d66e-133">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="4d66e-133">ALIASES</span></span>

## <span data-ttu-id="4d66e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d66e-134">RELATED LINKS</span></span>

