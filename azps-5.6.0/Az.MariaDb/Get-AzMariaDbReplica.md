---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
ms.openlocfilehash: c6fef537c3a0cc01bd2de01e00b69c1a69f81e3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927945"
---
# <span data-ttu-id="b8287-101">Get-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="b8287-101">Get-AzMariaDbReplica</span></span>

## <span data-ttu-id="b8287-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8287-102">SYNOPSIS</span></span>
<span data-ttu-id="b8287-103">List all the replicas for a given server.</span><span class="sxs-lookup"><span data-stu-id="b8287-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="b8287-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b8287-104">SYNTAX</span></span>

```
Get-AzMariaDbReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b8287-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b8287-105">DESCRIPTION</span></span>
<span data-ttu-id="b8287-106">List all the replicas for a given server.</span><span class="sxs-lookup"><span data-stu-id="b8287-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="b8287-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b8287-107">EXAMPLES</span></span>

### <span data-ttu-id="b8287-108">1. példa: Az összes replika DB felsorolása Egy MariaDB alatt</span><span class="sxs-lookup"><span data-stu-id="b8287-108">Example 1: List all replica DB under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbReplica -ServerName mariadb-test-szp6dt -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
mariadb-test-szp6dt-rep154 eastus   zcsxhpasdc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="b8287-109">Ez a parancs felsorolja az összes replika DB-t egy MariaDB alatt.</span><span class="sxs-lookup"><span data-stu-id="b8287-109">This command lists all replica DB under a MariaDB.</span></span>

## <span data-ttu-id="b8287-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8287-110">PARAMETERS</span></span>

### <span data-ttu-id="b8287-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8287-111">-DefaultProfile</span></span>
<span data-ttu-id="b8287-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b8287-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8287-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8287-113">-ResourceGroupName</span></span>
<span data-ttu-id="b8287-114">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b8287-114">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b8287-115">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="b8287-115">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b8287-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b8287-116">-ServerName</span></span>
<span data-ttu-id="b8287-117">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="b8287-117">The name of the server.</span></span>

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

### <span data-ttu-id="b8287-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b8287-118">-SubscriptionId</span></span>
<span data-ttu-id="b8287-119">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="b8287-119">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="b8287-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8287-120">CommonParameters</span></span>
<span data-ttu-id="b8287-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8287-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8287-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8287-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8287-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8287-123">INPUTS</span></span>

## <span data-ttu-id="b8287-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8287-124">OUTPUTS</span></span>

### <span data-ttu-id="b8287-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="b8287-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="b8287-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b8287-126">NOTES</span></span>

<span data-ttu-id="b8287-127">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b8287-127">ALIASES</span></span>

## <span data-ttu-id="b8287-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8287-128">RELATED LINKS</span></span>

