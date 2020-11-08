---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigraterunasaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
ms.openlocfilehash: 6f78a326efc29e3ba89f774575df1c4b7472e70c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194587"
---
# <span data-ttu-id="e373b-101">Get-AzMigrateRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="e373b-101">Get-AzMigrateRunAsAccount</span></span>

## <span data-ttu-id="e373b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e373b-102">SYNOPSIS</span></span>
<span data-ttu-id="e373b-103">A fiók futtatásának módja.</span><span class="sxs-lookup"><span data-stu-id="e373b-103">Method to get run as account.</span></span>

## <span data-ttu-id="e373b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e373b-104">SYNTAX</span></span>

### <span data-ttu-id="e373b-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e373b-105">List (Default)</span></span>
```
Get-AzMigrateRunAsAccount -ResourceGroupName <String> -SiteName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e373b-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="e373b-106">Get</span></span>
```
Get-AzMigrateRunAsAccount -AccountName <String> -ResourceGroupName <String> -SiteName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e373b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e373b-107">DESCRIPTION</span></span>
<span data-ttu-id="e373b-108">A fiók futtatásának módja.</span><span class="sxs-lookup"><span data-stu-id="e373b-108">Method to get run as account.</span></span>

## <span data-ttu-id="e373b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e373b-109">EXAMPLES</span></span>

### <span data-ttu-id="e373b-110">Példa 1: lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e373b-110">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="e373b-111">A lista minden futtatása fiókként egy webhelyen</span><span class="sxs-lookup"><span data-stu-id="e373b-111">List all run as accounts in a site.</span></span>

### <span data-ttu-id="e373b-112">2. példa: Get</span><span class="sxs-lookup"><span data-stu-id="e373b-112">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite -AccountName b090bef3-b733-5e34-bc8f-eb6f2701432a

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="e373b-113">A Futtatás fiókként név szerint.</span><span class="sxs-lookup"><span data-stu-id="e373b-113">Get Run as account by name.</span></span>

## <span data-ttu-id="e373b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e373b-114">PARAMETERS</span></span>

### <span data-ttu-id="e373b-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e373b-115">-AccountName</span></span>
<span data-ttu-id="e373b-116">Run as Account ARM név.</span><span class="sxs-lookup"><span data-stu-id="e373b-116">Run as account ARM name.</span></span>

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

### <span data-ttu-id="e373b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e373b-117">-DefaultProfile</span></span>
<span data-ttu-id="e373b-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e373b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e373b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e373b-119">-ResourceGroupName</span></span>
<span data-ttu-id="e373b-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e373b-120">The name of the resource group.</span></span>
<span data-ttu-id="e373b-121">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="e373b-121">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e373b-122">-SiteName</span><span class="sxs-lookup"><span data-stu-id="e373b-122">-SiteName</span></span>
<span data-ttu-id="e373b-123">Webhely neve mezőbe.</span><span class="sxs-lookup"><span data-stu-id="e373b-123">Site name.</span></span>

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

### <span data-ttu-id="e373b-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e373b-124">-SubscriptionId</span></span>
<span data-ttu-id="e373b-125">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e373b-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e373b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e373b-126">CommonParameters</span></span>
<span data-ttu-id="e373b-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e373b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e373b-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e373b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e373b-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e373b-129">INPUTS</span></span>

## <span data-ttu-id="e373b-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e373b-130">OUTPUTS</span></span>

### <span data-ttu-id="e373b-131">Microsoft. Azure. PowerShell. parancsmagok. áttelepítés. models. Api202001. IVMwareRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="e373b-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span></span>

## <span data-ttu-id="e373b-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e373b-132">NOTES</span></span>

<span data-ttu-id="e373b-133">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e373b-133">ALIASES</span></span>

## <span data-ttu-id="e373b-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e373b-134">RELATED LINKS</span></span>
