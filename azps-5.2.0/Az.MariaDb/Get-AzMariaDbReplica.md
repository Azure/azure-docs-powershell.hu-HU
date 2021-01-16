---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
ms.openlocfilehash: 336360c3c7aac901ae90ea02f4832a066c6fff12
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324151"
---
# <span data-ttu-id="ce346-101">Get-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="ce346-101">Get-AzMariaDbReplica</span></span>

## <span data-ttu-id="ce346-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce346-102">SYNOPSIS</span></span>
<span data-ttu-id="ce346-103">List all the replicas for a given server.</span><span class="sxs-lookup"><span data-stu-id="ce346-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="ce346-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ce346-104">SYNTAX</span></span>

```
Get-AzMariaDbReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ce346-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ce346-105">DESCRIPTION</span></span>
<span data-ttu-id="ce346-106">List all the replicas for a given server.</span><span class="sxs-lookup"><span data-stu-id="ce346-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="ce346-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ce346-107">EXAMPLES</span></span>

### <span data-ttu-id="ce346-108">1. példa: Az összes replika DB felsorolása Egy MariaDB alatt</span><span class="sxs-lookup"><span data-stu-id="ce346-108">Example 1: List all replica DB under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbReplica -ServerName mariadb-test-szp6dt -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
mariadb-test-szp6dt-rep154 eastus   zcsxhpasdc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="ce346-109">Ez a parancs felsorolja az összes replika DB-t egy MariaDB alatt.</span><span class="sxs-lookup"><span data-stu-id="ce346-109">This command lists all replica DB under a MariaDB.</span></span>

## <span data-ttu-id="ce346-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce346-110">PARAMETERS</span></span>

### <span data-ttu-id="ce346-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce346-111">-DefaultProfile</span></span>
<span data-ttu-id="ce346-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ce346-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce346-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce346-113">-ResourceGroupName</span></span>
<span data-ttu-id="ce346-114">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ce346-114">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ce346-115">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="ce346-115">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ce346-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ce346-116">-ServerName</span></span>
<span data-ttu-id="ce346-117">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="ce346-117">The name of the server.</span></span>

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

### <span data-ttu-id="ce346-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ce346-118">-SubscriptionId</span></span>
<span data-ttu-id="ce346-119">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="ce346-119">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="ce346-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce346-120">CommonParameters</span></span>
<span data-ttu-id="ce346-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce346-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce346-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce346-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce346-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ce346-123">INPUTS</span></span>

## <span data-ttu-id="ce346-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce346-124">OUTPUTS</span></span>

### <span data-ttu-id="ce346-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="ce346-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="ce346-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ce346-126">NOTES</span></span>

<span data-ttu-id="ce346-127">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ce346-127">ALIASES</span></span>

## <span data-ttu-id="ce346-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce346-128">RELATED LINKS</span></span>

