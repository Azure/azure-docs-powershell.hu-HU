---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
ms.openlocfilehash: 336360c3c7aac901ae90ea02f4832a066c6fff12
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469438"
---
# <span data-ttu-id="3ae8d-101">Get-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="3ae8d-101">Get-AzMariaDbReplica</span></span>

## <span data-ttu-id="3ae8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ae8d-102">SYNOPSIS</span></span>
<span data-ttu-id="3ae8d-103">List all the replicas for a given server.</span><span class="sxs-lookup"><span data-stu-id="3ae8d-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="3ae8d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3ae8d-104">SYNTAX</span></span>

```
Get-AzMariaDbReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3ae8d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3ae8d-105">DESCRIPTION</span></span>
<span data-ttu-id="3ae8d-106">List all the replicas for a given server.</span><span class="sxs-lookup"><span data-stu-id="3ae8d-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="3ae8d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3ae8d-107">EXAMPLES</span></span>

### <span data-ttu-id="3ae8d-108">1. példa: Az összes replika DB felsorolása Egy MariaDB alatt</span><span class="sxs-lookup"><span data-stu-id="3ae8d-108">Example 1: List all replica DB under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbReplica -ServerName mariadb-test-szp6dt -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
mariadb-test-szp6dt-rep154 eastus   zcsxhpasdc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="3ae8d-109">Ez a parancs felsorolja az összes replika DB-t egy MariaDB alatt.</span><span class="sxs-lookup"><span data-stu-id="3ae8d-109">This command lists all replica DB under a MariaDB.</span></span>

## <span data-ttu-id="3ae8d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ae8d-110">PARAMETERS</span></span>

### <span data-ttu-id="3ae8d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ae8d-111">-DefaultProfile</span></span>
<span data-ttu-id="3ae8d-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ae8d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ae8d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ae8d-113">-ResourceGroupName</span></span>
<span data-ttu-id="3ae8d-114">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3ae8d-114">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3ae8d-115">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="3ae8d-115">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3ae8d-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3ae8d-116">-ServerName</span></span>
<span data-ttu-id="3ae8d-117">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="3ae8d-117">The name of the server.</span></span>

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

### <span data-ttu-id="3ae8d-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ae8d-118">-SubscriptionId</span></span>
<span data-ttu-id="3ae8d-119">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="3ae8d-119">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="3ae8d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ae8d-120">CommonParameters</span></span>
<span data-ttu-id="3ae8d-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ae8d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ae8d-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ae8d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ae8d-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ae8d-123">INPUTS</span></span>

## <span data-ttu-id="3ae8d-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ae8d-124">OUTPUTS</span></span>

### <span data-ttu-id="3ae8d-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="3ae8d-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="3ae8d-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3ae8d-126">NOTES</span></span>

<span data-ttu-id="3ae8d-127">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3ae8d-127">ALIASES</span></span>

## <span data-ttu-id="3ae8d-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ae8d-128">RELATED LINKS</span></span>

