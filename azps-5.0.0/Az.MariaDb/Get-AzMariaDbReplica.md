---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
ms.openlocfilehash: 336360c3c7aac901ae90ea02f4832a066c6fff12
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194615"
---
# <span data-ttu-id="36644-101">Get-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="36644-101">Get-AzMariaDbReplica</span></span>

## <span data-ttu-id="36644-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36644-102">SYNOPSIS</span></span>
<span data-ttu-id="36644-103">Egy adott kiszolgáló összes replikájának listázása.</span><span class="sxs-lookup"><span data-stu-id="36644-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="36644-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36644-104">SYNTAX</span></span>

```
Get-AzMariaDbReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="36644-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="36644-105">DESCRIPTION</span></span>
<span data-ttu-id="36644-106">Egy adott kiszolgáló összes replikájának listázása.</span><span class="sxs-lookup"><span data-stu-id="36644-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="36644-107">Példák</span><span class="sxs-lookup"><span data-stu-id="36644-107">EXAMPLES</span></span>

### <span data-ttu-id="36644-108">1. példa: a replika DB MariaDB listája</span><span class="sxs-lookup"><span data-stu-id="36644-108">Example 1: List all replica DB under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbReplica -ServerName mariadb-test-szp6dt -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
mariadb-test-szp6dt-rep154 eastus   zcsxhpasdc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="36644-109">Ez a parancs a MariaDB alatt lévő összes replika DB-t felsorolja.</span><span class="sxs-lookup"><span data-stu-id="36644-109">This command lists all replica DB under a MariaDB.</span></span>

## <span data-ttu-id="36644-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36644-110">PARAMETERS</span></span>

### <span data-ttu-id="36644-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36644-111">-DefaultProfile</span></span>
<span data-ttu-id="36644-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36644-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36644-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36644-113">-ResourceGroupName</span></span>
<span data-ttu-id="36644-114">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="36644-114">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="36644-115">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="36644-115">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="36644-116">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="36644-116">-ServerName</span></span>
<span data-ttu-id="36644-117">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="36644-117">The name of the server.</span></span>

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

### <span data-ttu-id="36644-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="36644-118">-SubscriptionId</span></span>
<span data-ttu-id="36644-119">Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="36644-119">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="36644-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36644-120">CommonParameters</span></span>
<span data-ttu-id="36644-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36644-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36644-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="36644-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36644-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36644-123">INPUTS</span></span>

## <span data-ttu-id="36644-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36644-124">OUTPUTS</span></span>

### <span data-ttu-id="36644-125">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. modellek. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="36644-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="36644-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36644-126">NOTES</span></span>

<span data-ttu-id="36644-127">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="36644-127">ALIASES</span></span>

## <span data-ttu-id="36644-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36644-128">RELATED LINKS</span></span>

