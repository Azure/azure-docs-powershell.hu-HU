---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigraterunasaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
ms.openlocfilehash: 6f78a326efc29e3ba89f774575df1c4b7472e70c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152331"
---
# <span data-ttu-id="9cea1-101">Get-AzMigrateRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="9cea1-101">Get-AzMigrateRunAsAccount</span></span>

## <span data-ttu-id="9cea1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cea1-102">SYNOPSIS</span></span>
<span data-ttu-id="9cea1-103">A fiókként való futtatás módja.</span><span class="sxs-lookup"><span data-stu-id="9cea1-103">Method to get run as account.</span></span>

## <span data-ttu-id="9cea1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9cea1-104">SYNTAX</span></span>

### <span data-ttu-id="9cea1-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9cea1-105">List (Default)</span></span>
```
Get-AzMigrateRunAsAccount -ResourceGroupName <String> -SiteName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9cea1-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="9cea1-106">Get</span></span>
```
Get-AzMigrateRunAsAccount -AccountName <String> -ResourceGroupName <String> -SiteName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9cea1-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9cea1-107">DESCRIPTION</span></span>
<span data-ttu-id="9cea1-108">A fiókként való futtatás módja.</span><span class="sxs-lookup"><span data-stu-id="9cea1-108">Method to get run as account.</span></span>

## <span data-ttu-id="9cea1-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9cea1-109">EXAMPLES</span></span>

### <span data-ttu-id="9cea1-110">1. példa: Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9cea1-110">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="9cea1-111">List all run as accounts in a site.</span><span class="sxs-lookup"><span data-stu-id="9cea1-111">List all run as accounts in a site.</span></span>

### <span data-ttu-id="9cea1-112">2. példa: Get</span><span class="sxs-lookup"><span data-stu-id="9cea1-112">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite -AccountName b090bef3-b733-5e34-bc8f-eb6f2701432a

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="9cea1-113">A Futtatás fiókként név alapján.</span><span class="sxs-lookup"><span data-stu-id="9cea1-113">Get Run as account by name.</span></span>

## <span data-ttu-id="9cea1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cea1-114">PARAMETERS</span></span>

### <span data-ttu-id="9cea1-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9cea1-115">-AccountName</span></span>
<span data-ttu-id="9cea1-116">Futtassa fióknév ARM néven.</span><span class="sxs-lookup"><span data-stu-id="9cea1-116">Run as account ARM name.</span></span>

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

### <span data-ttu-id="9cea1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cea1-117">-DefaultProfile</span></span>
<span data-ttu-id="9cea1-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9cea1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cea1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cea1-119">-ResourceGroupName</span></span>
<span data-ttu-id="9cea1-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9cea1-120">The name of the resource group.</span></span>
<span data-ttu-id="9cea1-121">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="9cea1-121">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9cea1-122">-SiteName</span><span class="sxs-lookup"><span data-stu-id="9cea1-122">-SiteName</span></span>
<span data-ttu-id="9cea1-123">Webhely neve.</span><span class="sxs-lookup"><span data-stu-id="9cea1-123">Site name.</span></span>

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

### <span data-ttu-id="9cea1-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9cea1-124">-SubscriptionId</span></span>
<span data-ttu-id="9cea1-125">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9cea1-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9cea1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cea1-126">CommonParameters</span></span>
<span data-ttu-id="9cea1-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cea1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cea1-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9cea1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cea1-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9cea1-129">INPUTS</span></span>

## <span data-ttu-id="9cea1-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cea1-130">OUTPUTS</span></span>

### <span data-ttu-id="9cea1-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="9cea1-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span></span>

## <span data-ttu-id="9cea1-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9cea1-132">NOTES</span></span>

<span data-ttu-id="9cea1-133">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9cea1-133">ALIASES</span></span>

## <span data-ttu-id="9cea1-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9cea1-134">RELATED LINKS</span></span>

