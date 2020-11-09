---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
ms.openlocfilehash: 80f9e645c1c906e8275d3e25fb2ab833befa9328
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296786"
---
# <span data-ttu-id="134f1-101">Get-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="134f1-101">Get-AzMySqlReplica</span></span>

## <span data-ttu-id="134f1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="134f1-102">SYNOPSIS</span></span>
<span data-ttu-id="134f1-103">Egy adott kiszolgáló összes replikájának listázása.</span><span class="sxs-lookup"><span data-stu-id="134f1-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="134f1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="134f1-104">SYNTAX</span></span>

```
Get-AzMySqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="134f1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="134f1-105">DESCRIPTION</span></span>
<span data-ttu-id="134f1-106">Egy adott kiszolgáló összes replikájának listázása.</span><span class="sxs-lookup"><span data-stu-id="134f1-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="134f1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="134f1-107">EXAMPLES</span></span>

### <span data-ttu-id="134f1-108">Példa 1: a MySql-kiszolgáló replikájának beszerzése az erőforráscsoport és a kiszolgáló neve szerint</span><span class="sxs-lookup"><span data-stu-id="134f1-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="134f1-109">Ez a parancsmag a MySql-kiszolgáló replikáját erőforrás csoport és kiszolgálónév szerint kapja.</span><span class="sxs-lookup"><span data-stu-id="134f1-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="134f1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="134f1-110">PARAMETERS</span></span>

### <span data-ttu-id="134f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="134f1-111">-DefaultProfile</span></span>
<span data-ttu-id="134f1-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="134f1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="134f1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="134f1-113">-ResourceGroupName</span></span>
<span data-ttu-id="134f1-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="134f1-114">The name of the resource group.</span></span>
<span data-ttu-id="134f1-115">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="134f1-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="134f1-116">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="134f1-116">-ServerName</span></span>
<span data-ttu-id="134f1-117">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="134f1-117">The name of the server.</span></span>

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

### <span data-ttu-id="134f1-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="134f1-118">-SubscriptionId</span></span>
<span data-ttu-id="134f1-119">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="134f1-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="134f1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="134f1-120">CommonParameters</span></span>
<span data-ttu-id="134f1-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="134f1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="134f1-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="134f1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="134f1-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="134f1-123">INPUTS</span></span>

## <span data-ttu-id="134f1-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="134f1-124">OUTPUTS</span></span>

### <span data-ttu-id="134f1-125">Microsoft. Azure. PowerShell. parancsmagok. MySql. models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="134f1-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="134f1-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="134f1-126">NOTES</span></span>

<span data-ttu-id="134f1-127">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="134f1-127">ALIASES</span></span>

## <span data-ttu-id="134f1-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="134f1-128">RELATED LINKS</span></span>

