---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
ms.openlocfilehash: ebea7936483a34d2515c69c416146d07651b396b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147442"
---
# <span data-ttu-id="a5a16-101">Get-AzMigrateSite</span><span class="sxs-lookup"><span data-stu-id="a5a16-101">Get-AzMigrateSite</span></span>

## <span data-ttu-id="a5a16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5a16-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a16-103">A webhely szerezze be a módszerét.</span><span class="sxs-lookup"><span data-stu-id="a5a16-103">Method to get a site.</span></span>

## <span data-ttu-id="a5a16-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a5a16-104">SYNTAX</span></span>

```
Get-AzMigrateSite -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a5a16-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a5a16-105">DESCRIPTION</span></span>
<span data-ttu-id="a5a16-106">A webhely szerezze be a módszerét.</span><span class="sxs-lookup"><span data-stu-id="a5a16-106">Method to get a site.</span></span>

## <span data-ttu-id="a5a16-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a5a16-107">EXAMPLES</span></span>

### <span data-ttu-id="a5a16-108">1. példa: Bejl (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a5a16-108">Example 1: Get (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateSite -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

ETag Location      Name                Type
---- --------      ----                ----
     southeastasia BBVMwareAVScbbcsite Microsoft.OffAzure/VMwareSites

```

<span data-ttu-id="a5a16-109">Webhely lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="a5a16-109">Get site by name</span></span>

## <span data-ttu-id="a5a16-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5a16-110">PARAMETERS</span></span>

### <span data-ttu-id="a5a16-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a16-111">-DefaultProfile</span></span>
<span data-ttu-id="a5a16-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5a16-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5a16-113">-Name</span><span class="sxs-lookup"><span data-stu-id="a5a16-113">-Name</span></span>
<span data-ttu-id="a5a16-114">Webhely neve.</span><span class="sxs-lookup"><span data-stu-id="a5a16-114">Site name.</span></span>

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

### <span data-ttu-id="a5a16-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5a16-115">-ResourceGroupName</span></span>
<span data-ttu-id="a5a16-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a5a16-116">The name of the resource group.</span></span>
<span data-ttu-id="a5a16-117">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="a5a16-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a5a16-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5a16-118">-SubscriptionId</span></span>
<span data-ttu-id="a5a16-119">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a5a16-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a5a16-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a16-120">CommonParameters</span></span>
<span data-ttu-id="a5a16-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5a16-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a16-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5a16-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a16-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5a16-123">INPUTS</span></span>

## <span data-ttu-id="a5a16-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5a16-124">OUTPUTS</span></span>

### <span data-ttu-id="a5a16-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span><span class="sxs-lookup"><span data-stu-id="a5a16-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span></span>

## <span data-ttu-id="a5a16-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a5a16-126">NOTES</span></span>

<span data-ttu-id="a5a16-127">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a5a16-127">ALIASES</span></span>

## <span data-ttu-id="a5a16-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5a16-128">RELATED LINKS</span></span>

