---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
ms.openlocfilehash: ebea7936483a34d2515c69c416146d07651b396b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194584"
---
# <span data-ttu-id="fd8fc-101">Get-AzMigrateSite</span><span class="sxs-lookup"><span data-stu-id="fd8fc-101">Get-AzMigrateSite</span></span>

## <span data-ttu-id="fd8fc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd8fc-102">SYNOPSIS</span></span>
<span data-ttu-id="fd8fc-103">Módszert a webhelyek beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="fd8fc-103">Method to get a site.</span></span>

## <span data-ttu-id="fd8fc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd8fc-104">SYNTAX</span></span>

```
Get-AzMigrateSite -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="fd8fc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd8fc-105">DESCRIPTION</span></span>
<span data-ttu-id="fd8fc-106">Módszert a webhelyek beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="fd8fc-106">Method to get a site.</span></span>

## <span data-ttu-id="fd8fc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fd8fc-107">EXAMPLES</span></span>

### <span data-ttu-id="fd8fc-108">1. példa: beolvasás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd8fc-108">Example 1: Get (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateSite -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

ETag Location      Name                Type
---- --------      ----                ----
     southeastasia BBVMwareAVScbbcsite Microsoft.OffAzure/VMwareSites

```

<span data-ttu-id="fd8fc-109">Webhely beolvasása név szerint</span><span class="sxs-lookup"><span data-stu-id="fd8fc-109">Get site by name</span></span>

## <span data-ttu-id="fd8fc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd8fc-110">PARAMETERS</span></span>

### <span data-ttu-id="fd8fc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd8fc-111">-DefaultProfile</span></span>
<span data-ttu-id="fd8fc-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd8fc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd8fc-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fd8fc-113">-Name</span></span>
<span data-ttu-id="fd8fc-114">Webhely neve mezőbe.</span><span class="sxs-lookup"><span data-stu-id="fd8fc-114">Site name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd8fc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd8fc-115">-ResourceGroupName</span></span>
<span data-ttu-id="fd8fc-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fd8fc-116">The name of the resource group.</span></span>
<span data-ttu-id="fd8fc-117">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="fd8fc-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fd8fc-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fd8fc-118">-SubscriptionId</span></span>
<span data-ttu-id="fd8fc-119">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fd8fc-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fd8fc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd8fc-120">CommonParameters</span></span>
<span data-ttu-id="fd8fc-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd8fc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd8fc-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fd8fc-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd8fc-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd8fc-123">INPUTS</span></span>

## <span data-ttu-id="fd8fc-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd8fc-124">OUTPUTS</span></span>

### <span data-ttu-id="fd8fc-125">Microsoft. Azure. PowerShell. parancsmagok. áttelepítés. models. Api202001. IVMwareSite</span><span class="sxs-lookup"><span data-stu-id="fd8fc-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span></span>

## <span data-ttu-id="fd8fc-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd8fc-126">NOTES</span></span>

<span data-ttu-id="fd8fc-127">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="fd8fc-127">ALIASES</span></span>

## <span data-ttu-id="fd8fc-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd8fc-128">RELATED LINKS</span></span>

