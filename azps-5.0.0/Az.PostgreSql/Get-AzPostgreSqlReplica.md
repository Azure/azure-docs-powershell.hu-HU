---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
ms.openlocfilehash: 5d27610924fe0b4a92acfb5f7d1e678742d5b5c7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303028"
---
# <span data-ttu-id="67f8d-101">Get-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="67f8d-101">Get-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="67f8d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="67f8d-102">SYNOPSIS</span></span>
<span data-ttu-id="67f8d-103">Egy adott kiszolgáló összes replikájának listázása.</span><span class="sxs-lookup"><span data-stu-id="67f8d-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="67f8d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="67f8d-104">SYNTAX</span></span>

```
Get-AzPostgreSqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="67f8d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="67f8d-105">DESCRIPTION</span></span>
<span data-ttu-id="67f8d-106">Egy adott kiszolgáló összes replikájának listázása.</span><span class="sxs-lookup"><span data-stu-id="67f8d-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="67f8d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="67f8d-107">EXAMPLES</span></span>

### <span data-ttu-id="67f8d-108">Példa 1: a PostgreSql-kiszolgáló replikájának beolvasása az erőforráscsoport és a kiszolgáló neve alapján</span><span class="sxs-lookup"><span data-stu-id="67f8d-108">Example 1: Get PostgreSql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlReplica -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="67f8d-109">Ez a parancsmag a PostgreSql-kiszolgáló replikáját erőforrás csoport és kiszolgálónév szerint kapja.</span><span class="sxs-lookup"><span data-stu-id="67f8d-109">This cmdlet gets PostgreSql server replica by resource group and server name.</span></span>

## <span data-ttu-id="67f8d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="67f8d-110">PARAMETERS</span></span>

### <span data-ttu-id="67f8d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67f8d-111">-DefaultProfile</span></span>
<span data-ttu-id="67f8d-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="67f8d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67f8d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67f8d-113">-ResourceGroupName</span></span>
<span data-ttu-id="67f8d-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="67f8d-114">The name of the resource group.</span></span>
<span data-ttu-id="67f8d-115">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="67f8d-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="67f8d-116">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="67f8d-116">-ServerName</span></span>
<span data-ttu-id="67f8d-117">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="67f8d-117">The name of the server.</span></span>

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

### <span data-ttu-id="67f8d-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67f8d-118">-SubscriptionId</span></span>
<span data-ttu-id="67f8d-119">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="67f8d-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="67f8d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67f8d-120">CommonParameters</span></span>
<span data-ttu-id="67f8d-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="67f8d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67f8d-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="67f8d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67f8d-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="67f8d-123">INPUTS</span></span>

## <span data-ttu-id="67f8d-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67f8d-124">OUTPUTS</span></span>

### <span data-ttu-id="67f8d-125">Microsoft. Azure. PowerShell. parancsmagok. PostgreSql. models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="67f8d-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="67f8d-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="67f8d-126">NOTES</span></span>

<span data-ttu-id="67f8d-127">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="67f8d-127">ALIASES</span></span>

## <span data-ttu-id="67f8d-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67f8d-128">RELATED LINKS</span></span>

